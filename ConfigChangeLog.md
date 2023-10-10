# Changelog

## [1.1.0](2023-10-09)

**Fixed bugs:**

- When window is resized too small, elements reflow. The application can be a fixed sized application that is not responsive User will then resize window to see all the required content.
- Please note that number pad should be disabled until user clicks a blue field. When field selected, disable the color picker and enable the number pad. If R, G, or B, or Alpha select, disable the A,B,C,D,E,F keys.
- We should add a note that Images must be SVGs. I will update the Figma.
- Factory Reset does not work (reset applications to default. "yes" in button should be "Yes".
- We would like to restrict the secondary color to a percentage lightness of the primary color as shown in the screen below. Currently, you can select any color and the entry is no different compared to other colors.
- Based on our customer's recent feedback, compared to the Figma we provided to you, we also need to provision for one more field in Contact Info, "Website Help URL". This will be displayed as QR code in our application in future.


## [v1.0.0](2023-09-05)
**Merged pull requests:**
- Under Company configuration, we allow user to configure the company details. Here we capture basic company details which are exported in an json file.
- Under theme configuration, we allow user to configure theme colors to be used to show buttons and texts. This exports Json which changes look and feel of the main HISTPRO application.
- Company Configuration File description As per our configuration app we create 2 configuration json files. A. Theme configuration B. Company configuration These files are utilized to customize our main app as administrator. This way we can change the look and feel of our main app as per client requirement through Admin.
- 
