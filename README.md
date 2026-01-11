# mkigor_terminal_p
Debug serial display terminal (dsdt).<br>
ESP32-C3 translates Data from Serial0  (usb-serial port conerter or usb jtag port), or UART (Serial0), or I2C (addr 0x39)<br>
to display terminal (2" color TFT SPI display st7789v 240x320 px, 20x20 symbols).<br>
Terminal accept sybols with code from 0x20 to 0x7F. Buffer has 1000 sybbols, after lost by FIFO.<br>
Symbols 0x0D, 0x0D + 0x0A are interpreter like new line.<br>
Chip TXS0108E bi-directional, level-shifting, voltage translator, that do possible digital voltage level matching from 1.8 to 5.0 volt.<br>
There are 2 power suply: one for mcu esp32-c3 (it takes from USB-C) and second from "listerning" side.<br>
<br>
[![Watch the video](https://img.youtube.com/vi/E8EHJTB_pYE/0.jpg)](https://youtu.be/E8EHJTB_pYE) <BR>
<br>
