# Berto Tuya Dimmer

The Berto Tuya Dimmer driver allows control of a [Tuya Compatible Dimmer](https://www.aliexpress.com/item/Tuya-App-remote-control-LED-light-dimmer-switch-wifi-dimming-panel-switch-110V-220V-google-home/32946757894.html) running [Tasmota](https://github.com/arendst/Sonoff-Tasmota) firmware.  There are numerous dimmers that all use the Tasmota firmware module 54 for which this driver is designed to work with. Messaging to and from the device is managed by the [Berto MQTT Bridge](../../src/Berto_MQTTBridge/README.md).

The Berto MQTT Bridge needs to be installed in your project.

## Properties

* Topic - The topic name setup on the dimmer.
* Firmware - Tasmota firmware version.
* MAC Address - MAC Address of dimmer.
* IP Address - IP Address of dimmer.
* State - Current power state of light
* Level - The bright level when in White mode (0 -100)
* Status - MQTT connection status

## Licence

[DM](../../LICENSE.md)