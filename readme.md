TinyG Introduction
========

![TinyG v6 Board](http://farm7.staticflickr.com/6080/6138119387_c6301797dd.jpg)

TinyG is a port of grbl to the Atmel xmega that runs on the TinyG hardware. Some differences are:

* 6 axis motion (XYXABC axes)
* jerk controlled motion for acceleration planning (3rd order motion planning)
* status displays ('?' character)
* XON/XOFF protocol over serial
* config is necessarily different to take into account the larger number of settings

See these websites for more details.

* [Synthetos](https://www.synthetos.com/)
* [TinyG Wiki](http://www.synthetos.com/wiki/index.php?title=Projects:TinyG)
* [TinyG Github](https://github.com/synthetos/TinyG)



CURRENT VERSION
========
The current master version is 0.93.1 (Fanny Pack)
Changes in this version include:

MAJOR FEATURES IN 0.93.1
* [Homing cycles added - G28.1](http://www.synthetos.com/wiki/index.php?title=Projects:TinyG-Homing)
* [Return to home added - G28](http://www.synthetos.com/wiki/index.php?title=Projects:TinyG-Homing)
* Multiple work coordinate systems added - G54, G55, G56, G57, G58, G59 as per [NIST rs274NGCv3 specification](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.141.2441)
* Coordinate system offset support added - G92 as per [NIST rs274NGCv3 specification](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.141.2441)
* [Feedhold and cycle(re)start added (! and ~ respectively)](http://www.synthetos.com/wiki/index.php?title=Projects:TinyG-Gcode-Support#Starting.2C_Stopping.2C_Feedhold_and_Rate_Overrides_-_Design_Notes)
* [Software reset command added (control-X command)](http://www.synthetos.com/wiki/index.php?title=Projects:TinyG-Gcode-Support#Starting.2C_Stopping.2C_Feedhold_and_Rate_Overrides_-_Design_Notes)
* [TinyG JSON Support added](http://www.synthetos.com/wiki/index.php?title=Projects:TinyG-JSON)
* [Configuration has changed](http://www.synthetos.com/wiki/index.php?title=TinyG:Configuring) 
* [Support for spindle control added - M3,M4,M5](http://www.synthetos.com/wiki/index.php?title=Projects:TinyG-Gcode-Support#Gcode_Language_Support)
* [Support for coolant control added - M7,M8,M9](http://www.synthetos.com/wiki/index.php?title=Projects:TinyG-Gcode-Support#Gcode_Language_Support)

MINOR FEATURES AND INTERNALS IN 0.93.1
* Status reports are now configurable via JSON command
* Arcs are now planned through the line planner
* Help display updated (type $h)
* Self tests added (type $test)
* Restore settings to defaults command added (type $defaults)
* Configuration and display sub-system compeletly re-written for flexibilioty and to handle JSON

BUG FIXES IN 0.93.1
* Issues #5, #7 and #12 - Issues were found and fixed that affected positional accuracy with some combinations of settings (fixed since 0.93)
* Issue #10 - Help display error fixed
* Issue #8 - $xTR did not update until reset
* Fixed some typos in command strings (fixed since 0.93)

If you have feature requests or find any bugs please log them in the Issues tab on the github


