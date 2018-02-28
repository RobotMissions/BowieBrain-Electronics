# Bowie Brain Board v1.1

![Robot Missions logo, a green leaf on a white diamond situated within a purple circle](http://robotmissions.org/images/github/robot_missions_colour_500px.png)

Bowie Brain Board is the electronics for the [Robot Missions](http://robotmissions.org) introductory robot platform, _Bowie_.

### More information about our robot platform at the [Robot Missions Website ➞](http://robotmissions.org)

The Robot Missions Bowie Brain Board has ports for 6 servos, connections for 4 DC motors (2 controlled independently), can measure the current draw from the servos or DC motors, and has several connections for extendable modules. Microcontroller uses a [Teensy 3.6](https://www.pjrc.com/store/teensy36.html) for full functionality including data logging, or a [Teensy 3.2](https://www.pjrc.com/store/teensy32.html).

Firmware can be found here: [Bowie Library](https://github.com/RobotMissions/BowieLib) and [Bowie Shoreline](https://github.com/RobotMissions/BowieShoreline).

This board was designed in gEDA. You can edit it in [pcb-rnd](http://repo.hu/projects/pcb-rnd/).

## Pinouts

There are several ways you can extend the functionality of your Bowie robot. Here are the labeled connector ports with the according pins.

> **Note:** TX_n_ denotes data out from the brain's microcontroller, and RX_n_ is data in to it.

![Labeled connector pinouts](http://robotmissions.org/images/github/brain_board_pins_small_new.png)

## Schematics

For all pin usage, [see this spreadsheet](https://docs.google.com/spreadsheets/d/1hbOPDjGGXycjbXXOjvf-UFxm08XbPSapu2aIzFMsICY/edit?usp=sharing). _Note: This board was designed without a schematic._

## Board Setups

### Teensy 3.6

The setup for Teensy 3.6 uses the full functionality of the brain board. Solder all of the headers on to the teensy, except for the column in the middle. Make sure the male and female pins in the middle rows line up.

![Teensy 3.6 installed in the Robot Missions Brain Board v1.0](http://robotmissions.org/images/github/robot_missions_brain_teensy36.jpg)

### Teensy 3.2

The setup for Teensy 3.2 is a bit different. To get access to all of the servo pins and more of the GPIO, you have to solder a ribbon header out.

![Teensy 3.2 installed in the Robot Missions Brain Board v1.0](http://robotmissions.org/images/github/robot_missions_brain_teensy32.jpg)

Following the above image:

| Wire colour in image  |  Teensy 3.2 Pin  |  Bottom Row Header Pin
| :-------------------: | :--------------: | :-----------------:
| Black | 32 | 24
| White | 31 | 23
| Grey | 30 | 22
| Purple | 29 | 21
| Blue | 28 | 20
| Green | 27 | 19
| Yellow | 26 | 18
| Orange | 25 | 17
| Red | 24 | 16

## Bill of Materials

| Refdes | Description | Source |
| --- | --- | --- |
| N/A | Bowie Brain Board | [Robot Missions](mailto:hello@robotmissions.org) |
| U1 | Microcontroller Teensy 3.6 or Teensy 3.2 | PJRC: [3.6](https://www.pjrc.com/store/teensy36.html), [3.2](https://www.pjrc.com/store/teensy32.html) |
| U2 | Xbee Series 3 with whip antenna | Digikey 602-1560-ND |
| U2 | Xbee headers | Digikey S5751-10-ND |
| U3 | Motor driver TB6612FNG | [A2D Electronics](https://a2delectronics.ca/shop/modules/tb6612fng-motor-driver/) |
| U4 | 3.3V 1A regulator | [Pololu](https://www.pololu.com/product/2830) — Alternate _(less current)_: Digikey 497-7246-1-ND |
| U5, U6 | Current sensor | [Pololu](https://www.pololu.com/product/2453) |
| R1, R2, R3, R4, R5 | 330 Resistors for Xbee LEDs | Digikey 330QBK-ND |
| R6, R7 | 4.7k Pull-up resistors for I2C | Digikey 4.7KQBK-ND |
| R8 | 10K Voltage divider resistor for battery monitor | Digikey 10KQBK-ND |
| R9 | 20K Voltage divider resistor for battery monitor | Digikey 20KQBK-ND |
| R10 | 330 Resistor for speaker | Digikey 330QBK-ND |
| R11 | 2.0K Resistor for speaker | Digikey 2.0KQBK-ND |
| D1, D3 | 5mm Red LED | Digikey C503B-RCN-CX0Y0AA1-ND |
| D2, D4 | 5mm Green LED | Digikey C503B-GAN-CC0D0891-ND |
| D5 | 10mm LED | Digikey 754-1898-ND |
| D6 | 1N4001 Diode | Digikey 1N4001-TPMSCT-ND |
| LS | Speaker | Digikey 445-2525-1-ND |
| Q1 | PN2222A Transistor | Digikey PN2222AD26ZCT-ND |
| PWR IN | Barrier block | Digikey A98474-ND |
| J2 | _Optional_ Power supply connection using JST-SM 6 pin | [Adafruit](https://www.adafruit.com/product/1665) |
| J3 | Screw terminals | Digikey A98079-ND |
| J4, J5, J6, J7 | Motor connections using JST-SM | Digikey 1528-1596-ND | 
| N/A | Terminals for barrier block | Digikey A0989CT-ND |
| N/A | Coincell holder | Digikey BS-7-ND |
| N/A | 4x M3 8mm mounting screws | Home Hardware |
| N/A | Servo extension cables | [Hobbyking](https://hobbyking.com/en_us/twisted-30cm-servo-lead-extention-jr-22awg-5pcs-set.html) |
| N/A | Headers F | [A2D Electronics](https://a2delectronics.ca/shop/wires-and-connectors/5pcs-40pin-2-54mm-female-headers/) |
| N/A | Headers M | [A2D Electronics](https://a2delectronics.ca/shop/wires-and-connectors/5pcs-40pin-2-54mm-male-headers/) |
| N/A | Micro SD Card | Canada Computers | 
| N/A | 3V Coincell CR2023 | Dollarama |

## License

This board is released under the [CERN Open Hardware License v1.2](https://www.ohwr.org/projects/cernohl/wiki).

## Bug Reports / Feature Requests

Found a bug? Looking for a feature? Let us know by opening an Issue report. Further questions can be posted to our [forum](http://forum.robotmissions.org).

---

🤖✌️🌎

**Robot Missions - Helping the planet with robots**
