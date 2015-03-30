---
title: "iTunes Connect"
slug: itunes-connect
--- 

iTunes Connect is separate portal that is only used to submit and manage Apps that you want to publish or already have published. Here you will create all the meta information for your app that will appear in the Apple App Store, that includes an app description, keywords, screenshots and more.

#Create the App in iTunes Connect

Go to [iTunes Connect](itunesconnect.apple.com) and log in with your developer account.

Select *My Apps*:
![image](https://s3.amazonaws.com/mgwu-misc/Online_Academy/itunes_myapps.png)

Then Select the *+* button in the top left corner and choose *New iOS App*.

In the popup that shows up you should enter your App Name and select the Bundle ID of your app. You will also need to choose a version number that should match the version number that you have chosen in Xcode.

![image](https://s3.amazonaws.com/mgwu-misc/DistributionInstructions/2_iTunesConnect.png)

Once the information is complete you can hit *create*.

Now add all the information iTunes Connect asks you for on the main page: Screenshots, Descriptions, an App Icon, etc.

#Set up Pricing and Availability

Additionally you will need to chose a price tier and a release date for your app. You can do that by selecting the *Pricing* tab displayed at the top of the page:

![image](https://s3.amazonaws.com/mgwu-misc/Online_Academy/itunes_pricing.png)

On the pricing page you can select an availability date for your app. If you choose the current day, the app will be released as soon as it passes the Apple review process. If you choose a date far in the future, you will be able to control the release manually after your app has been approved. If you choose a future date you will have to remember to change it after your app has been reviewed.

Additionally you need to choose a price tier for your app. You can either offer it for free or make it a paid app.

Once you have chosen these settings, hit the save button in the bottom right.

#Check completion status

When you go back to the main page of your app you will see a *Submit for Review* button in the top right corner. If you hit this button iTunes Connect will tell you which information is missing before your app can be submitted for review. If you have provided all the necessary information so far, the only missing part should be:

- *You must submit your builds using Xcode 5.1.1 or later, or Application Loader 3.0 or later. After you’ve submitted a build, select it in the Builds section below.*

In the next steps we will prepare the Xcode settings of your app for submission, then we will be able to upload a build that can be selected in iTunes Connect.

Time to move on!