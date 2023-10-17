# Changelog

## [1.1.0](2023-10-09)

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


## [v1.0.0](2023-09-05)
**Merged pull requests:**
- The HistoPro 650 Tissue Embedding Center (The Embedding Center) is a modular system to be used for embedding processed tissue in paraffin to prepare the tissue blocks for sectioning.
- There are one modules in HistoPro® 650 Embedding System.
- 1.HistoPro 650 CS (the Cold Module) is the Cold Module of the system that contains the cold plate.
