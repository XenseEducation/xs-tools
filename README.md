# xs-tools
XS Tools is a set of tools/utils/modules for Lego Spike Prime and MINDSTORMS Robot Inventor, aiming improve ease-of-use of the official Python modules.

## app_gryo_reset
This is an application which will reset your gyro sensor. By default the HUB initializes the gyro sensor during powerup. However frequently users will move their HUBs during powerup, causing potential miscalculations of yaw/pitch/roll (which is based on rate of changes of the HUB along the 3 axis). This application allows users to reset the gyro sensor on a steady platform. It will not finish until it has detected that the HUB is resting on a steady platform. There are 3 levels of accuracy mode (low, medium, high). The higher the level, the more time it will take the HUB to reset the gyro.

## app_test_menu
This is an application which showcase how to use xs-tool's menu module. Currently it supports using the left/right/center buttons. Left/right buttons navigate menu items, center button select/execute the menu item as well as going back to previous menu (using either double-click or long hold of center button). See the code for details.


## xs-tools
This contains all the xs-tool's modules, without any applications embedded. 

## Things to do
- Provide documentation of the API
