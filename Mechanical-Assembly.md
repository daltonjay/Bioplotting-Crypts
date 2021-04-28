# Mechanical Assembly for Bioplotter

## Bioplotter Assembly

<iframe src="https://vanderbilt389.autodesk360.com/shares/public/SH919a0QTf3c32634dcf75c5ffeb4a9aec1c?mode=embed" width="680" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

## Bioplotter Overview
The _BioFAB Four Crypt Plotter_ is designed to achieve high resolution 3-dimensional bioprinting. The design is intended for printing hydrogel-based structures for the creation of intestinal crypt models within transwells. Yet, the bioplotter has intentionally been crafted for translation to alternative uses. Features that enable translation include:
- a print bed that exceeds the size necessary for crypt printing
- a larger range of motion for the print head provided by the corexy and z-direction stage motion
- interchangeable syringes for easy change between printed materials
- fast print times due to the lightweight carriage containing only the print head in the corexy system
- an awesome design to look good in any research laboratory, makerspace, or garage (depending on your taste)!

The Crypt Bioplotter employs a syringe pump based extrusion system, a linear actuator system for z-axis motion of the stage, and the [coreXY](http://corexy.com/index.html) technique to achieve flexible x and y motion of the print head. With this design, we are printing crypt structures with hydrogels (see [materials](/Bioplotting-Crypts/materials)) that can be seeded by stem cells (see [biological relevance](/Bioplotting-Crypts/Biological-Relevance/)). This enables recapitulation of intestinal organs that transcends current organoid technology.

### 3D Linear Motion
The Crypt Bioplotter is mobile in the x, y, and z directions. Z-axis motion is achieved by a NEMA-17 driven linear actuator that moves the print stage. The print stage is guided and supported by four linear rods attached via linear ball bearings for near frictionless motion. X- and y-axis motion are both achieved by the coreXY technique. The technique enables two motors to simultaneously manipulate the print head via a belt system. CoreXY is lightweight since it does not require the motion of any heavy motors. Motion without motors also reduces the inertia of the mobile components, thus, rapid accelerations can be achieved. This makes our x-y system and, as a result, our printer very fast. CoreXY also enables flexible printing, meaning that the print head can be moved at more angles than standard cartesian printers. This is desirable when printing small, curved structures, as we are doing with crypt printing. 

**Z-Axis Motion**

Linear actuation is driven by a NEMA-17 and a nut-locking mechanism built in to the stage. The stage is stabalized and guided by four linear rods with frictionless linear bearings.

![Z-Axis Motion by Linear Actuation](/Bioplotter-Assembly-Pictures/z-axis-pic.png)

**CoreXY System for X and Y motion**

The coreXY system operates with a two belt system driven by two NEMA-17 motors. Each driver pulley is connected with three idle pulleys to move the print head and print head cassette in the x and y directions. In the picture below, pulleys that are connected together for print head manipulation are grouped by color (red or green). Idle pulleys on the print head cassette would be connected to the print head by belt clips in practice. For more information on the coreXY system and implementation of the system, see the [coreXY website.](http://corexy.com/index.html) 

![CoreXY](/Bioplotter-Assembly-Pictures/coreXY.png)

### Extruder Design
The extruder system relies on a syringe pump system. The syringe pump system is attached to the print head by PVC tubing such that the syringe pump can rest beside the printer as opposed to attaching the syringe to the print head, reducing the burden of weight on our printer. The tubing is flexible enough to be run up to and move with the print head during operation while being rigid enough to not cause hysteresis, as may be seen with more flexible tubing. The syringe pump is driven by a NEMA-17-based linear actuator. By implementing a microstepping method to achieve a sixteenth of a step for the motor rotation, we achieve smaller interval motions of the plunger driver and, as a result, higher extrusion resolution. With the current materials used (i.e., the threaded rod with a pitch of 1.25mm), this syringe pump system enables us to achieve an extrusion resolution of 0.45uL per rotation. For more information regarding the syringe pump employed for this design, visit the [Syringe Pump website](https://daltonjay.github.io/Syringe-Pump/). Components for building the syringe pump have been included in the bill of materials. 

![Syringe Pump Extrusion](/Bioplotter-Assembly-Pictures/Syringe-Pump-v5.png)

### Sterility
By sealing the connection between the syringe and the print head with PVC tubing, we have created a closed system in which sterility is maintained to keep the printed hydrogel clean for later cell seeding. For further sterile practices, the printer is small enough to fit inside a standard biosafety cabinet. Since the device is not being packaged for commerical use and is instead used for laboratory research, sterility with respect to _good manufacturing practices (GMP)_ is not of relevance. 


### Future Directions

**4D Motion**

The corexy system functions by moving both x and y directions simultaneously to achieve more flexible printing capabilities. As already mentioned, this overcomes the rigidity typical of standard cartesian 3D printers. Yet, while the Crypt Plotter can print with higher angular accuracy, the printer remains fairly limited in its ability to create circular shapes - an important consideration for printing small cylindrical / conic structures, as we are doing when fabricating crypts. Thus, a future direction of this work would be to include a rotational axis to make the print 4-dimensional. This may look like adding a motor controlled rotational plate that can be added on top of the stage. The plate could be controlled by a motor and belt system, but may require z-axis motion of the motor used for this. The weight added to the z-ais, however, may be very well worth it to achieve high circular resolution.

**Multi-syringe system**

By implementing some means of using multiple print nozzles (e.g., two nozzles in the same print head), the Crypt Bioplotter could be easily adapted to print two separate materials in the same print. This would be accomplished by the use of two syringe pumps (aforementioned) in parallel. Both pumps would be closed-systems connected to separate print nozzles by PVC tubing. This implementation would require the software to accomodate for different positioning of the print nozzles in between the use of materials. This would improve the ease of use for multi-material prints. For example, the Crypt Plotter could print an acrylated hydrogel to provide structure and stability with ease in printing that could then be lined with Collagen IV printed from the second nozzle to provide cellular access to functional moieties for differentiation. 

**Print Head Changing System**

An alternative means to leveraging an effective multi-material printing system, the Crypt Bioplotter could be developed to have exchangeable print heads. This would reduce the burden of software accommodations for different positionings of the print head, enable the change in print nozzle size and temperature, and allow for rapid change of materials during the print process. A print head changing system would offer great potential for changing between syringe pump driven systems and droplet-on-demand systems that would be preferable for single-cell printing, if so desired for future uses.

**Single-cell Printing**

Addition of a droplet-on-demand (DOD) system would enable the Crypt Bioplotter to print with single-cell resolution. Inclusion of this in the printer would enable the bioplotter to print the crypts with hydrogel and then switch to the DOD system during the print to seed the crypt with cells. This would reduce the burden of adding the cells that would typically be left to the investigator. Further, this would ensure high accuracy and cell count for sensitive fabrication or studies. If the DOD inkjet system could be used in the print head changing system, the bioplotter could toggle between the cells and hydrogel materials with relative ease.

## Bill of Materials

Item         | Quantity  | Cost (per unit)
------------ | ----------|----------
[Aluminum Extrusion (1ft)](https://www.mcmaster.com/47065T107/) | 1 | $8.22
[Threaded Linear Rod (300mm)](https://www.mcmaster.com/1078N32/) | 2 | $12.57
[Linear Rod (300mm)](https://www.mcmaster.com/6112K44/) | 9 | $7.21
[Linear Bearing (#61205K75)](https://www.mcmaster.com/61205K75/) | 9 | $19.71
[External Retaining Ring (#9968K32)](https://www.mcmaster.com/9968K32/) | 6 | $0.72
[M8 Hex Nut (1.25 mm thread)](https://www.mcmaster.com/90592A022/) | 1 | $0.05
[5/32" T Nut & Bolt (1/4"-20 thread)](https://www.mcmaster.com/47065T139/) | 6 | $0.46
[M3 screws (Depth 4.5mm)](https://www.mcmaster.com/91251A059) | 4 | $0.29
[UV-Resistant Acrylic Sheet (12"x12"x1/8")](https://www.mcmaster.com/8560K239/) | 1 | $9.70
[Timing Pulley, 18T MXL (Idle)](https://shop.sdp-si.com/catalog/product/?id=A_6M16M018DF6006) | 8 | $10.73
[Timing Pulley, 18T MXL (Drive)](https://shop.sdp-si.com/catalog/product/?id=A_6T16M018DF6005) | 2 | $8.71
[MXL Timing Belt, 1/4" W, 77"L](https://www.mcmaster.com/1679K686/) | 2 | $10.10


## 3D Modeled Parts

[Home](/Bioplotting-Crypts/index)

[**Mechanical Assembly**](/Bioplotting-Crypts/Mechanical-Assembly)

[Electrical Logic](/Bioplotting-Crypts/Electrical-Assembly)

[Software Overview](/Bioplotting-Crypts/Software)

[Materials Overview](/Bioplotting-Crypts/Materials)

[Biological Relevance and Cells](/Bioplotting-Crypts/Biological-Relevance)

[Meet BioFAB Four](/Bioplotting-Crypts/meet-the-team)
