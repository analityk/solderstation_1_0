# solderstation_1_0
gerbers, bom (my local supllier but manufacturer part number are present), future is add all code for full functionality

You may download gerbers, login to jlcpcb and here look at pcb without extracting files on your own PC. 

There is initial stage of PCB build, so arduino nano is here and some errors too, look at schematic and you can find solve at least one. 
As long as you will use one type of solder tips you may place one feedback resistor insead of two. 
Any byte of code are not released now (but prototype pcb work well). 
I want implement a bit better solution than PI(d) controller.

This circuit implement power voltage measurement, solder tip current (real time with actual voltage) measurement 
so it is able to estimate amout of delivery heat. 
It work in PWM mode with relatively slow clock - something like 4-10Hz. Each cycle have two phase - heating, 
during it ADC read current and voltage on tip, so can calculate amount of delivered energy, and second phase, 
during it ADC measure amplified signal from tip thermocouple. 
Knowing tip heat capacity and air heat losses it should be possible to calculate one additional heat streem - this one heat that is delivered to soldering point. It shall be implemented because thermocouple is near heatig elements but beetwent it and solder point is introduced some serious heat flow resistance and temperature fall.
So even if PI can get constant temp. of thermocouple the bigger solder point are not able to reach desired temp. 
This is main reason of rise of this project. 
