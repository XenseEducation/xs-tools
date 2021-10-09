# XS Tools
XS Tools is a set of tools/utils/modules for Lego Spike Prime and MINDSTORMS Robot Inventor, aiming improve ease-of-use of the official Python modules.

## app_s2py_switcher
This is an application which enable/disable running Python code from word blocks (s2py). 

Instructions to enable s2py
- Load and run `app_s2py_switcher.llsp` or `app_s2py_switcher.lms` (depending on whether you are running Spike App or Mindstorms App)
  - You will be presented with a menu of 2 choices:
    - Checkmark: enable running Python code in word blocks
    - Cross: disable running Python code in word blocks
  - By default after running the program, it will enable the mode. 
- You can go back to this program in your hub to enable/disable this feature anytime
- You need to run this program once everytime when your hub is powered up. If not, you will just see the Python code displayed on the hub's screen.

Using s2py
- Once you have enabled s2py, you can use the "display message" block in Spike App or Robot Inventor App and write python code
  - s2py only accept Python expression. https://www.hackerearth.com/practice/python/working-with-data/expressions/tutorial/
- You need to prefix the text with `XS:` to tell s2py that you are sending a Python expression
  - example: `XS: hub.sound.beep()` (This will make a beep sound. `hub` is imported by default, so no need to use `xs_import()` to import `hub`)
- If you don't prefix the text with `XS:` it will be treated as normal text to be displayed in the hub.
- You can comment a Python expression with prefix `#XS:`
  - example: `#XS: this line will not be evaluated`
- Other examples:
  - `XS: hub.motion.yaw_pitch_roll(yaw_correction=2.5)` (adjust yaw correction of the gyro sensor)
  - `XS: xs_import('xs.motion')` (import `xs.motion` library)
  - `XS: xs.motion.gryo_reset(100)` (execute `xs.motion.gryo_reset(100)`)
  - `XS: xs_import_from_slot(13)` (import python code from slot 13 of the hub, the code will be import to module `slot13`)
  - `XS: slot13.hello('abc')` (run function `hello()` from slot 13)

## app_gryo_reset
This is an application which will reset your gyro sensor. By default the HUB initializes the gyro sensor during powerup. However frequently users will move their HUBs during powerup, causing potential miscalculations of yaw/pitch/roll (which is based on rate of changes of the HUB along the 3 axis). This application allows users to reset the gyro sensor on a steady platform. It will not finish until it has detected that the HUB is resting on a steady platform. There are 3 levels of accuracy mode (low, medium, high). The higher the level, the more time it will take the HUB to reset the gyro.

## app_test_menu
This is an application which showcase how to use xs-tool's menu module. Currently it supports using the left/right/center buttons. Left/right buttons navigate menu items, center button select/execute the menu item as well as going back to previous menu (using either double-click or long hold of center button). See the code for details.

## app_change_slot_image
This is an application which showcase how to change slot image of the hub menu. Users can also restore the slot images.

## xs-tools
This contains all the xs-tool's modules, without any applications embedded. 

## Things to do
- Provide documentation of the API
