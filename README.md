Introduction
====================

This is a project which implements google FCM.

Requirements
---------------------

* XCode
* iOS 8
* Google Account

_A code signing key from Apple is required to deploy apps to a device.
Without a developer key, the app can only be installed on the iPhone/iPad Simulator._
__FCM is only work on device__

Create Apple Project
---------------------

1. Login to [Apple Developer Console](https://developer.apple.com/account/ios/identifier/bundle)
2. Choose the App IDs under section Identifiers
3. Press the __+__ icon on the right hand corner
4. Input the App ID Description and Bundle ID
5. __Check the box of Push Notification__
6. Project is created and double check row __Push Notification__ has the yellow light on with the word Configurable
7. Click __Register__

Generate CSR
-------------------------

1. Open Keychain Access
2. Click __Keychain Access__ on the left hand corner
3. Click __Certificate Assistant__ -> __Request a Certificate From a Certificate Authority...__
4. Choose __Save to disk__
5. Save the CSR

Generate SSL Certificate
---------------------------

1. Back to [Apple Developer Console](https://developer.apple.com/account/ios/identifier/bundle)
2. Choose the App IDs under section Identifiers
3. Choose the project created just now
4. Click __Edit__
5. In the Push Notifications section, you can see two boxes, one is for Development and another is Production.  Click __Create Certificate__
6. Choose the CSR generated just now
7. Download the Certificate

Create Firebase Project
------------------------

1. Register a google account for configuring the Firebase project. (If you have one, skip this)
2. Create a project in [Firebase Console](https://console.firebase.google.com)
3. Enter a prject name and select your country
4. Choose iOS and enter the app information

Upload Certificate to Firebase Project
--------------------------------------

1. Double Click the Certificate your downloaded from [Apple Developer Console](https://developer.apple.com/account/ios/identifier/bundle)
2. It will take you to the Keychain Access, find the certificate of your project
3. Right the project and generate a p12 file
4. Click the setting next to your project name in [Firebase Console](https://console.firebase.google.com)
5. Choose __Project Setting__
6. Choose __CLOUD MESSAGING__ on the top tab menu
7. Upload the p12 file


