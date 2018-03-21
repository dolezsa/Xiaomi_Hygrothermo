# Xiaomi_Hygrothermo

Home-assistant sensor platform for Xiaomi Mijia BT Hygrothermo temperature and humidity sensor.

## Usage

To use, add the following to your `configuration.yaml` file:

```
sensor:
  - platform: xiaomi_hygrothermo
    name: mijia ht #1
    mac: 'xx:xx:xx:xx:xx:xx'
    scan_interval: 60
```

- mac is required.
- default "scan" interval is every 30 seconds.

## Determine the MAC address

using hcitool:
```
$ sudo hcitool lescan
LE Scan ...
LE Scan ...
4C:65:A8:xx:xx:xx (unknown)
4C:65:A8:xx:xx:xx MJ_HT_V1
[...]
```

using bluetoothctl:
```
$ sudo bluetoothctl 
[NEW] Controller xx:xx:xx:xx:xx:xx homeqube [default]
[bluetooth]# scan on
Discovery started
[CHG] Controller xx:xx:xx:xx:xx:xx Discovering: yes
[NEW] Device 4C:65:A8:xx:xx:xx MJ_HT_V1
[bluetooth]# 
[bluetooth]# quit
```

look for MJ_HT_V1 devices...
