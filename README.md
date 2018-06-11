# Blue-EForth
EForth for the Blue Pill with STM32F103

While other Forths like MECRISP are available and have many significant features EForth is more easily stuffed in the smaller chips.
This Forth was reconfigured from Dr Ting's STM3F407 Forth. Although, his original ran with '0' based addressing, I have not found a way to cause the F103 part to move its memory to 0.
EForth runs in RAM but is loaded into FLASH. RAM is at 20000000H so be careful.
Not inerrupts are enabled but space is resurved for interrupts in the FLASH
There is no boot loader needed. EFORTH is the boot loader.
It expects there to be a serial terminal connected to PA9 and PA10. It is 56K baud, 8 bit, Even parity. This was the same as I used for downloading.
The code is in a .HEX file.
I have not tried TURNKEY yet.
Most terminal programs should work but one may need some changes to download source.
I use a program that I wrote to boot load the FLASH, keyboard interface to EFORTH and source download Forth programs. It runs in Win32Forth, an open source Forth.
