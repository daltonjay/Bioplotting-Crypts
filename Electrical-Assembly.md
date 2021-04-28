# Electrical Assembly for Bioplotter

![Electrical diagram featuring the general layout of control and components.](/Bioplotting-Crypts/BioPics/finalelectricaldiagram.png)

# General Overview

Few specialty components are required for our bioplotter. Rather, standard NEMA 17 stepper motors, inexpensive drivers, and a single Arduino Uno are necessary to construct this device. 

Note: Due to the scale of the Transwell prints, resolution and stability of motion are necessary over speed, so it is recommended a further 3 digital pins are reserved to enable microstepping on the controllers.

# Future Directions

## Closed Loop Control System

To keep the overall price down for the crypt bioplotter and due to the relatively light system used, encoders/resolvers were not included in our original design. However, in the interest of increasing reliablity and removing any potential positioning error in the device, replacing the basic NEMA 17 Stepper Motors with a set that has built in encoders might be fruitful. A potential iteration of the software could include an option for including feedback from these encoders to ensure proper positioning is achieved, at least on the motor end--a different methology would be necessary to account for lash error. Closed loop control would be especially important in a drop-on-demand delivery system where increased precision and control of individual cell distribution control are critical. 

## UV Crosslinking

Only covering the bottom of the crypt with Collagen IV has the advantage of hastening print times and making crosslinking unnecessary. However, should layers of the protein be required a simple UV light source could be integrated with the print head to flash crosslink the protein. Control of this mechanism would have to be left to a relay wired to the Arduino Uno, flashing the lamp on and off when a layer was positioned properly. The existing voltage sources can be used to provide both the relay current and the lamp power. 

## Droplet on Demand

By far the most difficult to introduce electronically, creating a DoD system would require alterations in our syringe structure and pump, allowing us to quickly heat or use electrostatics to expel a single drop of the cell solution. Most of the work would need to be done on the mechanical side, but a custom driving system would need to be integrated with the electronics. 

## Bill of Materials

Item         | Quantity  |Cost (per unit)
------------ | ----------|-------------
[Solderless Breadboard & Jumpers](https://www.digikey.com/en/products/detail/twin-industries/TW-E41-102B/643113) | 1 | $15.99
[5V and 24V Power Sources]() | 1 | In house
[Arduino Uno](https://www.digikey.com/en/products/detail/arduino/A000073/3476357) | 4 | $20.90
[DCNC-Nema 17-0.5nm Stepper Motor 24V](https://www.digikey.com/en/products/detail/nmb-technologies-corporation/17PM-K858-00VS/2416995) | 4 | $49.56
[Stepper Motor Driver](https://www.digikey.com/en/products/detail/monolithic-power-systems-inc/MP6601GU-P/9817885) | 4 | $3.37

# Navigation
[Home](/Bioplotting-Crypts/index)

[Mechanical Assembly](/Bioplotting-Crypts/Mechanical-Assembly)

[**Electrical Logic**](/Bioplotting-Crypts/Electrical-Assembly)

[Software Overview](/Bioplotting-Crypts/Software)

[Materials Overview](/Bioplotting-Crypts/Materials)

[Biological Relevance and Cells](/Bioplotting-Crypts/Biological-Relevance)

[Meet BioFAB Four](/Bioplotting-Crypts/meet-the-team)
