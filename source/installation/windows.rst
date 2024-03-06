==================================
How to Install Flutter on Windows?
==================================

Minimum System Requirements
---------------------------

*   Operating Systems: Windows 7 or later [64-bit]
*   Disk Space: 400 MB
*   Git for Windows
*   Flutter SDK 3.0.0-stable

Get the Flutter SDK
-------------------

* Download Latest Flutter SDK HERE
* Unzip the downloaded zip in C:\flutter .
* Locate flutter_console.bat inside the flutter directory and start it by double-clicking.

Update your path
----------------

If you wish to run Flutter commands in the regular Windows console, take these steps to add Flutter to the PATHenvironment variable:

* From the Start search bar, type ‘env’ and select Edit environment variables for your account
* Under User variables check if there is an entry called Path:
* If the entry does exist, append the full path to flutter\bin using ; as a separator from existing values.
* If the entry does not exist, create a new user variable named Path with the full path to flutter\bin as its value.

.. note::
    You have to close and reopen any existing console windows for these changes to take effect.

Run flutter doctor
------------------

From a console window which has the Flutter directory in the path (see above), run the following command to see if there are any platform dependencies you need to complete the setup:

``C:\flutter>flutter doctor``

This command checks your environment and displays a report of the status of your Flutter installation. Check the output carefully for other software you may need to install or further tasks to perform (shown in bold text).

**For example:**

.. code:: bash
    
    [-] Android toolchain - develop for Android devices
    • Android SDK at C:\\Android\\sdk
    ✗ Android SDK is missing command line tools; download from https://goo.gl/XxQghQ
    • Try re-installing or updating your Android SDK,visit https://flutter.dev/setup/#android-setup for detailed instructions.

Android Setup
-------------

.. note::
    Flutter relies on a full installation of Android Studio to supply its Android platform dependencies. However, you can write your Flutter apps in a number of editors.


**Install Android Studio**

* Download and install Android Studio.
* Start Android Studio, and go through the ‘Android Studio Setup Wizard’. This installs the latest Android SDK, Android SDK Platform-Tools, and Android SDK Build-Tools, which are required by Flutter when developing for Android.

**Set up your Android device**

To prepare to run and test your Flutter app on an Android device, you’ll need an Android device running Android 5.0 (API level 21) or higher.

* Enable Developer options and USB debugging on your device. Detailed instructions are available in the Android documentation.
* Windows-only: Install the Google USB Driver
* Using a USB cable, plug your phone into your computer. If prompted on your device, authorize your computer to access your device.
* In the terminal, run the flutter devices command to verify that Flutter recognizes your connected Android device.

By default, Flutter uses the version of the Android SDK where your adb tool is based. If you want Flutter to use a different installation of the Android SDK, you must set the ANDROID_HOME environment variable to that installation directory.

**Install the Flutter and Dart plugins**

* Start Android Studio.
* Open plugin preferences (File > Settings > Plugins).
* Select Browse repositories, select the Flutter plugin and click Install.
* Click Yes when prompted to install the Dart plugin.
* Click Restart when prompted.