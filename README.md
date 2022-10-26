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
The Gerber files can be downloded here:
