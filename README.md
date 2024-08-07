
A collection of tips for the Sovol SV08 Printer.
Mostly derived from the Official Facebook Page [Sovol SV08 Official User Group] (https://www.facebook.com/groups/6997076173737632)

SV08 - Useful Tips

Motherboard Fan Loudness
On the 2.3.3 Firmware Sovol have put the wrong PIN to control the motherboard fan. 
it can be fixed and improved turning it into a Temperature controlled reaactive Fan.

> [!IMPORTANT]
> == Make Backups of any File you change! ==

Open Printer.cfg and replace the following Text.

[fan_generic fan3] # exhaust fan
pin: PA2
max_power: 1.0

With this text

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
