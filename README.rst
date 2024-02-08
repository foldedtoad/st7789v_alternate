

Overview
********

Display "Hello World" and a dynamic counter using LVGL.  

This sample application displays "Hello World" in the center of the screen
and a counter at the bottom which increments every second. If an input driver
is supported, such as the touch panel controller on mimxrt10{50,60,64}_evk
boards, "Hello World" is enclosed in a button that changes to the toggled state
when touched.

The **alternate** aspect of this project is it doesn't use the arduino shield schema, but rather directly configures the display device.
This was done in order to break away from the Zephyr LVGL example code configuration.

Requirements
************

Display shield and a board which provides a configuration
for example:

[**Display**] (https://www.aliexpress.us/item/3256805850192151.html) 

Building and Running
********************

Example building for `nrf52840dk_nrf52840`:




References
**********

.. target-notes::

.. _LVGL Web Page: https://lvgl.io/
.. _SDL2: https://www.libsdl.org
.. _RK043FN02H-CT: https://www.nxp.com/products/processors-and-microcontrollers/arm-based-processors-and-mcus/i.mx-applications-processors/i.mx-rt-series/4.3-lcd-panel:RK043FN02H-CT
