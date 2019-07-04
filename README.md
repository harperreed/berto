# Berto Control4 Drivers

A collection of Control4 drivers providing integration using various technologies along with other ancillary drivers. The [Berto_Cloud](src/Berto_Cloud/README.md) should be installed first and is required for all other Berto drivers to function. The default service and subcription levels allows a single instance of any Basic level drivers to function in your project. A Premium level subcription is available that provides addtional drivers and extended features of some of the other drivers.

All Berto driver C4Z files are available for download at https://berto.io/c4z and should be installed by a Control4 dealer with Composer Pro. Should you require remote installation of any Berto driver you can also email support@berto.co.uk.

The Berto Cloud driver also provides a programming action to send simple email messages and execute system commands on the local controller eg. to cleanly shutdown the controller in the event of a power cut or reboot.

## Installation
Download the [Berto Cloud](c4z/Berto_Cloud.c4z) driver and copy to your Control4 Drivers directory. Once installed all other available Berto drivers can be installed from the Properties page by selecting the driver and room and then the Install option from the Management Action property. 

All Berto drivers require OS 2.10.0 or above.

## Drivers

### Integration

* [Berto_Cloud](src/Berto_Cloud/README.md) - Master Berto driver which manages all installs and updates of the Berto drivers. The driver provides integration to MQTT brokers allowing the sending and receiving of IoT messages. The driver also provides the ability to send emails using the Berto email service.

* [Berto_MQTTBridge](src/Berto_MQTTBridge/README.md) - Provides connection to MQTT brokers and IoT devices eg. Sonoff Relay, Homekit Bridge.

* [Berto_LifxBridge](src/Berto_LifxBridge/README.md) - Provides integration to Lifx devices on the local network without the need for an Internet connection or access to the Lifx Cloud. 

* [Berto_MQTTRelay](src/Berto_MQTTRelay/README.md) - A simple MQTT Relay driver that allows connection to any MQTT controlled relay device.

* [Berto_SonoffRelay](src/Berto_SonoffRelay/README.md) - Sonoff 4 Channel Relay driver for the Standard and Pro model.

* [Berto_ShellyRelay](src/Berto_ShellyRelay/README.md) - Shelly Relay driver for the Shelly1, Shelly1PM, Shelly 2.5 and Shelly 4 Pro relays.

* Berto_Assist - Provides integration to the Google Home Assistant service. (Premium subscription only, please email support@berto.co.uk for details).

* [Berto_Pushover](src/Berto_Pushover/README.md) - Provides integration to the Pushover messaging service.

* [Berto_IFTTT](src/Berto_IFTTT/README.md) - Provides integration to the IFTTT Webhooks service.

* [Berto_OwnTracks](src/Berto_OwnTracks/README.md) - Provides integration to an OwnTracks location service.

* [Berto_ABGateway](src/Berto_ABGateway/README.md) - Provides integration to the April Beacon Gateway V4.0.

* [Berto_Hub](src/Berto_Hub/README.md) - Provides integration to the Homekit and Flic Buttons via the Berto Hub.

* [Berto_HomeAssistant](src/Berto_HomeAssistant/README.md) - Provides integration to Home Assistant.

* [Berto_Mail](src/Berto_Mail/README.md) - Provides integration to most mail servers including SSL and TLS support.

### Lighting

* [Berto_ShellyLight](src/Berto_ShellyLight/README.md) - Shelly Light driver for the Shell RGBW2 LED dimmer.

* [Berto_LifxBulb](src/Berto_LifxBulb/README.md) - Provides integration of Lifx bulbs with the Berto Lifx Bridge.

* [Berto_RelayLight](src/Berto_RelayLight/README.md) - Simple On/Off Light driver that connects to a standard relay.

* [Berto_TuyaDimmer](src/Berto_TuyaDimmer/README.md) - Tuya Dimmer Compatible drvers for dimmers running Tasmota firmware with module 54.

### Audio & Video

* [Berto_Humax_DTR-2000T](src/Berto_Humax_DTR-2000T/README.md) - IR driver for the Humax Youview+ HD TV Recorder.

* [Berto_SkyQ](src/Berto_SkyQ/README.md) - IP driver for the Sky Q & Sky Q Mini Boxes.

* [Berto_Kodi](src/Berto_Kodi/README.md) - IP driver for the for the Kodi Media Player.

* [Berto_NowTV](src/Berto_NowTV/README.md) - IP driver for the for the Now TV Player.

* [Berto_BenQ](src/Berto_BenQ/README.md) - IP driver for the for the BenQ range of projectors.

### Other

* [Berto_Profile](src/Berto_Profile/README.md) - Provides user profile configuration used by other Berto drivers.

* [Berto_Scene](src/Berto_Scene/README.md) - Provides simple device grouping and media control for use with the Berto Assist driver or direct from programming.

* [Berto_BeaconManager](src/Berto_BeaconManager/README.md) - Provides management of beacon gateways to beacon devices.

* [Berto_ButtonBeacon](src/Berto_ButtonBeacon/README.md) - Provides button state updates from beacons which are availabe in programming.

* [Berto_ProximityBeacon](src/Berto_ProximityBeacon/README.md) - Provides proximity updates from beacons which are availabe in programming.

* [Berto_TemperatureBeacon](src/Berto_TemperatureBeacon/README.md) - Provides temperature updates from beacons which are availabe in programming.

* [Berto_FlicButton](src/Berto_FlicButton/README.md) - Provides button state updates from Flic buttons which are availabe in programming.

## Licence & Privacy Policy

[Licence Agreement](LICENSE.md)

[Privacy Policy](PRIVACY.md)