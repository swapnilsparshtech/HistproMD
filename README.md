# ADMIN CONFIGURATION APP
## 1.	Introduction
This document provides an overview of the architecture for the Rushabh Instruments administrator app configurator app. This is application intends to change the details and look and feel of our main HISTPRO Application.  This document outlines the key components, design decisions, and architectural styles used to develop the application.

## 2.	Architectural Overview
"Admin Config App" is an installable and can run over web, which enables the administrator of Rushabh Instruments to configure look and feel and sort of whitelisting the developed HOSTPRO App for users. This allows user to select the theme colors for look and feel, and allows to set predefined company support information for branding.

## 3.	Architectural Design Decisions
Electron js – As we need to have this installable on client system, as this is not for distribution but for restrictive usage, so we intentionally used electron js for it.
Html/Css – Simple html and css coding language is use to give better look and feel of the application. 
Node.js – To run some functions and give compatibility for electron js we used npm package structure with node. 

## 4.	Architectural Views
### A.	Company Configuration View
Under Company configuration, we allow user to configure the company details. Here we capture basic company details which are exported in an json file. 
### B.	Theme Configuration View
Under theme configuration, we allow user to configure theme colors to be used to show buttons and texts. This exports Json which changes look and feel of the main HISTPRO application.

## 5.	Folder Structure
A standard npm folder structure is maintained. Some dedicated folders are kept to give flexibility to developer for future enhancements.
Assets > This is common folder to keep css and javascript code which is to be used in application
Bootstrap > This library is added to make our screens responsive and user friendly. As it gives more functionalities for screen size wise developments.
Company_config > Code related to company config module is maintained.
Theme_config > Code related to theme configuration is maintained.
Package.json > This is main npm file to maintain all used dependencies for npm package.  
## 6.	Technology Stack
- Frontend: HTML5, CSS3,JSON.
- Backend: Node.js.
- Packaging: electron.js.

## 7.	App Structure
Company Configuration File description
As per our configuration app we create 2 configuration json files.
A.	Theme configuration
B.	Company configuration
These files are utilized to customize our main app as administrator. This way we can change the look and feel of our main app as per client requirement through Admin.
### A.	Theme Configuration
JSON file created through admin application built. 
#### a.	User Inputs
Admin can change the theme for the deployed application using configuration app. 

Primary color – This is primary color of all buttons and texts. 
Primary color icon & Text – This is icon and text color which can be white or black.
Secondary Color – Secondary color is sub ordinate information is displayed on our app. Color is defined with this color.
Secondary color icon & Text – This is icon and text color which can be white or black.
Lighter color for Cells and input fields- This is lighter color to be displaced in input fields.
#### b.	JSON Structure
Created JSON file structure is as follows.
  
primary_color : This color is primary color of icons and text.
primary_color_icon_text : Icon and Text color of primary fields.
secondary_color: Secondary color of icons and texts.
secondary_color_icon_text : Secondary color of icon and text.
Lighter_color: Lighter color of input fields.

#### c.	Deployment Path
In order to change the original HISPRO app with this newly created theme, this file has to be pasted in following folder path

~~~
ANDROID: Internal Storage\Rushabh Instruments\theme_config.json
~~~

~~~
WINDOWS: Documents\Rushabh Instruments\ theme_config.json
~~~
 
### d.	Theme config sample JSON
~~~
{
  "primary_color": "#115DDE",
  "primary_color_icon_text": "#ffffff",
  "secondary_color": "#E8FF00",
  "secondary_color_icon_text": "#26335b",
  "lighter_color": "#ff0000"
} 
~~~
### B.	Company Configuration
Admin can change the company configuration for the deployed application using configuration app. 
#### a.	User Inputs
Company configuration app will create a JSON consisting of below details.
Contact Information:
 
Address – Address to be displayed in App.
Phone – Contact Phone
Email – Email address
Website – Website of the contact company.
Logo Information
 

Company Logo – Logo of the company to be displayed.
Transparent Logo – Transparent logo to show at background. (On/Off)
On checking ON for transparent logo for background, user can upload the transparent logo 
Transparent Logo style – This is style to place the background logo.

 

#### b.	JSON Structure
Created JSON file structure for company theme is as follows.
  
contact_info : This is parent data holder which holds contact information object. 
	address: Address to be displaced.
	phone : phone to be displaced
	email: Email to contact
	website: website to show under contact.
logo : This parent head holds logo information
	company_logo : Base64 converted string of uploaded logo is saved,
	transparent_logo : true or false based on user action for it
	transparent_logo_for_background : Base 64 converted transparent logo
	transparent_logo_style: Logo style to be displayed on device.


#### c.	Deployment Path
In order to change the original HISPRO app with this newly created theme, this file has to be pasted in following folder path
~~~
ANDROID: Internal Storage\Rushabh Instruments\company_config.json
~~~
~~~
WINDOWS: Documents\Rushabh Instruments\ company_config.json
 ~~~

#### d.	Company confirguration sample JSON
 


