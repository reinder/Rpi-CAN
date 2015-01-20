# Rpi-CAN
Rpi-CAN is a CAN-bus extension board for Raspberry Pi.

The board runs completly on 3.3V and is powered by the Raspberry Pi 3.3 V rail.
Alternativly it can be powered by the Raspberry Pi 5V rail.

The Rpi-CAN uses the [Microchip MCP2515 CAN controller](www.microchip.com/solutionsmcp2515) via SPI.
The MCP2515 is supported by Linux and Raspbian, allthough support for the MCP2515 is missing in the default Raspbian kernel.

**NOTE:** There is no galvanic isolation between the CAN-bus and the Raspberry Pi!

## Components
- R1: Resistor, 0 Ohm, 0805 (Optional: only if directly powered from the 3.3 V rail.)
- R2: Resistor, 120 Ohm, 0805 
- R3: Resistor, 10 kOhm, 0805 
- R4: Resistor, 10 kOhm, 0805 
- R5: Resistor, 0 Ohm, 0805 (Optional: for connecting *optional ground* to the Raspberry Pi ground) 
- R6: Resistor, 0 Ohm, 0805 (Optional: for connecting *CAN-ground* to the Raspberry Pi ground)
- R7: Resistor, 0 Ohm, 0805 (Optional: for connecting *optional power* to the Raspberry Pi 5V rail)
- C1: Ceramic Capacitor, 100 nF, 0805
- C1: Ceramic Capacitor, 100 nF, 0805
- C5: Ceramic Capacitor, 18 pF, 0805
- C6: Ceramic Capacitor, 18 pF, 0805
- C9: Ceramic Capacitor, 100 nF, 0805 (Optional: only if powered from 5 V rail.)
- C10: Ceramic Capacitor, 100 nF, 0805 (Optional: only if powered from 5 V rail.)
- Q1: Crystal, 20 MHz, SM49
- IC1: CAN tranciever, SN65HVD233-HT, SO-8
- IC2: CAN controller, MCP2515, SO-18W
- IC3: Voltage regulator 3.3V, XC6221B332MR, SOT25 (Optional: only if powered from 5 V rail.)
- JP1: 3 pin jumper, RM254
- JP2: 2 pin jumper, RM254
- JP3: 3 pin jumper, RM254
- X2: Pin header 2x13 female, RM254 
- X3: D-sub 9 pin male, solder

## Jumpers
- JP1 is for selecting the SPI chip select (CS0 or CS1).
- JP2 is for enabling/disabling the 120 Ohm bus temination resitor.
- JP3 is for selecting the interrupt GPIO (23 or 24).
