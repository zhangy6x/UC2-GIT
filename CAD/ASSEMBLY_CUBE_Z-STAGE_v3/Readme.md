# Z-Stage (Objective) Cube
This is the repository for the Z-Stage (Objective) Cube.

The stl-files can be found in the folder [STL](./STL).

## Purpose
In microscopy one often needs the ability to move the objective along the optical axis in order to refocus a given 3D sample.
In order to automate this, we designed a very simple z-stage itself relying on flexure bearings also known from Bowman's flexurescope.

<p align="center">
<img src="./IMAGES/Assembly_Cube_Z_stage_sample_outercube_motorized.png" width="500">
</p>

### Properties
* theoretically no play due to the use of flexure bearings
* moving range +/-2mm
* very low cost by relying on off-the-shelf components
* motorized with a stepper motor

## Parts
### <img src="./IMAGES/P.png" height="40">

3D printing parts

* Inside the Prusa we add a support enforcer (green part) 
* Have 80-100% infill
* Layerheight: 200µm
* Remove the thin piece which is designed to support the motor holding bit

<p align="center">
<img src="./IMAGES/PrintStage.jpeg" width="500">
</p>


The Cube consists of the following components.

* **The Lid (1x1)** where the Arduino + Electronics finds its place ([LID](./STL/10_Lid_1x1_v2.stl))
* **The Cube (2x1)** which will be screwed to the Lid. Here all the functions (i.e. Mirrors, LED's etc.) find their place ([BASE](./STL/10_Cube_1x1_v2.stl))
* **The Z-Stage and Motor Holder** which moves the sample and holds the stepper motor ([INSERT](./STL/20_Cube_Insert_Z-Focus_single_motorized_v3.stl))
* **The Z-Stage for manual operation using a micrometer screw** it moves the sample using a micrometer ([INSERT](./STL/20_Cube_Insert_Z-Focus_single_v3))
* **The Z-Stage for manual operation using an M3 screw** it moves the sample using a M3 screw ([INSERT](./STL/20_Cube_Insert_Z-Focus_single_M3_v3))
* **The M3 to Motor Adapter (mech. Coupling)** which connects the Motor directly to an M3 screw which acts as a wormdrive ([SCREW](./STL/30_Coupling_Screw_28BYJ_M3.stl))
* **The Insert for the RMS/25mm objective** With this you can slide in the objective lens inside the lower cube ([RMS/25mm Lens adapter](./STL/20_IM_Cube_Insert_Lens_holder_RMS_63x.stl))
* **The insert for a RMS objective lens** With this you can move the objective lens rather than the sample. It fits inside the whole of the moving plate [Objective Mount](./STL/20_Cube_Insert_Z-Focus_objectivemount.stl)

***HINT:*** For the new puzzle-piece based cube, you need "M5 Madenschrauben". There will be more in the future. For now, please find some screws like these ones: [Ebay](https://www.ebay.de/itm/25-St-Madenschrauben-Gewindestifte-Spitze-DIN-914-M5-x-Laengen-4-bis-50-mm-V2A-/400494812602)


### <img src="./IMAGES/B.png" height="40"> Additional parts
* Check out the [RESOURCES](../../TUTORIALS/RESOURCES) for more information!
* 10× - 20× DIN912 M3×12 screws (galvanized steel) [🢂](https://eshop.wuerth.de/Zylinderschraube-mit-Innensechskant-SHR-ZYL-ISO4762-88-IS25-A2K-M3X12/00843%20%2012.sku/de/DE/EUR/)
* 3× DIN912 M3×8 screws (galvanized steel)
* 2× DIN912 M3×18 screws (galvanized steel)
* 1× M3 Nut
* 1× M3 Screw, 30 mm or longer (non-magnetic)
* 1× 28-BYJ stepper motor with 1x Driving electronic [🢂](https://www.amazon.de/Elegoo-Stepper-Schrittmotor-28BYJ-48-Treiberplatine/dp/B01MEGIHLF/ref=sr_1_1_sspa?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&keywords=stepper+arduino&qid=1565008205&s=gateway&sr=8-1-spons&psc=1)
* 1× ESP32 for controlling the motor [🢂](https://www.amazon.de/AZDelivery-NodeMCU-Development-Nachfolgermodell-ESP8266/dp/B074RGW2VQ/ref=sr_1_3?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&keywords=esp32&qid=1565008313&s=gateway&sr=8-3)
* wires to connect everything; for example: 6× Female-Female Jumper Wire, 0.14 mm² [🢂](https://www.amazon.de/ZOORE-120pcs-Multicolored-Female-Breadboard/dp/B07P85V1G3/ref=sr_1_5?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&keywords=jumper+male&qid=1565690543&s=industrial&sr=1-5)
* 1× USB Micro Cable [🢂](https://www.amazon.de/dp/B0778FV6K4/ref=sr_1_2?dchild=1&fst=as%3Aoff&qid=1586361990&refinements=p_89%3AGritin&rnid=669059031&s=computers&sr=1-2)



## <img src="./IMAGES/A.png" height="40"> Assembly

### Tutorial with images (Z-Stage)
This is the assembly guide for the Z-Stage.

1. Insert the motor into the motor-screw-coupling adapter.
<p align="center">
<img src="./IMAGES/Z_stage_assembly_02.jpg" width="300">
</p>

1. Insert the head of the M3×20 screw into the motor-screw-coupling adapter. Use pliers to press the screw inside.
<p align="center">
<img src="./IMAGES/Z_stage_assembly_03.jpg" width="300">
</p>

1.  Fix the head of the M3 screw inside the adapter using two M3 worm screws (This can also be done later, in case the screw becomes too wobbly.) You may fix the motor-end the same way, if needed.
<p align="center">
<img src="./IMAGES/Z_stage_assembly_04.jpg" width="300">
</p>


1.  That is how it looks like without the motor. The Z-stage will "wrap" around the Cube
<p align="center">
<img src="./IMAGES/Zstage.jpeg" width="300">
</p>

## Fully assembled

<p align="center">
<img src="./IMAGES/Zstagetower.jpeg" width="300">
</p>

<p align="center">
<img src="./IMAGES/Assembly2.png" width="700">
</p>

## Z-Stage in Action

The stage can be used with the new (v3) and old (v2) cubes!
One can also mount the objective in place where the sample usually moves. 

<p align="center">
<img src="./IMAGES/zstageinaction.gif" width="700">
</p>



## Safety
Be careful!
