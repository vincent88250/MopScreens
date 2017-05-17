# MopScreens
Large event results display for MeOS

## Description
MopScreens is a set of php files to be used on a web server (mainly a local one) to display large event results in real time in an O'Ringen like style.
It uses MeOS Online Protocol for data updating, and reuse part of the Mop example provided with MeOS.

Currently it can handle 12 screens, but can be extended to more screens very easily. Main limitation concerns relay : currently the team is limited to 3 members and to 3 radio controls per leg.
The limitation in team size will be increased to 10 members before June 2016.

To get a better idea of what it looks like, have a look to the english documentation MeOSScreensEn.pdf

It is provided "as is" as open source code and can be freely used, modified, enhenced and distributed. It is licensed in the same conditions as MeOS.

## What's new ?

### 2017-05-17 Quote bug fixed
[x] Fix bug dealing with quotes in names (mainly in class names and team names).

[x] Fix start list time table timezone issue

[x] Fix start list number of fixed lines

[x] Changes in Readme organisation and merge bugfix branch into master

### 2017-03-15 Version planned to be used for Nationale Sud Est orienteering race on 2017 march the 18th
[x] Fix bugs introduced in original results display show.php (still used for public WiFi diffusion of results on the arena)

[x] Fix undefined variables in different php files avoiding Apache error/warning generation in Apache error log file. The error file could grow as large as many hundreds of mega bytes due to warning generation during races ! That slow seriousely the server down for large events.

[x] Separate log files from picture file in file management lists

[x] Some other cosmetic changes in code.


### 2016-11-07 Version planned to be used for PACA night orienteering on November the 19th
[x] Better support of 1, 2, 3 and 4 panels modes

[x] Up to 15 radio controls supported (in 1 panel mode individual race)

[x] Better suport for homemade radio system (based on LoRa technology) with real time radio quality and battery level display superimposed on map. Ask for details.


### 2016-05-04 Version used for French Clubs Championship
[x] Rows height have been decreased in order to stack more lines on the screen

[x] Support for slideshow

[x] Support for micro blogging (not connected to standard blogging software)

[x] Support for a summary of the competition allowing winners of all classes to be displayed on the same screen (updated in real time)

[x] Suport for homemade radio system (based on LoRa technology) with real time radio quality and battery level display superimposed on map. Ask for details.

[x] Allows CSS selection on a screen by screen basis to match caracteristics of screens (ex adapt rows height)

[x] Partial support of GECO software.

### 2016-04-04 Relay extended to 10
NOTE : Database tables structure have been altered. If you are updating an existing version, please ask for support.

[X] Relay extended up to 10 team members

[X] Screens can now be divided in two, three or four panels for non relay competitions

[X] MP, DNF etc... translation

[x] Support for experimental radio transmitted punches improved. Ask for details if interested.

### 2016-03-25 Fixes
[x] Empty panels refresh issue fixed

[x] Radio control is no more mandatory for relays

[x] Rows height has be decreased in order to stack more lines on the screen

[x] Team members names added above radio times on relays

[x] No wrap on team name

[x] Added support for experimental radio transmitted punches. Ask for details if interested.

[x] Documentation can be accessed right from the interface

### 2016-01-09 Warning fix and simultaneous support of both original MeOS display and new "MopScreens" display
[x] Fixes a warning issue in formatResult() function in functions.php

[x] It's now possible to simultaneousely use show.php (original MeOS result online display) and pages.php ("Screen" O'Ringen like one).

### 2015-11-08 Picture files management and internationalisation
[x] It's now possible from screenconfig.php to upload pictures and html files to their respective directories and to manage them.

[x] Fixed an issue relative to picture and html file allowing configuration even if these files do not exist on the PC used for configuration.

[x] Added French and Swedish support. Language can be chosen from screenconfig.php. Default language is determined based on browser configuration. Thanks to Jens Kastensson for the Swedish translation.

### 2015-11-04 Source code cleaning and small fixes and improvements
[x] Icons for configuration rename and edit have been changed to remove any possible confusion

[x] It is now possible to define the fisrt line of a screen or panel (for instance to keep the content of a panel fixed while on another panel the remaining of the class is scrolling)

[x] When scrolling, stops now after 3 empty lines

[x] It is now possible to select classes in full screen mode right from the summary table of screen.php clicking on the podium icon

### 2015-09-13 Version used by CSP Orienteering club
[x] Includes a temporary fix of the lost of class allocation on MeOS service restart.

## Known bugs
[ ] Relay results can only be displayed in the first panel. Please prefer using single panel mode for relay results.

[ ] Multistages competition are not correctly handled (no cumulative time)

[ ] Documentation is no more up to date, but still help.

[Fixed] If pressing classes edit button while editing a screen configuration, all changes already made in the form fields are lost. Workaround : use podium icon in screen.php

[Fixed] Relay display order may be incorrect if a runner lost time after radio control until he completes the course (he can appears ahead of already arrived competitors in the list).

[Fixed] When screens' panels are empty, they are not correctly refreshed. Workaround : edit the screen in screenconfig.php and press ok.

[Fixed] In relay mode it is mandatory to have at least one radio control

[Fixed] If pressing classes edit button while editing a screen configuration, all changes altready made in the form fields are lost. Workaround : use podium icon in screen.php

## Missing Features
[ ] Add multilines scrolling. Well not sure it is really useful...

[ ] Allow course based instead of class based display (may require some changes in MeOS)

[ ] Display first available competition ID (to be entered in MeOS Services/Online results)

[Done] Relay must be extended up to 10 team members (work in progress)

[Done] Screens should be dividable in three and four panels (work in progress)

[Done] Add MP, DNF etc... translation (work in progress)



