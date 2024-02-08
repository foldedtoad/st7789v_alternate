# Zephyr Support for ST7789 Display

## Overview
Display "Hello World" and a dynamic counter using LVGL.  

This sample application displays "Hello World" in the center of the screen
and a counter at the bottom which increments every second. 

The **alternate** aspect of this project is it doesn't use the arduino shield schema, but rather directly configures the display device.
This was done in order to break away from the Zephyr LVGL example code configuration.

See [video](https://studio.youtube.com/video/sml6Ic_K4g4) for demostration.

## Requirements

Display shield and a board which provides a configuration
for example:

* [**ST7789**](https://www.aliexpress.us/item/3256805850192151.html) display panel.
* **PCA10056** Nordic nRF52840 Eval Board.

### Soldering
The 0.10" headers will need to be soldered onto the display pannel. In addition, wiring between the display panel and the PCA10056 board needs to be made.  
Review the **nrf52840dk_nrf52840.overlay** file for wire-to-pin specifics.

## How to Build
This project was developed using Zephyr V3.5, and successfully built on both Ubuntu and MacOS.  

**NOTE** -- building may take longer that expected as LVGL has quite a bit of code.

There are two easy methods to build the firmware.

### CMake Method
This build method use cmake directly, and doesn't use west or ninja.
1) cd to your st7789v_alternate root directory
2) run "./configure.sh"
3) cd to build directory
4) make

### West Method
1) cd to your st7789v_alternate root directory
2) rm -rf build
3) west build -b st7789v_alternate
