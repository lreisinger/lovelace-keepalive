# lovelace-keepalive

Keep connection to Home Assistant server alive even when the display of the device is off for some time.

Tablets running Fully Kiosk or similar have the issue, that after 6 - 7 minutes of screensaver the connection to Home Assistant is dropped and some lovelace cards have to be reloaded when the dashboard becomes visible again.
This is because Chromium marks the tab as inactive and suspends javascript execution after some time. 

This integration simply plays a silent audio file in the background which keeps the tab active.

## Installation
via [HACS](https://hacs.xyz/)

## How to use
Add '?keepalive' (or '&keepalive' if other parameters are already in the url) to the dashboard url 
### Examples:
```
http://homeassistant.local:8123/tablet-livingroom/0?keepalive
http://homeassistant.local:8123/tablet-livingroom/0?kiosk&keepalive
```