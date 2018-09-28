## Objective
The main objective of this blog post is to help you understand the implementation of **Push Notification in Unity using Pushwoosh**.

It is very useful for developers who don’t have much idea about this function in Unity. Pushwoosh SDK is used for this purpose.

## Step 1 : Configure YOUR APP ID at Developer Portal

- Create an app at [Apple Developer Portal](https://developer.apple.com/).
- Enable Push Notification in AppID and configure Development SSL Certificate and Production SSL Certificate.
- Download Development SSL Certificate and install it – get APNS development iOS from development tab and install it.
- Now, open keychain access and right click on installed certificate and click on export and select the file format p12.
- To prevent the miss use of this file, set the password. i.e. 12345

## Step 2 : Pushwoosh Configuration

Open [Pushwoosh](https://cp.pushwoosh.com/).
Click on application tab and then click on add new button

![](http://www.theappguruz.com/app/uploads/2015/06/new-test-apps.png)

- After adding the app click on configure tab and then click on iOS configure button.

![](http://www.theappguruz.com/app/uploads/2015/06/send-push-test-app-585x1024.png)

- Click on iOS Configuration

![](http://www.theappguruz.com/app/uploads/2015/06/ios-not-configured.png)

## Step 3 : PushWoosh iOS App Configuration Setting

- Browse certificate file – select the APNS certificate file downloaded from apple developer portal.
- Browse p12 file – select p12 file created from keychain access.
- Private Key password – write p12 password - i.e. **12345**

## Step 4 : Unity SDK Implementation

- Import Push Notifications iOS – Unity package in your unity project
- Set Pushwoosh App id in Assets/Pushwoosh/info script.

![](http://www.theappguruz.com/app/uploads/2015/06/pushwoosh.png)

- Set bundleID in player settings
- Build project - Xcode


## Step 5 : Make Changes in Xcode

- Add **-ObjC** flag to the Linker Flags in your project.
- Set provisional profile for your project and run your project.
- Note that your device UDID should be added in apple developer portal when you run your project as push doesn’t work in sandbox mode.
- In Production mode (Live), this same procedure is followed with Production SSL Certificate instead of Development SSL Certificate.
- While configuring Pushwoosh, select gateway production instead of sandbox.

![](http://www.theappguruz.com/app/uploads/2015/06/gateway-sandbox.png)

## Step 6 : Send Push Notification

- Open https://cp.pushwoosh.com.
- Login to your account.
- Select your application.
- Enter your push message in General tab.

![](http://www.theappguruz.com/app/uploads/2015/06/send-push-start-test.png)

- Select the platform from platform settings.

![](http://www.theappguruz.com/app/uploads/2015/06/plateform-settings.png)

- Click on Woosh! button at the bottom right corner.

![](http://www.theappguruz.com/app/uploads/2015/06/send-to-soecific-geozone.png)

I hope you find this very helpful while using **Push Notification in Unity Using Pushwoosh**.
