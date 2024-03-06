=================
Setup Android App
=================

#. Download the Mr. Fixter purchased package from Codecanyon. Open the source code (project folder/ service folder) in your preferred Code Editor by simply Drag & Drop the folder in editor.
#. You must be ready with your unique App label , Andoid App package name.
#. Replace the default package name "com.example.service" with your android package name inside the following files:

    * android/app/src/main/kotlin/com/example/service”/MainActivity.kt
    * android/app/src/main/res/values/strings.xml
    * android/app/src/main/AndroidManifest.xml
    * android/app/src/profile/AndroidManifest.xml
    * android/app/src/debug/AndroidManifest.xml
    * android/app/build.gradle
#. Replace App label name "Service App" with your “App Label name” in the following path:
    * android/app/src/main/AndroidManifest.xml

    .. image:: /_static/images/app_label.png
    
    ``android:label="Service App"``

App Configuration
=================

App Colors
----------

To change app default color you need to change them inside the folder: ``lib/const/all_colors.dart``

.. image:: /_static/images/colors.png


Text Customization
------------------

If you want to customize the text string then you need to change them inside the folder: ``lib/const/all_texts.dart``


Text Style Customization
------------------------

If you want to customize the text style then you need to change them inside the folder: ``lib/const/all_styles.dart``


Set App Version Number (Android)
--------------------------------

1. Set android app version number inside : ``android/local.properties`` & further increment both version Name & Version code before every release build

    ``flutter.versionName=1.0.0``

    ``flutter.versionCode=1``

2. Set android app version number inside : pubspec.yaml & further increment both version Name & Version code before every release build

    ``version: 1.0.0+1``

Set Release keystore.jks Properties
-----------------------------------

#. Click here to generate a upload keystore, rename it to ``keystore.jks`` file and place it in the path: ``android/app/keystore.jks``.

#. Set the key properties in : ``android/key.properties``

*And congratulations, You have succeeded on setuping your Service App Android Side. Now go publish your version publicly.*