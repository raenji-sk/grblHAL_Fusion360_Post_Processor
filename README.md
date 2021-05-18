# grblHAL_Post_Processor
Experimental grblHAL post processor with canned cycles and 4th axis support

Added features and modifications:
1. Update coolant settings to support air(M7) and mist(M8) as well as vac on AUX0 on Teensy 4.1 BOB. M64 P0 to turn on and M65 P0 to turn off. Aux ports range P0 to P2.

2. Add spidnle delay to properties (dwell G4 Px - x is user adjustble (seconds)), after M3/M4 command (spindle CW/CCW), defalut 2 seconds, enough for Kress spindle

3. Arcs for XZ and YZ are disabled (add it as an option in the future?) grblHAL can not rotate them

4. Merge Canned cycles from LinuxCNC (needs testing) G81,G82,G83 as per grblHAL documentation. G83 and G73 work only when dwell is ZERO "0"

5. Add 4th Axis as a selectable option in PP settings. Must be in X axis direction. Simultaneous not supported. This too was merged from a LinuxCNC PP.

6. Add G73 Chip breaking - not tested

7. 18.05.2021 - add option for the A axis to be placed along X or Y (UCCNC/CNCDrive PP source)


![image](https://user-images.githubusercontent.com/16104239/118500835-6bcb6a00-b728-11eb-8ea1-cbe9dddd7482.png)
