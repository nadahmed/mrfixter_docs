==============================
Build Android App (.apk, .aab)
==============================

Before you publish kindly make sure you have set up your own server key, website url/api url and license key or else the app will fail to Run. Run the app for 2nd time to recheck it’s working properly according the required documents you provided.

Clean the project
-----------------

Run the command in Android Studio terminal:

.. code-block:: bash

    flutter clean

Delete the following folders (if present):

1. android/.gradle
2. .dart_tool

Run Release App
---------------

Run the app in release mode using the command:

.. code-block:: bash

    flutter run --release

Build Release App (.apk)
------------------------

Build app-release.apk file using the command:

.. code-block:: bash

    flutter build apk --release

Build Android App bundle (.aab)
-------------------------------

Build app-release.aab app bundle to submit it in Google Playstore. Run the following command:

.. code-block:: bash
    
    flutter build appbundle --release


*And BOOM! your android app is ready to be submitted to the store.*