# mkigor_terminal_p
Debug display termanal.<br>
Data from Serial (usb-serial port conerter or usb jtag port), UART (Serial0), I2C (addr 0x39) translate to display terminal (st7789v 240x320 px, 20x20 symbols)<br>
Terminal accept sybols with code from 0x20 to 0x7F. Buffer has 1000 sybbols, after lost by FIFO.<br>
Symbols 0x0D, 0x0D + 0x0A are interpreter like new line.<br>
Chip TXS0108E bi-Directional, Level-Shifting, Voltage Translator, that do possible digital voltage level matching from 1.8 to 5.0 volt.<br> 

<img src="images/mkigor_terminal.png" alt="Scheme" style="width:70%; height:auto;"><BR>
