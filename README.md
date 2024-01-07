# Dual-pos-neg-5V-Supply-from-USB-power
Provides +/-5 power from USB power, KiCAD design files.

## Introduction
This repository provides KiCAD files for a filtered +/-5V supply that I use with some of the precision instrumentation circuits that I build and use in my lab.  These are often operated by microcontrollers such as Arduino and Teensy that typically provide only +5V (USB) or 3.3V power.
While a lot can be done in designing for single ended supplies, there are some important instrumention circuits that inherently require a dual supply.

In this design, the +5V supply is based on an LT1930 configured as a SEPIC converter to accomodate 
supply voltages that may be greater or lesser than the 5V output.
The -5V suppy is based on an LT1931, an inverting DC/DC converter.
The datasheets describe the supplies as providing 350mA and 300mA, respectfully.
In this design, the circuits are connected by jumpers to the input power connector.
Either supply can be turned off individually by removing the corresponding jumper which is located next to the 5V input.

![LT193n_+-5V_Supply](https://github.com/drmcnelson/Dual-pos-neg-5V-Supply-from-USB-power/assets/38619857/708b6ee7-3a98-4e26-a6b1-3268e7a2e2db)
