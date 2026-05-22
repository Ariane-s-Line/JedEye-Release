# JedEye-Release

Public firmware releases for the **JedEye** cave-surveying device.

Each release on the [Releases page](https://github.com/Ariane-s-Line/JedEye-Release/releases)
ships a ready-to-flash `firmware-<version>.uf2` together with notes describing
what's new for users.

## Install / update the firmware

1. Download the latest `firmware-<version>.uf2` from the
   [Releases page](https://github.com/Ariane-s-Line/JedEye-Release/releases/latest).
2. Connect the JedEye to your computer over USB.
3. On the device, go to **OPTIONS → SETTINGS → SYSTEM → UPDATE → Confirm**. The
   JedEye reboots into update mode and a drive named **RPI-RP2** appears on your
   computer.
4. Drag the `.uf2` file onto that drive. The device reboots automatically into
   the new firmware.

> After some updates you may also need to refresh the device's radio module
> once via **OPTIONS → SETTINGS → SYSTEM → RADIO FW UPDATE**. The release notes
> say when this is required.

## About JedEye

JedEye is a handheld instrument for cave surveying, measuring distance, heading,
inclination and temperature in a single shot. It runs on an Arduino Nano RP2040
Connect and talks to survey apps (e.g. TopoDroid) over Bluetooth, or serves its
own web interface over WiFi. It is optimized for use with the
[Ariane](https://www.arianesline.com/) cave-surveying software.

This repository hosts **release builds only**. The firmware source code lives in
a separate repository.
