# homebridge-fibaro

Homebridge plugin for Fibaro Home Center. Based on [homebridge-fibaro-home-center](https://github.com/ilcato/homebridge-fibaro-home-center) code.

# Installation

Install this plugin by running:
```
npm install -g homebridge-fibaro
```
or use the terminal to install the developer version:
```
npm install --save https://github.com/oxystin/homebridge-fibaro.git#dev
```
    
# Configuration
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

Look for a sample config in [config.json example](https://github.com/oxystin/homebridge-fibaro/blob/master/config.json)