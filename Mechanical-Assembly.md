# Mechanical Assembly for Bioplotter

## Bioplotter Overview
The _BioFAB Four Crypt Plotter_ is designed to achieve high resolution 3-dimensional bioprinting. The design is intended for printing hydrogel-based structures for the creation of intestinal crypt models within transwells. Yet, the bioplotter has intentionally been crafted for translation to alternative uses. Features that enable translation include:
- a print bed that exceeds the size necessary for crypt printing
- a larger range of motion for the print head provided by the corexy and z-direction stage motion
- interchangeable syringes for easy change between printed materials
- fast print times due to the lightweight carriage containing only the print head in the corexy system
- an awesome design to look good in any research laboratory, makerspace, or garage (depending on your taste)!

The Crpyt Bioplotter employs a syringe pump based extrusion system, a linear actuator system for z-axis motion of the stage, and the [coreXY](http://corexy.com/index.html) technique to achieve flexible x and y motion of the print head. With this design, we are printing crypt structures with hydrogels (see [materials](/Bioplotting-Crypts/materials)) that can be seeded by stem cells (see [biological relevance](/Bioplotting-Crypts/Biological-Relevance/)). This enables recapitulation of intestinal organs that transcends current organoid technology.

### 3D Linear Motion
The Crypt Bioplotter is mobile in the x, y, and z directions. Z-axis motion is achieved by a NEMA-17 driven linear actuator that moves the print stage. The print stage is guided and supported by four linear rods attached via linear ball bearings for near frictionless motion. X- and y-axis motion are both achieved by the coreXY technique. The technique enables two motors to simultaneously manipulate the print head via a belt system. CoreXY is lightweight since it does not require the motion of any heavy motors. Motion without motors also reduces the inertia of the mobile components, thus, rapid accelerations can be achieved. This makes our x-y system and, as a result, our printer very fast. CoreXY also enables flexible printing, meaning that the print head can be moved at more angles than standard cartesian printers. This is desirable when printing small, curved structures, as we are doing with crypt printing. 

### Extruder Design
The extruder system relies on a syringe pump system. The syringe pump is driven by a NEMA-17-based linear actuator. By implementing a microstepping method to achieve a sixteenth of a step for the motor rotation, we achieve smaller interval motions of the plunger driver and, as a result, higher extrusion resolution. With the current materials used (i.e., the threaded rod with a pitch of 1.25mm), this syringe pump system enables us to acheive an extrusion resolution of 0.45uL per rotation. For more information regarding the syringe pump employed for this design, visit the [Syringe Pump webiste](https://daltonjay.github.io/Syringe-Pump/)

### Sterility

### Future Directions

**4D Motion**
The corexy system functions by moving both x and y directions simultaneously to achieve the flexible printing capabilities. As aforementioned, this overcomes the rigidity typical of standard cartesian 3D printers. Yet, while the Crypt Plotter can print with higher angular accuracy, the printer remains fairly limited in its ability to create circular shapes - an important consideration for printing small cylindrical / conic structures, as we are doing when fabricating crypts. Thus, a future direction of this work would be to include a rotational axis to make the print 4-dimensional. This may look like adding a motor controlled rotational plate that can be added on top of the stage. The plate could be controlled by a motor and belt system, but may require z-axis motion of the motor used for this. The weight added to the z-ais, however, may be very well worth it to achieve high circular resolution.

**Multi-syringe system**


**Print Head Changing System**

**Single-cell Printing**

## Bioplotter Assembly

## Bill of Materials

Item         | Quantity  | Cost (per unit)
------------ | ----------|----------
[Aluminum Extrusion (1ft)](https://www.mcmaster.com/47065T107/) | 1 | $8.22
[Threaded Linear Rod (300mm)](https://www.mcmaster.com/1078N32/) | 2 | $12.57
[Linear Rod (300mm)](https://www.mcmaster.com/6112K44/) | 5 | $7.21
[Linear Bearing (#61205K75)](https://www.mcmaster.com/61205K75/) | 5 | $19.71
[External Retaining Ring (#9968K32)](https://www.mcmaster.com/9968K32/) | 6 | $0.72
[M8 Hex Nut (1.25 mm thread)](https://www.mcmaster.com/90592A022/) | 1 | $0.05
[5/32" T Nut & Bolt (1/4"-20 thread)](https://www.mcmaster.com/47065T139/) | 6 | $0.46
[M3 screws (Depth 4.5mm)](https://www.mcmaster.com/91251A059) | 4 | $0.29
[UV-Resistant Acrylic Sheet (12"x12"x1/8")](https://www.mcmaster.com/8560K239/) | 1 | $9.70
[Timing Pulley, 18T MXL (Idle)](https://shop.sdp-si.com/catalog/product/?id=A_6M16M018DF6006) | 8 | $10.73
[Timing Pulley, 18T MXL (Drive)](https://shop.sdp-si.com/catalog/product/?id=A_6T16M018DF6005) | 2 | $8.71
[MXL Timing Belt, 1/4" W, 77"L](https://www.mcmaster.com/1679K686/) | 2 | $10.10


## 3D Modeled Parts
