# mkigor_terminal_p
Debug display termanal.<br>
Serial, UART (Serial0), I2C (addr 0x39) => display terminal (st7789 240x320 px, 20x20 symbols)<br>
Terminal accept sybols with code from 0x20 to 0x7F. Buffer has 1000 sybbols, after lost by FIFO.<br>
Symbols 0x0D, 0x0D + 0x0A are interpreter like new line.<br>

<img src="images/mkigor_terminal.png" alt="Scheme" style="width:70%; height:auto;"><BR>
