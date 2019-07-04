# Berto Scene

The Berto Scene driver creates a virtial scene that can be used by [Berto Assist](../../src/Berto_Scene/README.md).

Scenes can also be turned on, off or toggled from programming using the ON, OFF and TOGGLE commands.

The driver uses the Room Contol driver to manage media devices and can also activate and deactivate other devices within the project.

## Properties

* Room Control Device - The Room Control device that the scene will use.
* Preset - The Room Control Preset number to turn on when the scene is activated.
* Scene Devices - The devices that the scene will turn on when activated and off when deactived.
* Invert Scene Devices - The devices that the scene will turn off when activated and on when deactived.

## Programming

### Events

* ACTIVATE - Event triggered when the scene is activated
* DEACTIVATE - Event triggered when the scene is deactivated

## Release Notes

### v1 - 2019-04-17

- Initial Release

## Licence

[DM](../../LICENSE.md)