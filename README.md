# Xiomi_Hygrothermo
Home-assistant sensor platform for Xiaomi Mijia BT Hygrothermo temperature and humidity sensor

## Usage
```
sensor:
  - platform: xiaomi_hygrothermo
    name: mijia ht #1
    mac: 'xx:xx:xx:xx:xx:xx'
    scan_interval: 60
```

mac is required.

default "scan" isterval is every 30 seconds.
