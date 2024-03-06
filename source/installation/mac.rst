================================
How to Install Flutter on MacOS?
================================

Minimum System Requirements
===========================

* Operating Systems: macOS [64-bit]
* Disk Space: 700 MB
* Git for macOS
* Download Latest Flutter SDK HERE
* Extract the file in the desired location e.g.

.. code:: bash

    cd ~/development
    unzip ~/Downloads/flutter_macos_v1.5.4-hotfix.2-stable.zip
    
* Add the flutter tool to your path. To do this, open your bash profile from your terminal (might need sudo)

.. code:: bash

    sudo vim ~/.bash_profile

Add your flutter path to the $PATH variable in bash_profile.

E.g. If you extracted flutter in your Applications folder, your path will be /Applications/flutter/bin . Add this to the existing $PATH variable by using : in between two paths. Once added, save and close the bash_profile . Run terminal again and check the $PATH by running

.. code:: bash

    echo $PATH

You should see your Flutter path added to the $PATH

Flutter
=======

Run flutter precache in the terminal.

Run flutter doctor
------------------

Run the following command to see if there are any dependencies you need to install to complete the setup (for verbose output, add the -v flag):

.. code:: bash

    flutter doctor

*This command checks your environment and displays a report to the terminal window. The Dart SDK is bundled with Flutter; it is not necessary to install Dart separately. Check the output carefully for other software you may need to install or further tasks to perform (shown in bold text). For example: If you haven’t used Flutter before, you might see an output like this by running flutter doctor*

.. code:: bash

    [✓] Flutter (Channel stable, 3.7.8, on macOS 13.2.1 22D68 darwin-arm64, locale en-IN)
    [✓] Android toolchain - develop for Android devices (Android SDK version 33.0.2)
    [✓] Xcode - develop for iOS and macOS (Xcode 14.2)
    [✓] Chrome - develop for the web
    [✓] Android Studio (version 2022.1)
    [✓] VS Code (version 1.78.2)
    [✓] Connected device (2 available)
    [✓] HTTP Host Availability

You can see there are several things to be done to begin using Flutter in this Mac. To correct these issues, let’s run following commands

Fix license issue in Android studio
-----------------------------------

.. code:: bash


    $ brew update
    $ brew install --HEAD usbmuxd
    $ brew link usbmuxd
    $ brew install --HEAD libimobiledevice
    $ brew install ideviceinstaller

Update iOS-deploy
-----------------

.. code:: bash

    npm install -g ios-deploy


iOS Setup
---------

**Install Xcode**

To develop Flutter apps for iOS, you need a Mac with Xcode 9.0 or newer:

* Install Xcode 9.0 or newer (via web download or the Mac App Store).
* Configure the Xcode command-line tools to use the newly-installed version of Xcode by running the following from the command line:

    .. code:: bash

        sudo xcode-select --switch /Applications/Xcode.app/Contents/Developer

* This is the correct path for most cases, when you want to use the latest version of Xcode. If you need to use a * different version, specify that path instead.
* Make sure the Xcode license agreement is signed by either opening Xcode once and confirming or running sudo xcodebuild -license from the command line.

.. image:: /_static/images/flutter_plugins.png

With Xcode, you’ll be able to run Flutter apps on an iOS device or on the simulator.

Set up the iOS simulator
------------------------

To prepare to run and test your Flutter app on the iOS simulator, follow these steps:

* On your Mac, find the Simulator via Spotlight or by using the following command:

    .. code:: bash

        open -a Simulator

* Make sure your simulator is using a 64-bit device (iPhone 5s or later) by checking the settings in the simulator’s Hardware > Device menu.
* Depending on your development machine’s screen size, simulated high-screen-density iOS devices may overflow your screen. Set the device scale under the Window > Scale menu in the simulator.