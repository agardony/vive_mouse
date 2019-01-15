# vive_mouse
Vive controller as a mouse pointer, v0.3
Software that turns a Vive controller into a mouse pointer.
Originally developed by [reddit user -olli-](https://www.reddit.com/user/-olli-)
Hosted Here: http://olli.wtf/vive/
Rehosted with permission from developer.

ORIGINAL README

Vive mouse pointer program v0.3. Author: Olli Moisio, https://www.reddit.com/user/-olli-/.

v0.2 -> v0.3 Changelog:
Added the option to adjust the pointing angle of the controller. Right now this value can only be accessed by manually editing the default.config file after configuration/calibration has been done.

v0.1 -> v0.2 Changelog:

- Support for multiple displays
- The application menu -button can be used to enable/disable the cursor

- Background: Nearly total rewrite of the program using an object-oriented style.

========================================

Dependencies:

========================================

If you get an error message about a missing file "MSVCP140.dll", you need to install the "Visual C++ Redistributable for Visual Studio 2015" from Microsoft:

https://www.microsoft.com/en-us/download/details.aspx?id=48145

If prompted select the download option: vc_redist.x86.exe.

========================================

About:

========================================

This program enables the use of an HTC Vive controller as a mouse pointing device. The display can be physically located within the trackable volume of the base stations, or even outside those limits as long there is a direct line of sight between the display and the area where the controllers are trackable.

The physical location of the display must be calibrated by using a Vive controller. This is done with the "vive_mouse_config.exe" executable. Two means of calibration are available:

1. Calibration by touch
Uses the physical location of the controller within the trackable volume to map the borders of the display. This is the recommended calibration method.

2. Calibration by pointing
A more advanced method that uses the intersection of two sets of lines to calculate the position of the display. This method allows calibration even when the display is not within base station tracking limits (for example a video projector pointing at a high ceiling).

Follow these steps alongside the configuration program to perform the calibration:
1. Select two positions within the trackable volume of the base stations that have a direct line of sight to the display. These points should be at least one meter apart.
2. From point A, use the Vive controller to point to the corners of the display. Imagine the long handle of the controller as a gunsight and try to align the system button and the application button. The program uses a virtual line formed along this axis to calculate the position of the display. The configuration program will give instructions.
3. Move to point B and repeat the procedure.

After configuration has been done, you can start the main program and use a Vive controller to control the mouse by pointing at the physical display.

========================================

Button configuration:

========================================

Trigger: primary mouse button
Grip: middle mouse button
Digital pad (middle): scroll up / down
Digital pad (left): double click with primary button
Digital pad (right): secondary mouse button
Application menu: enable / disable cursor

If a left-handed configuration is selected, the middle and right dpad buttons are reversed.

========================================

Limitations / Known issues:

========================================

- Not a direct Windows mouse driver implementation, so functionality within programs can vary.

========================================

TODO:

========================================

- Configurable buttons / Lua or LuaJIT scripting support
- Much better instructions, both graphical and textual

========================================

Misc:

========================================

In addition to the OpenVR runtime this software uses the following open source libraries:

"OpenGL Matrix Class (C++)" by Song Ho Ahn (http://www.songho.ca/opengl/gl_matrix.html)
"JsonCpp" by Baptiste Lepilleur (https://github.com/open-source-parsers/jsoncpp)

The license file for JsonCpp can be found under the "license" subdirectory.

