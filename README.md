# Basic OLED CNC I/O Module
This is a small OLED display build into a CNC I/O module. It is designed to be used with the 6 Pack Universal CNC I/O Controller and Grbl_ESP32 firmware. The size is 0.96" diagonal and the resolution is 128 x 64 pixels. The is no input such as a touch screen, buttons or encoder. The display is for basic status only. The display can be rotated 180 degrees to change the view orientation.

The current set of information is rather simple, but it is easy to change. The code is implemented through the custom user code capabilities of Grbl_ESP32. This is an easy way to do custom modifications without touching the core Grbl_ESP32 code. You need basic C++ programming skills.  We have a Discord server channel to discuss and share code.

With the basic firmware, the screen displays 4 different screens depending on the mode of operation:

- Startup: Shows the machine name.
- Alarm: This displays the mode and shows the current Wifi or Bluetooth status. This will help to establish a wireless connection.
- Idle or Run: This displays the mode and the current position of the XY and Z axes in the current work coordinate system
- SD File running: This shows the name of the file and a progress bar.

It uses the SSD1306Wire library and any display compatible with that can probably be used.  The display is widely available (Amazon, eBay, AliExpress) and available in a few colors.