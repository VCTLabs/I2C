# Arduino I2C master library

A better I2C master library, originally by Wayne Truchsess.
See http://dsscircuits.com/index.php/articles/66-arduino-i2c-master-library

On most Arduino boards, SDA (data line) is on analog input pin 4, and SCL (clock line) is on analog input pin 5. On the Arduino Mega, SDA is digital pin 20 and SCL is 21.  (source: http://arduino.cc/it/Reference/Wire)

           Arduino Wire (I2C) Library Pin Chart

  Board	               I2C / TWI pins
Uno, Ethernet       A4 (SDA), A5 (SCL)
Mega2560            20 (SDA), 21 (SCL)
Leonardo             2 (SDA),  3 (SCL)
Due/Udoo            20 (SDA), 21 (SCL), SDA1, SCL1

           Arduino Interrupt Pin Table

  Board	        Int.0  int.1  int.2  int.3  int.4  int.5
Uno R3, Ethernet    2      3      -      -      -      -
Leonardo            3      2      0      1      7      -
Mega	            2      3	 21     20     19     18
Due/Udoo                    (see below)

The Arduino Due board has powerful interrupt capabilities that allows you to attach an interrupt function on all available pins. You can directly specify the pin number in attachInterrupt(). 

           MOD-1016 SPI Pinout

  MOD-1016         Uno R3        Leonardo
VDD                  5v             5v
GND                 GND            GND
MOSI        11 or ICSP-4          ICSP-4
MISO        12 or ICSP-1          ICSP-1
SCLK        13 or ICSP-3          ICSP-3
IRQ               2 or 3     3, 2, 0, 1, or 7
CS                   10             10

CPU Type and How to Determine Arduino Bord

According to selected target processor, compiler defined constant by processor name.

  Constant                CPU              Board

__AVR_ATmega168__          ATmega 168      Arduino Decimilia and older
__AVR_ATmega328P__         ATmega 328P     Arduino Duemilanove and Uno
__AVR_ATmega1280__         ATmega 1280     Arduino Mega
__AVR_ATmega2560__         ATmega 2560     Arduino Mega 2560
__AVR_ATmega32U4__         ATmega 32U4     Arduino Leonardo
__SAM3X8E__                AT91SAM3X8E     Arduino Due

