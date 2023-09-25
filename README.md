# HistoPro® 650 H Tissue Embedding Center Cold Unit

## 1.  **About :-**

The HistoPro 650 Tissue Embedding Center (The Embedding Center) is a modular system to be used for embedding processed tissue in paraffin to prepare the tissue blocks for sectioning. There are one modules in HistoPro® 650 Embedding System. 1.HistoPro 650 CS (the Cold Module) is the Cold Module of the system that contains the cold plate.

## 2.  **Development environment :-**
A.  Set up an editor :-

Android Studio offers a complete, integrated IDE experience for Flutter.

-   [Android Studio](https://developer.android.com/studio), version 2020.3.1 (Arctic Fox) or later (<https://developer.android.com/studio>)
1.  Install Flutter:-
-   Open plugin preferences (File \> Settings \> Plugins).
-   Select Marketplace, select the Flutter plugin and click Install.
2.  Download Dart and Flutter:-
-   Download the following installation bundle to get the latest stable release of the Flutter SDK (<https://storage.googleapis.com/flutter_infra_release/releases/stable/windows/flutter_windows_3.10.5-stable.zip>)
-   Extract the zip file and place the contained flutter in the desired installation location for the Flutter SDK (for example, C:\\src\\flutter).
-   Download the following installation bundle to get the latest stable release of the Dart SDK (<https://storage.googleapis.com/dart-archive/channels/stable/release/3.0.5/sdk/dartsdk-windows-x64-release.zip>)
-   Extract the zip file and place the contained dart in the desired installation location for the Dart SDK (for example, C:\\src\\dart).
3.  Path Setup:
-   Path setup for Dart:
~~~
-   Android Studio-> File->Settings-> Plugins->Language& Frameworks->Flutter
~~~
-   Path setup for Dart:
~~~
-   Android Studio->File->Settings->Plugins->Language & Frameworks->Dart
~~~
4.  Check flutter installation:
~~~
-   Android Studio->Tools->Flutter->Flutter Doctor
~~~
5.  Deploy Source Code:
~~~
-   Android Studio-> File->Open->Select Directory
~~~
6.  Install external packages for project:
~~~
-   Android Studio-> Tools->Flutter->Flutter Pub Get
~~~
7.  Install apk on proculus:
-   Provide sufficient power to Poculus to power on i.e. Required 06 to 24 voltage. The power supply of 12v (recommended).
-   Connect the Proculus to your computer via Micro USB (USB DEBUG1. USB HOST3).
-   Remember when using Micro USB for project download, you must provide a power supply to the LCM.
-   Android LCM will recognize automatically when USB connects to the DEBUG interface.
-   Click on Android Studio \> Run \> Run
-   It will automatically install apk on proculus
## 3.  **Project Structure and Files:**
![Project](/img/project.png)
    
    -   assets folder :- This folder contain all images and logos
![Assets](/img/cold_asset.png)

    -   fonts folder :- This folder contain project fonts
![Fonts](/img/font.png)

    -   lib folder: Main project source code folder
![Lib](/img/lib.png)

    -   main.dart -\> Startting class of project that have splash screen widget with 4 sec timer for screen. Connection for uart and start timer of getting temperatures.
~~~
-   screen folder-\> This folder include all pages of app and ui.
~~~
![Screen](/img/cold_screen.png)

    -   about.dart -\> Frame-65, App about screen to show info of app.
    -   brightness.dart -\> Frame-45, User can change LED brightness here. After user change data send to uart and also save in shared preferances.
    -   configuration.dart-\> Frame-33, Configuration page is used for show users set temperature setpoints.
    -   configuration_auto_start.dart -\>Frame-35, Configuration page is used for show users set autostart time.
    -   configuration_offset.dart-\> Frame-57, Configuration page is used for show users set temperature offsets.
    -   editstarttime.dart -\> Frame-44, Edit page for edit start time of both hot and cold module.
    -   errors.dart -\> Frame-73, Errors and warning description page.
    -   legend.dart -\> Frame – 64, This page have info about both hot and cold module parts.
    -   runmode.dart -\> Frame-32, Show live temperature and LED brightness.
    -   temp_offset.dart-\> Frame-56, Edit temperature offset screen
    -   temp_set_point.dart-\>Frame-39, Edit temperature setpoint.
~~~    
-   utils folder-\> app utility folder
~~~
![Utils](/img/utils.png)
~~~
-   alarm.dart-\> Alarm and timer for app
-   color.dart -\> App color constant file
-   constant.dart-\>App static constant file
-   converter.dart-\> Data converter file
-   msg.dart-\> User toast msg file
-   string.dart-\>App static string constant file
-   uart.dart-\> Uart connection, data send and receive
-   uart.api-\> Uart api
~~~
~~~
-   widgets folder:- App ui folder
~~~
![Widget](/img/widgets.png)
~~~
-   background_img_stack.dart-\> Background device module images
-   bk_start_time.dart-\> Widget of Background start time button
-   bk_temp_edit.dart-\> Widged of background temperature edit buttin
-   btn_keyboard-\> Widget of keyboard button
-   btn_setting-\> Widget of setting button
-   btn_settings_menu-\> Widget of setting button menu
-   container_icon.dart-\> Rounded circle outer icons
-   dash.dart-\> Widget of dash line
-   navbar_menue.dart-\> widget of navbar menu
-   navbar_title.dart-\> Widget of navbar title
~~~
## 4.  **External Library :**

| **Package**          | **Recommended Version** | **Descrirption**                                                                                                                                                                         |
|----------------------|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| cupertino_icons      | 1.0.2                   | This is an asset repo containing the default set of icon assets used by Flutter's [Cupertino widgets](https://github.com/flutter/flutter/tree/master/packages/flutter/lib/src/cupertino) |
| flutter_switch       | 0.3.2                   | A custom switch widget that can have a custom height and width, borders, border radius, colors, toggle size, custom text and icons inside the toggle                                     |
| fluttertoast         | 8.2.1                   | Toast Library for Flutter, Easily create toast messages in single line of code                                                                                                           |
| number_system        | 0.0.6+8                 | A package to extend the functionality to convert between number systems                                                                                                                  |
| event_listener       | 0.2.0                   | A dart package implements NodeJS style event listening functionality                                                                                                                     |
| cron                 | 0.5.1                   | A time-based job scheduler similar to cron. Run tasks periodically at fixed times or intervals.                                                                                          |
| sprintf              | 7.0.0                   | Dart implementation of sprintf. Provides simple printf like formatting such as sprintf("hello %s", ["world"]);                                                                           |
| intl                 | 0.18.1                  | Contains code to deal with internationalized/localized messages, date and number formatting and parsing, bi-directional text, and other internationalization issues.                     |
| flutter_svg          | 2.0.5                   | An SVG rendering and widget library for Flutter, which allows painting and displaying Scalable Vector Graphics 1.1 files.                                                                |
| serial_communication | 0.0.2                   | An Android Plugin for Serial Communication which allows you to read and write the data through the available ports                                                                       |

## 5.  **Screen Flow Chart :**
![Flow](/img/flow.png)

## 6.  **App Flow Chart :**
![App Flow](/img/app_flow.png)
