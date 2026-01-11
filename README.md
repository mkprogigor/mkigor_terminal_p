# mkigor_terminal_p
Debug display termanal.<br>
Data from Serial (usb-serial port conerter or usb jtag port), UART (Serial0), I2C (addr 0x39) translate to display terminal (st7789v 240x320 px, 20x20 symbols)<br>
Terminal accept sybols with code from 0x20 to 0x7F. Buffer has 1000 sybbols, after lost by FIFO.<br>
Symbols 0x0D, 0x0D + 0x0A are interpreter like new line.<br>
Chip TXS0108E bi-directional, level-shifting, voltage translator, that do possible digital voltage level matching from 1.8 to 5.0 volt. There are 2 power suply: one for mcu esp32-c3 (it takes from USB-C) and second from "listerning" side.<br>
<br>
[![Watch the video](https://img.youtu.com/vi/E8EHJTB_pYE/0.jpg)](https://youtu.be/E8EHJTB_pYE) <BR>
<br>
https://img.youtube.com/vi/HN013gZs_Y4/0.jpg
