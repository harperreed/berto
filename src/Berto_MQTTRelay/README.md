# Berto MQTT Relay

The Berto MQTT Relay driver provides a connection to any simple MQTT relay device. You can define the topic and message values for opening, closing and causing a query state message to be published. The driver can also subscribe to state topic messages so the driver can receive realtime open and close events. Messaging to and from the driver is managed by the [Berto MQTT Bridge](../../src/Berto_MQTTBridge/README.md).

The Berto MQTT Bridge needs to be installed in your project.

## Properties

* Open Relay Publish Message - The Topic and Value to publish to open the relay eg. cmnd/relay/0 OPEN.
* Open Relay State Message - The Topic and Value message received to show the when the relay is opened.
* Close Relay Publish Message - The Topic and Value to publish to close the relay eg. cmnd/relay/0 CLOSE.
* Close Relay State Message - The Topic and Value message received to show the when the relay is closed.
* Query State (Seconds) - The number of seconds betwen publishing a query message to get the state of the device, setting to 0 will disable polling.
* Query Relay Publish Message - The Topic and Value to publish to trigger the relay to publish it's state eg. cmnd/relay/0 QUERY.
* Status - Shows the connection status to the MQTT Bridge.

## Connections

The driver has 1 standard relay connection that can be connected to relay devices. The [Berto Relay Light](../../src/Berto_RelayLight/README.md) can be used to add simple On/Off lights.

## Licence

[DM](../../LICENSE.md)