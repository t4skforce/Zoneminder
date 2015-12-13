# Zoneminder IP-Camera control scripts
IP-Camera control scripts

## Add protocol file Wanscam HW0025
```
cd /usr/share/perl5/ZoneMinder/Control/
wget https://github.com/t4skforce/Zoneminder/raw/master/WanscamHW0025.pm
chmod +x ./WanscamHW0025.pm
```

## Add Protocol in ZoneMinder
###Enable PTZ Support on ZoneMinder**
```
Options > System > OPT_CONTROL: Tick
```

###Add the Control Type
Click on edit and add a new control with these details:

**Main**
```
Name:WANSCAM HW0025
Type:Remote
Protocol: WanscamHW0025
Can Wake:Tick
Can Sleep:Tick
Can Reset:Tick
```

**Move**
```
Can Move:Tick
Can Move Diagonally:Tick
Can Move Continuous:Tick
```

**Pan**
```
Can Pan:Tick
values to 0 (eg. Min/Max Pan Range)..
```

**Tilt**
```
Can Tilt:Tick
values to 0 (eg. Min/Max Tilt Range)..
```

**Zoom**
```
Can Zoom:Tick
Can Zoom Relative:Tick
values to 0 (eg. Min/Max Zoom Range)..
```

**Preset**
```
Has Presets:Tick
Num Presets:16
Has Home Preset:Tick
Can Set Presets:Tick
```

## Configure your Camera
Edit > Control

```
Controllable:Tick
Control Type:WANSCAM HW0025
Control Device:loginuse=admin&loginpas=
Control Address:192.168.1.111:99
Auto Stop Timeout:0.0
```

