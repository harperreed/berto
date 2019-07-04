# Berto Cloud

The Berto Cloud driver is the master driver for all other Berto drivers. The driver provides integration services to MQTT brokers that is used by other Berto drivers. 

In order to see all available drivers and gain additional features you need to create a Berto account which your system is linked to. To create an account you must first enter your email address in the Email Address property then take the "Create or Verify account" action from the Actions tab. This will generate a Link Code whish is emailed to your email address. Enter code in the "Enter Link Code" action. If you do not have an account one will be created for you automatically otherwise your existing account will be found using your email address. 

Linking your system to an account is optional but not required for the Basic level Berto drivers to be installed. When you system is linked to an account the Mnu poerpty will be available which, at base seerver level, provides a Service menu.

The Service menu provides 3 addtional options :-

* System Check In - Login in to the Berto Clound service to retrieve the drivers available for your system along with your service and subscription levels.
* List Available Drivers - List the available drivers for you system. This will show the subscription required for the driver and the URL to download the driver from.
* Upgrade All Drivers - Upgrade all Berto installed drivers to the latest release.

You can also setup an [OpenVPN](https://openvpn.net) server on your system and can then set individual clients up to access your network using the [Berto_Profile](../../src/Berto_Profile/README.md) driver. The OpenVPN server listens on UDP port 2194 so you will need to configure a port forward NAT on your router to point to your this port on your system. The OpenVPN server requires Service Level 1 or above.

To enable the OpenVPN server you first need to create a configration using the Reset option under Menu proeprty. Once the configuration has been created it can be enabled and disabled from the Enable Remote Access property or the UI button on any Navigator screen.

## Properties

* System Id - System Identifiaction address ued when setting up external services such as IFTTT and Google Assistant.
* Service Level - System service level which defines the features active across the Berto platform for your system.
* Email Address - Email address used as From address when sending emails and also by the account registation service.
* Account - Account code associated with the system. Configured from the Actions tab.
* Subscription Level - Subscription level associated with the system (Basic or Premium).
* Subscripotion Expiry - Date the systems subscription is due to expire. (Premium only).
* Notification - System notifcation messages.
* Enable Berto Dynamic DNS - Creates a bertio.io hostname entry in the Berto DNS for use with the OpenVPN server in the event you do have not a static IP address or your own dynamic DNS service. The hostname created will be used in the OpenVPN client configurations.
* Berto Dynamic DNS Hostname - Display only field showing the Berto DNS hostname created.
* Hostname - The external hostname or IP address to be used for the OpenVPN server if not using the Berto Dynamic DNS service.
* Remote Access Network - This is the subnet used by the OpenVPN server. Clients are issued IP addresses from this subnet when they connect. Requires Service Level 1 or above.
* Enable Remote Access - Start/Stop the Remote Access Server. (Service Level 1+ only).
* Enable Watchdog - Starts a watchdog timer in background that monitors the system specifically the state of the "director" process and in the event that the system becomnes unresponsive the "director" is restarted. (Service Level 1+ only).
* Menu - Provides additional features based on the Service and Subscriptions Levels of the system. You need to create an account and link you system to it for the menu to be available.
	
	
## Actions

* Create Or Verify Account - Start an account verification with the Berto Cloud services. A 4 digit link code with be sent to the email address setup in Properties which is to be used in the Enter Link Code action.
* Enter Link Code - Entering the link code received in the email verification will associate the system to your account.


## Programming

### Events

* Selected - Event triggered when the UI button is selected from any Navigator screen

### Actions

* EXECUTE_COMMAND - Allows the execution of any system command on the local controller eg. reboot to reboot or halt to shutdown system.
* SEND_MAIL - Sends a simple email message using the Berto mail server.

## Release Notes

### v1 - 2018-12-13

- Initial Release

### v2 - 2019-02-11 

#### Added

- New command to send email notifications using the Berto mail server.

### v3 - 2019-03-14

#### Changed

- Changed SMTP authentication to use StartTLS submission protocol when connecting to Berto SMTP mail relay server.

### v4 - 2019-03-16

#### Added

- Added Enable Remote Access property.
- Both the status of the Watchdog and Remote Access properties are retained following a reboot and started automatically if enabled.

### v5 - 2019-03-17

#### Added

- Added hidden control binding to query status of Berto drivers.

### v6 - 2019-03-30

#### Fixed

- Issue with 2.10.5 systems not supporting C4:url function and causing the Cloud driver to intermittently stop connecting to MQTT brokers and Websocket servers for other drivers. Systems running 2.10.5 or below will need to update the driver from Compsoer Pro using the Update option.

### v7 - 2019-05-21

#### Added

- Email address added to be used as From address when senbding emails via the Berto Mail service.

### v8 - 2019-06-11

#### Changed

- Disabled use of the Watchdog Timer and Remote Accesss Server. This will stop an update to the /etc/crontabs/root being made. After updating to this version of the driver you will need to manually remove the "berto.sh" in /etc/crontabs/root and do a killall crond to refresh.

### v9 - 2019-06-12

#### Changed

- Disabled use of the Watchdog Timer and Remote Accesss Server. This will stop an update to the /etc/crontabs/root being made. After updating to this version of the driver you will need to manually remove the "berto.sh" in /etc/crontabs/root and do a killall crond to refresh.

### v10 - 2019-06-15

#### Added

- Added Service Level property to distinguish between public and private systems and the features activated.
- Disabled email notifications for public systems with a base service level.

### v11 - 2019-06-18

#### Changed

- Removed Management Action and associated proeprties as no longer required.
- Added Menu poperty based on the Service Level assigned to the system. (Service Level 1+ only).

### v12 - 2019-06-28

#### Added

- Added Subscription Level property. Defaults to Basic subscription which allows unlimited use of one instance of Basic level drivers.


## Licence

[DM](../../LICENSE.md)