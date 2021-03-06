# homebridge-controllerlink
Provides a link for the [HomeBridge Controller](https://github.com/kraigm/homebridgecontroller) app to [HomeBridge](https://github.com/nfarina/homebridge)

This repository contains the HomeBridge Controller Link plugin for homebridge, which allows the HomeBridge Controller app a way to interact with your homebridge, no matter where on the local network it is installed. For more information, please see the main [GitHub repo](https://github.com/kraigm/homebridgecontroller).


# Installation

1. Install homebridge using: npm install -g homebridge
2. Install this plugin using: npm install -g homebridge-controllerlink
3. Update your configuration file. See sample-config.json snippet below. 


# Configuration

Configuration sample:

 ```
"platforms": [
		{
			"platform": "HomeBridgeControllerLink",
			"restartStyle": "respawn",
			"disableAutoRestart": false,
			"disableLogger": false
		}
	],

```
"restartStyle" - Optional config to specify how the restart should be handled:
    - "respawn" (default) : Spawns a new instance of homebridge when restarted
    - "stopOnly" : Only shutsdown and then exits with exitCode 1
"disableAutoRestart" - Optional config that can disable auto restarting homebridge when an unhandled error occurs (which will cause homebridge to crash)
"disableLogger" - Optional config that can disable the automatic file logging as well as the streaming of the logs
