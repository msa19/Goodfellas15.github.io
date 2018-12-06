---
#
# Here you can change the text shown in the Home page before the Latest Posts section.
#
# Edit cayman-blog's home layout in _layouts instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#
layout: home
---
<center><img src="https://raw.githubusercontent.com/Goodfellas15/Goodfellas15.github.io/master/speed-e%20logo.jpg" alt="logo of speed-e" style="max-width:40%;"/></center>

<h1 align="center"> Speed-e: Speeding up, Saving Lives </h1>

## Background:
The first hour after a traumatic injury, aka ‘The Golden Hour’, is considered the most critical time frame for successful treatment. Optimal routing obtained by continuously monitoring traffic conditions is necessary to reduce the transition between the initial call, response to an emergency, and the transit to the location of the incident.

## Overview
Speed-E aims to provide efficient traffic routes to emergency responders using real time vehicle sensing technology. Collected data will be transmitted to other accessible nodes and eventually an online server. First responders will then gain access to the data through a web interface, which reroutes accordingly to provide the fastest arrival time.
## Block Diagram
<img src="https://raw.githubusercontent.com/Goodfellas15/Goodfellas15.github.io/master/block_diagram.png" alt="block diagram" style="max-width:100%;"/>
## Conceptual Design
Currently researching the most viable material that can withstand weathering, vehicular impact, and  abrasion. Our primary consideration for material would be plastic, similar to that of the raised pavement markers.

## Key Components
### TI DRV5053 Analog-Bipolar Hall Effect Sensor
Outputs a voltage depending on the magnetic field around it
* Sensitivity: 9 mT
* Average current: 2.7 mA
* Operating Voltage: 2.5V - 38V

### AVR® ATMega328P-PU Microcontroller
Microcontroller to be used within each device. User friendly and compatible with existing LoRa libraries.
* Operating Voltage: 1.8 V - 5.5 V
* On Current: 19 mA
* Sleep Mode Current: 0.3 µA

### RFM95 915 MHz LoRa Transceiver
Low cost transceiver operating at 915 MHz that provides long range transmission and low current draw
* Operating Voltage: 3 V
* TX Current: 10 mA 
* RX Current: 10.3 mA

## Expected Baterry Life
  
  |Current Draw (mA) | Time (H) |
--- | --- | --- |
Sleep Mode | 0.0003 | 22.3
On (Not Peak) | 19 | 0.3
Transmit | 30 | 1.4
Average Current | 0.272 mA


Capacity | Days | Years
--- | --- | ---
10,000 mAh | 1530.82 | 4.19

## Communication
### Network
* We use LoRaWAN
<img src="https://raw.githubusercontent.com/Goodfellas15/Goodfellas15.github.io/master/network50.png" alt="logo of speed-e" />
### Antenna Research
* We use antenna from Taoglas
<img src="https://raw.githubusercontent.com/Goodfellas15/Goodfellas15.github.io/master/testingAntenna50.png" alt="antenna"/>

* __First image (from left to right):__  Construct mock up board with ground plane that would simulate circuit ground plane with dimensions similar to road mark housing.
* __Second image:__  Potential antenna with ISM capabilities.
* __Third image:__  Test for signal loss due to reflections from the transmission line.
* __Fourth image:__  Test in anechoic chamber for efficiency and peak gain.
## Budget
