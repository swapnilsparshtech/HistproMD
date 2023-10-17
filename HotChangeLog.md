# Changelog

## [v1.5.0](2023-08-8)

**New design:**
- Dynamic logo get from config json file
- Loading screen before getting data from Uart
- Add date time in runmode screen
- All theme colour are dynamic
- Add days in autostart to start mode in specific days
- Show system date and time in autostart
- Add days for user will be select autostart for specific days
- Add Service and manufacture contact info
- Add software and hardware version info
- Add acknowledgments screen for details of hardware and software
- Add acknowledgments details screen
- Add separate error description for hot and cold module
- Add separate screen for standby mode
- Show warnings for disconnect hardware
- Show autostart days and time
- Show system current time
- Errors and warnings for all screen

## [v1.4.0](2023-07-10)

**New design:**
- Add days in autostart days and time.
- Add about screen
- Add autostart days and time on stand by mode
- Show system time in runmode screen


## [v1.3.0](2023-07-05)

**Fixed bugs:**
- If cold unit is not connected, show that as communication error between hot and cold unit.
- "+" and "–" signs in the square blocks are not centered for changing brightness of the LED.
- Please see the space between picture of SUN and the xx% in UI compared to Figma.
- Please check the details before sending a new revision for review.  Ensure that all spellings are correct (example “undoo” instead of “undo” on the number pad for editing temperatures.)
- While editing a number (temperature, offset, etc.) allow appropriate number of digits (e.g.2 digits) even if it is out of range (e.g. 75) and if the user enters to confirm the out of range number, display a message that the entry was out of range instead of allowing only one digit to be entered.  Currently someone enters 75 deg C, they end up with 5 deg C as a set point which is out of range anyway.
- The entire area for a given number should activate the number push instead of ONLY the printed digit.
- Look at the UI elements and Style Guide for Primary Buttons (and for that matter for everything else) and implement the changes accordingly.  For example, when user presses the button from default condition, it should change the color to clicked element color and if the processing takes longer than 3 seconds, show the animation to indicate that the system is still processing the last button press to avoid user pressing the same button multiple times while system has not completed the response to the previous button press.
- The setting button keeps moving up and down while going back.
- The range for the offset values need to change to -5.0 to +4.9 based on our last discussion regarding communication between Proculus and Firmware.    1. New implementation.
- Pre-filtering values while editing any entry definitely creates confusion.  We think that it is better to display a message that the selection was out of range if the user presses Confirm button before getting a proper value on the screen.  Also, while accepting and displaying time (for start time) must be a proper time value – e,g, 25:50 or 00:00 are not good values.  Also a space is missing between time and AM for the cold unit start time.
- Please ensure that going back does not take back to a screen in the same mode unless it was desired.  It should take back to previous level – for example from Configuration menu, back button should go back to RUN mode directly.
- UI Elements should be sized for max number of digits. The size of the box changes when going from 9 to 10 degrees. Box size should be same regardless of quantity entered.
- Brightness box -The Layout of Certain elements needs to be improved to match the Figma There is a faint grey outline around the black outline that should not be there Application.

  
## [v1.2.0](2023-06-28)

**Cold module ui design:**
- The HistoPro 650 Tissue Embedding Center have two module 1st is hot module and 2nd is cold module. For cold module new figma designa added and we implement in flutter app.


## [v1.1.0](2023-06-10)

**Fixed bugs:**
- Please ensure colored UI Elements are designed in Flutter -> All png imgs replaced with material icon and svg files. Also I create separate widgets for
   repeat UI.
- Frame 32: Green zone +/- 3 deg C -> Added +/- 3 degree green zones for temperature with user mmsg on high and low value touch for 40 to 70 degree
- Frame 45: Instead of stating Run Mode, it should mention Adjust LED Brightness -> Title rename
- Frame 56: Display Measured temperature + offset value to allow user to match the actual temperature to displayed temperature.
   Offset range +/- 7 deg C in 0.1 deg C increment. Change Delete key to +/-. Always enter 2 digits and any additional digit makes the
   older number roll to the left and being ignored. For example entering 12 means 1.2 deg C, entering 125 means 2.5 deg C -> Set +/- 7 dec offset value
- Frame 44:  changes time in 15 minutes increments -> Fixed 15 min increment and decrement value
- Frame 73: Frame shows a phone number. It should be editable in the configuration screen.
- Frame: 65: Contact Information: It should be editable in the configuration screen.
- Frame 64: Remove the Legend expansion buttons. This will make frames for Legend expansion (frame 89-97) unnecessary for this project.
- Only Run Mode Screen with Calculated temperatures displayed as well as Offset Adjust screens will be dynamic screens displaying real time data.


## [v1.0.0](2023-05-15)
**Merged pull requests:**
- The HistoPro 650 Tissue Embedding Center (The Embedding Center) is a modular system to be used for embedding processed tissue in paraffin to prepare the tissue blocks for sectioning.
- There are one modules in HistoPro® 650 Embedding System.
- 1.HistoPro 650 CS (the Cold Module) is the Cold Module of the system that contains the cold plate.
