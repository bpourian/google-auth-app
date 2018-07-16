# Google Authenticator App (Java)

This application is using the TOTP (Time-Based One-Time Password Algorithm) [RFC6238](https://tools.ietf.org/html/rfc6238) to 
generate a 6 digit code which is generally used when 2FA is activated on your account.

I first use the existing Java libraries to create a `secret key`. This is 20 bytes encoded as a base32 string.
This is what your 'Google Authenticator' expects. Typically you can manually enter this or in the case of this application
I have used this secret key and the [Google ZXing library](https://github.com/zxing/zxing) to generate a QR code
which can be scanned directly via the authenticator app. This sets your account up and starts generating the 6 digit numbers required.

Material used to create this app - [Blog](http://www.asaph.org/2016/04/google-authenticator-2fa-java.html)


