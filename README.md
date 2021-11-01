# SmartThings-Edge

Edge drivers for the SmartThings platform.

WARNING:
SmartThings Edge is still in beta status, and only recommended to developers and advanced users at the moment.


## Install/uninstall via the web UI

Enroll, install, uninstall and unenroll via https://api.smartthings.com/invitation-web/accept?id=00770d41-65e6-4110-949d-f19d6df139e8.


## Install/uninstall with SmartThings CLI

### Install

0. Download the SmartThings CLI for your platform: https://github.com/SmartThingsCommunity/smartthings-cli/releases

0. Using SmartThings CLI, enroll to my SmartThings Edge Drivers channel

    ./smartthings edge:channels:enroll --channel 2d9568d4-da3e-4b3b-9178-626d122e5d7e

0. Install the driver of your choice, from my channel to your hub

    ./smartthings edge:drivers:install --channel 2d9568d4-da3e-4b3b-9178-626d122e5d7e

### Uninstall

To uninstall a driver from your hub:

    ./smartthings edge:drivers:uninstall


## Add the device to your hub

After installation, simply start a discovery from the SmartThings app to add your device.
If it is already paired, make sure to remove it from the SmartThings app first, then start the discovery.


## Check that the Edge driver is the actual driver used

When an Edge driver exists, it should automatically be selected even though your device may be supported natively or with a Groovy Device Handler.
However, to make sure the Edge driver is in use, open your device in the SmartThings app and check that the menu now has a "Driver" entry.
If you want to revert from the Edge driver back to a Groovy Device Handler, you first need to uninstall the Edge driver.
