# BTT-SKR-mini-E3-V3.0---Creality-Ender-6
Modified Ender 6 with orbital extruder, btt skr E3 mini, BLtouch, and others

You can access the board schemattics on [https://github.com/bigtreetech/BIGTREETECH-SKR-mini-E3/blob/master/hardware/BTT%20SKR%20MINI%20E3%20V3.0/Hardware/BTT%20E3%20SKR%20MINI%20V3.0_PIN.pdf]

## The firt Thing to do
First check that your endstops are working in [mainsailos.locl] unthe machine at the bottom 
you can check if the endstops are working.
 ### BLtouch 
 the Make sure that the BLti contected to `sensor_pin: ^PC14 control_pin: PA1` the folow the guide on [BLtouch.md]

 The hat "^" is very inportant i spend a lot of time figuring out these, my BLtouch used to work fine with all the tests but 
 when the G28 command it didin deploy until i added the "^" befores "the PC14"

## Test your stepper mottors
Check the direction pin of the x and y, the boron guide is very usefull for these when you are trying a new board.
[https://docs.vorondesign.com/build/startup/]
For the SKR mini E3 V3 is the followwing Stepper X : dir_pin: PB12, Stepper Y: dir_pin: !PB2 and Stepper Z: dir_pin: PC5
## Configure off-set of probe. you can follow the guide of klipper
### First 
You need to manualy level the bed, you can use the klippler guide
[https://www.klipper3d.org/Manual_Level.html] is very usfull if you hava a bl touch because you can use it to adjust it.
you will have to first set the offset [https://www.klipper3d.org/Probe_Calibrate.html] then repet everything.
then you can use these
[screws_tilt_adjust]
screw1: -5, 30
screw1_name: front left screw
screw2: 155, 30
screw2_name: front right screw
screw3: 155, 190
screw3_name: rear right screw
screw4: -5, 190
screw4_name: rear left screw
horizontal_move_z: 10.
speed: 50.
screw_thread: CW-M3

The readjust the z offset

