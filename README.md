# mkigor_terminal_p
Debug serial display terminal (dsdt).<br>
ESP32-C3 translates Data from Serial0  (usb-serial port conerter or usb jtag port), or UART (Serial0), or I2C (addr 0x39)<br>
to display terminal (2" color TFT SPI display st7789v 240x320 px, 20x20 symbols).<br>
Terminal accept sybols with code from 0x20 to 0x7F. Buffer has 1000 sybbols, after lost by FIFO.<br>
Symbols 0x0D, 0x0D + 0x0A are interpreter like new line.<br>

1) Possible directions:<br>
UART => dsdt (+ usb2uart0);<br>
I2C => dsdt (+ usb2uart0);<br>
UDP => dsdt (+ usb2uart0);<br>
usb2uart0 => dsdt + UART + I2C + UDP.<br>
2) Thanks to Texas Instruments chip TXS0108E we have Bi-Directional, Level-Shifting, 
Voltage Translator from 1.65 to 5.5V. Really it works up to 3 Mbit/s on UART connector. 
That is adjustment MCU GPIO with 1,8V, 3.3V, 5V level peripheral IO. 
It's possible drive gate of low-voltage high-current MOSFET (not fast and not high power).
The chip TXS0108E doesn't have galvanic isolation, but makes a little protection to MCU GPIO.
There are 2 power suply: one for mcu esp32-c3 (it takes from USB-C) and second from "listerning" side.<br>
3) Thanks to very useful library Bodmer/TFT_eSPI on GitHub we've got MCU with 
economic 2 inch TFT Module 240×320 ST7789V GMT020-02. And it's remaines 8 GPIO, UART, I2C. 
That's enough and suitable to many startup DIY project.<br>

<br>
[![Watch the video](https://img.youtube.com/vi/E8EHJTB_pYE/0.jpg)](https://youtu.be/E8EHJTB_pYE) <BR>
<br>
