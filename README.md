# xs-tools
tools/utils/modules for Lego Spike Prime and MINDSTORMS Robot Inventor

## app_gryo_reset
This is an application which will reset your gyro sensor. By default the HUB initialize the gyro sensor during powerup. However users will move their HUBs during powerup, causing potential miscalculations of yaw-pitch-roll (which is based on rate of changes of the HUB along the 3 axis). This application allows users to reset the gyro sensor on a steady surface. It will not finish until it has detected that the HUB is resting on a steady platform. There are 3 levels of accuracy mode (low, medium, high). The higher the level, the more time it will take the HUB is reset the gyro.

## app_test_menu
This is an application which showcase how to use xs-tool's menu module. See the code for details.


## Things to do
- Provide documentation of the API
