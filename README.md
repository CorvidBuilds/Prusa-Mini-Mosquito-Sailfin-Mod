# Prusa Mini Mosquito Sailfin Mod
Direct Drive Extruder Mounting Option for Prusa Mini
![Assembly](https://github.com/CorvidBuilds/Prusa-Mini-Mosquito-Sailfin-Mod/blob/main/images/Assembly.png)
I've been using 4nthonylin's [Mosquito Mount](https://www.prusaprinters.org/prints/36643-prusa-mini-mosquito-mount) and [Fan Shroud](https://www.prusaprinters.org/prints/37368-prusa-mini-mosquito-fan-shroud) mods for a long time and I've wanted to experiment with direct drive extruders for almost as long. I considered putting [Annex Engineering's Sherpa Mini](https://www.prusaprinters.org/prints/32331-prusa-mini-z-axis-bottom-redesign) using [athlon789789's mount](https://www.prusaprinters.org/prints/66519-prusa-mini-sherpa-extruder-direct-drive-conversion) but [CroXY's Sailfin](https://github.com/CroXY3D/Sailfin-Extruder) looked funnier. After some tinkering, I have created these two mounts.

I've been using this without issue since January 2022.

# List of modifications
The Mosquito mount was modified by:

- Removing two nut retainers.
- Removed M6 threading.
- Moved relief to the other side of the feeder hole.

The Sherpa Mini mount was modified by

- Aligning output of extruder with hot end.
- Widening the top plate for said alignment.
- Shortening the overall height by ~3mm.
- Adding a cutout to clear the Z Carriage.

This mount should fit both the Sherpa Mini and the Sailfin (using the Mid_Sherpa_Mount.stl).

# Instructions
- PTFE Length: 40.5mm 
# Klipper Config
Always confirm configurations will work for your system. The below is an example from what works on my Prusa Mini with the Buddy controller board and an LDO 36STH20-1004AHG.
```
#### Sailfin
[extruder]
step_pin: PD9
dir_pin: !PD8
enable_pin: !PD10
microsteps: 32
rotation_distance: 23.5976 
gear_ratio: 50:10
full_steps_per_rotation: 200	#200 for 1.8 degree, 400 for 0.9 degree
nozzle_diameter: 0.400
filament_diameter: 1.750
## Confirm your own thermistor config
# heater_pin: PB1
# sensor_type: ATC Semitec 104GT-2
# sensor_pin: PC0
max_extrude_only_velocity: 70
max_extrude_only_accel: 1500
min_temp: 10
max_temp: 305
## Confirm your own PA values
# pressure_advance = 0.028
# pressure_advance_smooth_time: 0.030
```