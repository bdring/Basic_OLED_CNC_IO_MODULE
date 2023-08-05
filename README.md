# Basic OLED CNC I/O Module

<img src="https://github.com/bdring/Basic_OLED_CNC_IO_MODULE/blob/main/images/OLED_Module_1.jpg" width="600">

This is a small OLED display build into a CNC I/O module. It is designed to be used with the [6 Pack Universal CNC I/O Controller](https://github.com/bdring/6-Pack_CNC_Controller) and [Grbl_ESP32 firmware](https://github.com/bdring/Grbl_Esp32). The size is 0.96" diagonal and the resolution is 128 x 64 pixels. The is no input such as a touch screen, buttons or encoder. The display is for basic status only. The display can be rotated 180 degrees to change the view orientation.

The current set of information is rather simple, but it is easy to change. The code is implemented through the custom user code capabilities of Grbl_ESP32. This is an easy way to do custom modifications without touching the core Grbl_ESP32 code. You need basic C++ programming skills.  We have a Discord server channel to discuss and share code.

With the basic firmware, the screen displays 4 different screens depending on the mode of operation:

- Startup: Shows the machine name.
- Alarm: This displays the mode and shows the current Wifi or Bluetooth status. This will help to establish a wireless connection.
- Idle or Run: This displays the mode and the current position of the XY and Z axes in the current work coordinate system
- SD File running: This shows the name of the file and a progress bar.

It uses the SSD1306Wire library and any display compatible with that can probably be used.  The display is widely available (Amazon, eBay, AliExpress) and available in a few colors.

The module uses the 5th and 6th I/O pins of the socket. These are gpio.14 and gpio.13 regardless of what socket is used. Socket 4 on the 6 Pack and socket 2 of the 6 Pack external driver version repeats these pins in 1st and 2nd position. You cannot use this module in another socket if you have a module in one of those sockets. Basically it is best to use the OLED in socket 4 of the 6 Pack or socket 2 of the external version. 

```yaml
i2c_oled:
  sda_pin: gpio.14
  scl_pin: gpio.13
  i2c_address: 60
  width: 128
  height: 64
```

<img src="https://github.com/bdring/Basic_OLED_CNC_IO_MODULE/blob/main/images/OLED_Module_2.jpg" width="400">
<img src="https://github.com/bdring/Basic_OLED_CNC_IO_MODULE/blob/main/images/OLED_Module_3.jpg" width="400">
<img src="https://github.com/bdring/Basic_OLED_CNC_IO_MODULE/blob/main/images/OLED_Module_4.jpg" width="400">

[<img src="https://github.com/bdring/TMC2209_4x_DK/blob/main/images/tindie-logo.png" width="160">](https://www.tindie.com/products/33366583/oled-display-cnc-io-module/)
