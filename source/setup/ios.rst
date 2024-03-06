=============
Setup iOS App
=============

Before proceeding ahead, please make sure you have Completed setting up the Android App first, as it makes up most of the tasks required for this project.

*Open the project folder in Android Studio, In the terminal, run following command:*

.. code-block:: bash

    flutter clean
    flutter pub get
    cd ios
    pod install --repo-update

Configuration
=============

Drag & Drop the ios folder in Xcode & then perform the below steps:

#. Open Xcode, double click on runner.
#. Check if all the app name, package name, version is correct in the General Section & Make sure your bundle name is showing correct in Info section in the Xcode.
#. Go to Signing & Capabilities, select or add the team & bundle identifier.

Change Your iOS App Icon
------------------------

#. Go to https://www.appicon.co this website.
#. Select/Drag your icon file here.
#. Select platform. (iOS for this section, and iPad if you want to publish for iPad also).
#. Click generate and download the zip file.
#. Now extract this zip file and copy the AppIcon.appiconset folder inside of the AppIcon file which you extracted just now.
#. Past the AppIcon.appiconset folder inside this following directory: your_project/ios/Runner/Assets.xcassets.
#. And click replace to replace old icon with yours.


*That’s only few simple step and congratulations again. You are ready to publish your iOS version also.*