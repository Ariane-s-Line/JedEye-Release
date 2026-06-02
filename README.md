# JedEye-Release

Public firmware releases for the **JedEye** cave-surveying device.

Each entry on the [Releases page](https://github.com/Ariane-s-Line/JedEye-Release/releases) ships:

- **`firmware.bin`** — the over-the-air (OTA) update image, served automatically to devices over WiFi.
- **`firmware-manual-install.uf2`** — a ready-to-flash image for manual USB install.
- Notes describing what's new.

## Update over WiFi (recommended, v2.6+)

From v2.6.0 the JedEye updates **itself over WiFi** — no cable, no file copying.

1. Make sure the JedEye can reach a WiFi network with internet (a phone hotspot is fine).
2. On the device, go to **OPTIONS → SETTINGS → SYSTEM → OTA UPDATE**.
3. If a newer version is available it is shown — tap **Confirm** to download and install.
   A progress bar runs and the JedEye reboots into the new firmware on its own.

The JedEye also checks automatically whenever you switch WiFi on, and offers the
update if one is available. When needed, the radio (NINA) firmware is updated in
the same step. After installing, the device shows a **What''s New** page with the
release highlights on the first boot (also viewable any time from **System Info**).

> Updates are safe: the device only switches to the new firmware once it has
> received a complete, valid image, so an interrupted download cannot brick it.

## Manual install over USB (fallback)

1. Download **`firmware-manual-install.uf2`** from the
   [latest release](https://github.com/Ariane-s-Line/JedEye-Release/releases/latest).
2. Connect the JedEye to your computer over USB.
3. On the device, go to **OPTIONS → SETTINGS → SYSTEM → UPDATE → Confirm**. The
   JedEye reboots into update mode and a drive named **RPI-RP2** appears on your computer.
4. Drag the `.uf2` file onto that drive. The device reboots automatically into the new firmware.

> Some updates also need a one-time radio refresh via
> **OPTIONS → SETTINGS → SYSTEM → RADIO FW UPDATE** — the release notes say when this is required.

## About JedEye

JedEye is a handheld instrument for cave surveying, measuring distance, heading,
inclination and temperature in a single shot. It runs on an Arduino Nano RP2040
Connect and talks to survey apps (e.g. TopoDroid) over Bluetooth, or serves its
own web interface over WiFi. It is optimized for use with the
[Ariane](https://www.arianesline.com/) cave-surveying software.

This repository hosts **release builds only**. The firmware source code lives in
a separate repository.

---

<sub>`manifest.txt` in this repo is generated automatically from the latest
release and tells devices which firmware to fetch over the air — there is no need
to edit it by hand.</sub>