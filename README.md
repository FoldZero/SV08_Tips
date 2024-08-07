# SV08 - Useful Tips
A collection of tips for the Sovol SV08 Printer.
Mostly derived from the Official Facebook Page 
-  [SOVOL SV08 Facebook Group](https://www.facebook.com/groups/sovol.sv08) 

## First Steps

> [!IMPORTANT]
> == Make Backups of any File you change! ==

### Calibrate the printer
- Run a Pid tune for the Bed and Extruder
- Home the Printer
- Calibrate the Z-Offset
- Install Orca Slicer
- Run a Temperature Tower to familiarise yourself with the speeds and flows capable, every filament has potential to be different.
- Run a Test Print

## Motherboard Fan Loudness
On the 2.3.3 Firmware Sovol have put the wrong PIN to control the motherboard fan. 
it can be fixed and improved turning it into a Temperature controlled reaactive Fan.

Credit John Hansknecht and Video here - https://www.youtube.com/watch?v=t3RJ5DbOdcs&ab_channel=JohnHansknecht

Open Printer.cfg and replace the following Text.
```
[fan_generic fan3] # exhaust fan
pin: PA2
max_power: 1.0
```

With this text

```
[temperature_fan fan3]
pin: PA1
kick_start_time: 0.5
max_power: 1.0
min_temp: 0
max_temp: 90
hardware_pwm: true
target_temp: 60
sensor_type: temperature_host
max_speed: 1.0
min_speed: 0.1
control: pid
pid_Kp: 2.0     ;40
pid_Ki: 5.0     ;0.2
pid_Kd: 0.5     ;0.1
pid_deriv_time: 2.0
```


## Printhead Upgrades

## SPARTACUS The Toolhead

https://www.printables.com/model/745412-spartacus-the-toolhead

## Stealthburner Conversion

Description: Convert your SV08 to use the Voron Stealthburner printhead
STL Files: Printables - SV08 Stealthburner Conversion
Guide: YouTube - SV08 Stealthburner Mod

BambuLab X1 Hotend Adapter

Description: Adapter to use the BambuLab X1 hotend on the SV08
STL Files: Printables - BambuLab X1 Hotend Adapter for SV08


# Profiles
## PrusaSlicer
- **Description**: Pre-configured profiles for PrusaSlicer specifically for the SOVOL SV08.
- **GitHub Link**: [SV08 PrusaSlicer Profiles](https://github.com/user/SV08-PrusaSlicer-Profiles) *(Placeholder link, replace with actual if available)*


### Mainline Firmware
- **Description**: Enhanced firmware for improved performance and additional features.
- **GitHub Link**: [Sovol-SV08-Mainline](https://github.com/Rappetor/Sovol-SV08-Mainline)

  
### Bambu Nozzle on Your Sovol SV08!

- stl - [Sovol SV08 Bambulab Hotend Support](https://www.printables.com/model/942453-sovol-sv08-bambulab-hotend-support)
Credit Nadir [Printables]
- Video - [Bambu Nozzle on Your Sovol SV08!](https://www.youtube.com/watch?v=mqC7Y-PyLHw&ab_channel=3DPrintedObjects)
Credit 3D Printed Objects [yt]
