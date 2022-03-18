<p align="center">
  <a href="https://github.com/oxystin/homebridge-fibaro"><img src="https://raw.githubusercontent.com/oxystin/homebridge-fibaro/main/img/fibaro-device.png" width="540"></a>
</p>

<span align="center">

# Homebridge Fibaro
[![npm](https://badgen.net/npm/dt/homebridge-fibaro?color=purple)](https://www.npmjs.com/package/homebridge-fibaro) 
[![npm](https://badgen.net/npm/v/homebridge-fibaro?color=purple)](https://www.npmjs.com/package/homebridge-fibaro)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/oxystin/homebridge-fibaro.svg)](https://github.com/oxystin/homebridge-fibaro/pulls)
[![GitHub issues](https://img.shields.io/github/issues/oxystin/homebridge-fibaro.svg)](https://github.com/oxystin/homebridge-fibaro/issues)

Homebridge plugin for Fibaro Home Center

</span>


## Installation

Install this plugin by running:

```
npm install -g homebridge-fibaro
```


## Configuration

Remember to configure the plugin in config.json in your home directory inside the .homebridge directory. Configuration parameters:

- Required parameters:
  - `platform` - Always "FibaroHC".
  - `name` - Plugin name as displayed in the homebridge log.
  - `host` - IP address (or hostname) of the Fibaro Home Center machine. Ignored if `url` is present.
  - `url` - URL of the Fibaro Home Center machine. **Example:** https://hc-00000XXX.local
  - `username` - Username for accessing Fibaro Home Center machine.
  - `password` - Password for accessing Fibaro Home Center machine.
- Optional parameters:
  - `pollerperiod` - Polling interval for querying Fibaro Home Center machine (**0**: disabled, **7**: seconds is the default).
  - `excludeDeviceID` - Device IDs to be excluded from homekit.


## config.json

```json
"platforms": [
    {
        "platform": "FibaroHC",
        "name": "Fibaro",
        "host": "192.168.1.100",
        "url": "https://hc-00000XXX.local",
        "username": "admin",
        "password": "***********",
        "pollerperiod": 10,
        "excludeDeviceID": [
            145,
            146,
            215,
            216
        ]
    }
]
```
Look for a sample config in [config.json example](https://github.com/oxystin/homebridge-fibaro/blob/master/config.json)

## Release notes:

### 1.3.1
- [FIX] Using ca.cer for https URLs only
- [NEW] Support for garage door opener additonal states (opening, closing, stopped)
- [NEW] Added support to Nice roller shutters

### 1.3.0
- [FIX] Dimmer issue when controlling device from Homekit
- [NEW] New mode start debugging
- [NEW] Added a new options (excludeDeviceID) that allows you to exclude selected devices from Homekit
- [NEW] Ability to add Carbon Dioxide Sensor for devices of type 'com.fibaro.multilevelSensor' (it is necessary to fill in the "User Description" field in the Fibaro interface)