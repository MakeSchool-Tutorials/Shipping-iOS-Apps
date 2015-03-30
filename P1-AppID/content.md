---
title: "Creating an App ID"
slug: app-id
--- 

In this step we will set up a couple of things up in the Apple Developer portal. These steps are required to build an application that can be uploaded to the Apple App Store.

#Find the Bundle Identifier of your App

To submit your App to the AppStore you will need to know the bundle identifier. The bundle identifier is a unique string for your app. You can find the current bundle identifier of your App in Xcode by selecting:

![image](https://s3.amazonaws.com/mgwu-misc/DistributionInstructions/1_BundleIdentifier.png)

Typically bundle identifiers contain the domain name of your personal or company website and the name of your app (that ensures that the bundle id is unique). If you don't have a registered domain you can also use your full name. E.g. *com.benjaminencz.flappybird*. In case your bundle identifier is already taken Apples Web Portal will let you know about it in the next step.

If you happen to change the bundle identifier you should delete your app from devices and simulators before re-installing it, otherwise Xcode might have difficulties installing and launching your app.

Once you have chosen a bundle identifier you can move on.

#Create an App ID 
Now it's time to go to the [Apple Developer Portal](https://developer.apple.com/membercenter/index.action) and log in with your Developer Account. In this step will create an *App ID*. Every app that gets submitted to the App Store needs its own *App ID*. 

On the welcome page of the portal you need to select "Certificates, Identifiers & Profiles". Next, you need to select Identifiers:

![image](https://s3.amazonaws.com/mgwu-misc/DistributionInstructions/Identifiers.png) 

Then select the Add Button in the top right corner:

![image](https://s3.amazonaws.com/mgwu-misc/DistributionInstructions/Add_AppID.png)

You should fill out the next screen as follows:  

- App ID Description: The name of your app, e.g. "Flappy Bird"
- App ID Suffix: Select "Explicit App ID" and type in the *Bundle Identifier* of your application.

Hit *Submit* and confirm the Settings on the next Screen. Now your App ID is created.

#Create a Certificate

If you haven't released any Apps with your account yet you will need to create a new *Certificate*. This certificate will be used to create a *Provisioning Profile* and that will finally be used to generate an App archive that can be uploaded to the App Store. If you don't have a certificate yet, create one by selecting *Certificates -> All* in the left panel and hitting the *+* button in the top right: 
![image](https://s3.amazonaws.com/mgwu-misc/DistributionInstructions/Cert.png)

On the next page you need to select *App Store and Ad Hoc*:
![image](https://s3.amazonaws.com/mgwu-misc/DistributionInstructions/AppStoreCertificate.png)

Hit *Continue*.

**Follow the instructions on the screen** to create CSR file. After you created the CSR file go on to the next screen.

On the next screen upload the CSR file you created. Then hit *Generate*.

On the next page download the generated certificate and add it to you keychain by double-clicking on the downloaded file.

The certificate you have just created can be used to generate as many provisioning profiles as you want.

#Create a Provisioning Profile  

Next, you need to create a Provisioning Profile. A Provisioning Profile is unique per App that you upload to the App Store, just as the App ID that we created in the first step.
Select *Provisioning Profiles* -> *Distribution* and hit the *+* Button:

![image](https://s3.amazonaws.com/mgwu-misc/DistributionInstructions/Provisioning_Profile.png)

On the next Screen, choose **App Store** and hit *Continue*.

On the next Screen select the App ID you created earlier from the drop-down (in most cases it is pre-selected). Then hit *Continue*:

![image](https://s3.amazonaws.com/mgwu-misc/DistributionInstructions/4_ProvisioningProfile.png)

On the next Screen select the Certificate you created earlier. Then hit *Continue*.

On the next Screen you need to choose a *Profile Name*. It should be *[App Name] + App Store*, e.g. "Flappy Bird App Store". Hit *Generate*:

![image](https://s3.amazonaws.com/mgwu-misc/DistributionInstructions/5_ProvisioningProfile2.png)

On the next Screen select *Download* to download the newly generated Provisioning Profile.

After the download completes, **double-click the Provisioning Profile so that it is added to Xcode**:

![image](https://s3.amazonaws.com/mgwu-misc/DistributionInstructions/6_ProvisioningProfile3.png)