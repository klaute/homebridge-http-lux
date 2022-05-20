# homebridge-http-lux2

It is a fork of https://github.com/epadillac/homebridge-http-lux/fork

Increased maximum light level, updated serial number and disabled some log messages.
Added info log message of the read light value.

Supports http ambient light sensor devices on the Homebridge platform. Additional hardware required.
This is a modified version of the https://github.com/metbosch/homebridge-http-temperature plugin.
This version only supports the light sensor. MAX lightlevel is set to 800.

# Installation

1. Install homebridge using: npm install -g homebridge
2. Install this plugin using: npm install -g homebridge-http-lux2
3. Update your configuration file. See sample-config.json in this repository for a sample.

# Configuration


Configuration sample file:

 ```
 "accessories": [
     {
         "accessory": "HttpLux2",
         "name": "Ambient Light Level",
         "url": "http://192.168.0.20/api/lightlevel",
         "http_method": "GET"
     }
 ]

```


The defined endpoint will return a json looking like this
```
{
	"lightlevel": 450
}
```


This plugin acts as an interface between a web endpoint and homebridge. You will need additional hardware to expose the web endpoints with the light level information. I built my Temperature, Humidity and Light Sensor on the NodeMCU board with Arduino IDE.
