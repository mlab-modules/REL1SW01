# REL1SW01 - One Relay and/or Two N-MOSFET

## Introduction
The REL1SW01 is a versatile module from the MLAB series designed for triggering high current demaining devices (eg. high power led, high voltage circuits, DC motors, ..) using two N-MOSFET transistors or relay. It supports both bistable and monostable relay configurations and can be integrated into various electronic projects requiring relay switching or direct MOSFET control.

![REL1SW01A](/doc/gen/img/REL1SW01-top.png)

## Features
- Equipped with two N-MOSFET transistors (IRLML6244).
  - Capable of switching voltages up to 20V.
- Supports optional relay addition (e.g., DPDT FRT5).
- Configurable for either relay coil driving or independent transistor switching.
- Compatible with MCU control.

## Specifications
### MOSFET Transistors (IRLML6244)
- **Drain-Source Voltage (Vds):** 20V
- **Gate-Source Voltage (Vgs):** ±12V
- **Continuous Drain Current (Id):** 6.3A
- **Total Power Dissipation (Pd):** 1.3W
- **Gate Threshold Voltage (Vgs(th)):** 1.1V
- **On-State Resistance (Rds(on)):** 21mΩ at Vgs = 4.5V


## Usage
### Without Relay
- Connect the load to the drain of the MOSFET.
- The source of the MOSFET should be connected to GND.
- Use the gate to control switching via the MCU.

### With Relay
- Connect the relay's coil terminals to the MOSFETs as per the required configuration.
- The relay contacts will then be used to switch the external load.

## Configuration
To configure the module for different uses:
1. For direct MOSFET switching, connect the load between the drain and the positive supply (VCC).
2. For relay operation, connect the relay coil to the designated pins controlled by the MOSFETs.
