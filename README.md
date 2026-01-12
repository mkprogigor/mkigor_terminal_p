# mkigor_terminal_p
Debug serial display terminal (dsdt).<br>
MCU ESP32-C3 send rext data 
from 
  UART or I2C (addr 0x39) or UDP port or Serial0 (usb-serial),
to
  display terminal (2" color TFT SPI display st7789v 240x320 (GMT020-02).<br>
Terminal accept sybols with code from 0x20 to 0x7F. Buffer has 1000 sybbols, after lost by FIFO.<br>
Symbols 0x0D, 0x0D + 0x0A are interpreter like new line.<br>
<br>
Thanks to Texas Instruments chip TXS0108E we have Bi-Directional, Level-Shifting, 
Voltage Translator from 1.65 to 5.5V. Really it works up to 3 Mbit/s on UART connector. 
That is adjustment MCU GPIO with 1,8V, 3.3V, 5V level peripheral IO. 
It's possible drive gate of low-voltage high-current MOSFET (not fast and not high power).
The chip TXS0108E doesn't have galvanic isolation, but makes a little protection to MCU GPIO.
There are 2 power suply: one for mcu esp32-c3 (it comes from USB-C) and second from I2C or UART side.<br>
<br>
Thanks to very useful library Bodmer/TFT_eSPI on GitHub we've got MCU with 
economic 2 inch TFT Module 240×320 ST7789V GMT020-02. And it's remaines 8 GPIO, UART, I2C. 
That's enough and suitable to many startup DIY project.<br>

<br>
[![Watch the video](https://img.youtube.com/vi/E8EHJTB_pYE/0.jpg)](https://youtu.be/E8EHJTB_pYE) <BR>
<br>
