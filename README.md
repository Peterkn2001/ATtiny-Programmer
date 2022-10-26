# ATtiny-Programmer
Using an Arduino Nano to program ATtiny 25/45/85 chips 

## Overview
This is a PCB designed to simplyfy programming ATtiny 25/45/85 chips using an Arduino Namo.
This repository contains the Gerber files to allow you to order your own PCBs from suppliers such as
JLCPCB and PCBWay

## Images
![PCB Front](https://github.com/Peterkn2001/ATtiny-Programmer/blob/main/images/ATtiny_Programmer_PCB_front.jpg)

![PCB Back](https://github.com/Peterkn2001/ATtiny-Programmer/blob/main/images/ATtiny_Programmer_PCB_back.jpg)

![Completed PCB](https://github.com/Peterkn2001/ATtiny-Programmer/blob/main/images/ATtiny_Programmer_PCB_Complete.jpg)

## Bill of Materials

### Bill of Materials for ATTiny Programmer V1.0

Description | Quantity
------------ | -------------
Ardduino Nano (Original version) |1
LED in SMT 0805 package | 1
1k Resistor in 0805 package | 1
10uf 5v or more radial lead Electrolytic Capacitor| 1
6x6mm momentary tactile through-hole switch | 1
18-Pin ZIF IDP Socket (see notes below) | 1
15-pin 0.1" headers (Optional) | 2
8-pin 0.1" PCB mount ribbon cable header (Optional)| 1

### Notes

Only 8 pins are used on the ZIF Socket.
These lever-operated Zero Insertion Force sockets are commonly only available in 14 pins or greater,
with the 16 pin version being very common. A 14 pin version coud be substituted if desired.

The 15-pin 0.1" headers are not needed if you solder the Nano directly to the PCB (Not reccomended)

The 8-pin 0.1" PCB mount ribbon cable header is only needed if you wish to connect a programming clip to allow
SMD or through-hole devices to be programmed in-situ

## Gerber Files
The Gerber file can be downloded here:

https://github.com/Peterkn2001/ATtiny-Programmer/blob/main/Gerber/Gerber_ATtiny%20Programmer%20v1_0.zip

Note that this is a .zip file and doesn not need to be un-zipped. Simply upload it to your PCB supplier.

## Additional Information

### Arduino Nano
In my experience, only the original Arduino Nano will work with this hardware and the sketch below. The Nano Pro Micro doesn't work.

### Sketch for the Nano
The Nano needs to be flashed with ths sketch (written by Randall Bohn)...

XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

### Installing the ATtiny Core
Follow the instructions here to install the ATtiny core and board definitions:
https://github.com/damellis/attiny/

Other ATtiny cores m,ay also work, bit this is the one that I use.

### Flashing the ATtiny firmware
Begin by choosing "Arduino as ISP" in the Programmer menu of the Arduino IDE...

![PCB Front](https://github.com/Peterkn2001/ATtiny-Programmer/blob/main/images/Arduino_IDE_Settings.jpg)

With the ATtiny in the ZIF socket and the correct Board and Procesor selected in the IDE, plug the programmer in and select the correct serial port in the IDE.
Select "Burn Bootloader" in the IDE's Tools menu. This will burn a bootloader to the AT tiny to enable a sketch to be uploaded.

Once this is done your ATtiny is ready for you to upload your sketch.

