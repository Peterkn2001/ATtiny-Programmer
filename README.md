# ATtiny-Programmer
Custom PCB design to simplify using an Arduino Nano to program ATtiny 25/45/85 chips 

## Overview
This is a PCB designed to simplify programming ATtiny 25/45/85 chips using an Arduino Namo.
This repository contains the Gerber files to allow you to order your own PCBs from suppliers such as
JLCPCB and PCBWay

## Images
![PCB Front](https://github.com/Peterkn2001/ATtiny-Programmer/blob/main/images/ATtiny_Programmer_PCB_front.jpg)

![PCB Back](https://github.com/Peterkn2001/ATtiny-Programmer/blob/main/images/ATtiny_Programmer_PCB_back.jpg)

![Completed PCB](https://github.com/Peterkn2001/ATtiny-Programmer/blob/main/images/Programmer.jpg)

## Bill of Materials

### Bill of Materials for ATTiny Programmer V1.0

Description | Quantity
:--- | :---:
Arduino Nano (Original version) | 1
LED in SMT 0805 package | 1
1k Resistor in SMT 0805 package | 1
10uf 16v radial lead electrolytic capacitor| 1
6x6mm momentary tactile through-hole switch | 1
18-Pin ZIF IDP socket (see notes below) | 1
15-pin 0.1" headers (Optional) | 2
8-pin 0.1" PCB mount ribbon cable header (Optional)| 1

### Notes

Only 8 pins are used on the ZIF Socket, but these sockets are commonly only available in 14 pins or greater.
A 16 pin socket is used to allow an SOP8 adapter to be used without fouling the ZIF lever,
but a 14 pin version (or smaller if available) could be substituted if this is not a consideration

![ZIF Socket](https://github.com/Peterkn2001/ATtiny-Programmer/blob/main/images/ZIF_Socket.jpg)

The 15-pin 0.1" headers are not needed if you solder the Nano directly to the PCB (Not recommended)

The 8-pin 0.1" PCB mount ribbon cable header is only needed if you wish to connect a programming clip to allow
SMD or through-hole devices to be programmed in-situ

## Gerber File
The Gerber file can be downloaded here:

https://github.com/Peterkn2001/ATtiny-Programmer/blob/main/Gerber/Gerber_ATtiny%20Programmer%20v1_0.zip

Note that this is a .zip file and does not need to be un-zipped. Simply upload it to your PCB supplier as a .zip file.

## Additional Information

### Arduino Nano
In my experience, only the original Arduino Nano will work with this hardware and the sketch below. The Nano Pro Micro doesn't work.

### Sketch for the Nano
The Nano needs to be flashed with this sketch (written by Randall Bohn)...

https://github.com/Peterkn2001/ATtiny-Programmer/blob/main/ArduinoISP/ArduinoISP.ino

### Installing the ATtiny Core
Follow the instructions here to install the ATtiny core and board definitions:

https://github.com/damellis/attiny/

Other ATtiny cores may also work, but this is the one that I use.

### Flashing the ATtiny firmware
Begin by choosing "Arduino as ISP" in the Tools > Programmer menu of the Arduino IDE...

![PCB Front](https://github.com/Peterkn2001/ATtiny-Programmer/blob/main/images/Arduino_IDE_Settings.jpg)

With the ATtiny in the ZIF socket (orientated with Pin 1 next to the white dot on the PCB - near the Activity LED) and the correct Board and Processor selected in the IDE, plug the programmer in and select the correct serial port in the IDE.
Select "Burn Bootloader" in the IDE's Tools menu. This will burn a bootloader to the AT tiny to enable a sketch to be uploaded.

Once this is done your ATtiny is ready for you to upload your sketch using the Sketch > Upload Using Programmer CTRL+Shift+U command in the IDE.

