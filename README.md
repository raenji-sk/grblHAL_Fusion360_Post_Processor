# grblHAL_Fusion360_Post_Processor
Experimental grblHAL post processor with canned cycles and 4th axis support for use with Autodesk Fusion 360

Added features and modifications:
1. Update coolant settings to support air(M7) and mist(M8) as well as vac on AUX0 on Teensy 4.1 BOB. M64 P0 to turn on and M65 P0 to turn off. Aux ports range P0 to P2.

2. Add spidnle delay to properties (dwell G4 Px - x is user adjustble (seconds)), after M3/M4 command (spindle CW/CCW), defalut 2 seconds, enough for Kress spindle

3. Arcs for XZ and YZ are disabled (add it as an option in the future?) grblHAL can not rotate them

4. Merge Canned cycles from LinuxCNC (needs testing) G81,G82,G83 as per grblHAL documentation. G83 and G73 work only when dwell is ZERO "0"

5. Add 4th Axis as a selectable option in PP settings. Must be in X axis direction. Simultaneous not supported. This too was merged from a LinuxCNC PP.

6. Add G73 Chip breaking - not tested

7. 18.05.2021 - add option for the A axis to be placed along X or Y (UCCNC/CNCDrive PP source)
   add 4th axis table / rotary option into PP settings

8. 19.05.2021 - fix 4 axis simultaneous operation


![image](https://user-images.githubusercontent.com/16104239/118820385-83385d80-b8b6-11eb-8ee4-f9a86a9279fd.png)
