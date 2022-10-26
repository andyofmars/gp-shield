# gp-shield - A general purpose arduino-compatible shield for UTAS projects

## Overview
The shield is intended to be used as a general purpose shield for Arduino Uno compatible microcontroller development boards or as an interface between a development board and other custom electronics.

From previous projects we have identified multiple common issues when interfacing with common microcontroller development boards including the Arduino UNO and Xplained Mini series of development boards.
1. Many development boards are sensitive to fluctuations in the power supply during programming and can become 'bricked'.
1. A lack of protection on the Vin and 5V lines when being powered from a shield or other electronics makes them susceptible to damage.
1. Due to the lacj of protection on GPIO pins and the lareg number of exposed GPIO pins it is easy to draw too much current or apply an overvoltage condition which will damage the microcontroller.

See https://www.rugged-circuits.com/10-ways-to-destroy-an-arduino for more issues with the Arduino UNO.

To resolve these issue for most use cases and provide general functionality commonly needed in electronics projects we have developed the gp-shield to be used as the standard method of interfacing with Arduino UNO compatible development boards.

Features of the gp-shield are:
- Can be powered from external battery (~6V - 20V)
- Power supply includes overvoltage (25V?), overcurrent (6A), and reverse polarity protection as well as undervoltage lockout (adjustable?) and an on-board or external power switch.
- Onboard 5V regulation (up to 1A output) with circuitry to safely handle condition where board is powered externally while the development board is powered by USB.
- Overvoltage (5.1V) and overcurrent (30mA) protection on all GPIO pins when using the on-board connections
- Standard connectors for analogue outputs, PORTD and PORTB GPIO pins, 6 PWM outputs, UART, SPI and a high current output for powereing other electronics from the same supply with all of the built in seafty features.
- On-board reset switch
- On-board general purpose LED and push button
