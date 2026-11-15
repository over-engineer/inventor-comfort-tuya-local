# Inventor Comfort dehumidifier profile for Tuya Local

An unofficial device profile for the **Inventor Comfort dehumidifier**, for use with [Tuya Local](https://github.com/make-all/tuya-local) in Home Assistant.

The profile was tested on one Inventor Comfort unit with **Tuya Local 2026.10.0**. Compatibility with other variants or firmware versions is unverified.

## What the profile exposes

| Control                                    | Home Assistant entity               | Details                                                              |
|--------------------------------------------|-------------------------------------|----------------------------------------------------------------------|
| Power, humidity setpoint, current humidity | Humidifier (dehumidifier)           | Setpoint 35–80% in 5% steps, plus current humidity                   |
| Fan speed                                  | Select                              | Low, Medium, High                                                    |
| Dehumidification mode                      | Select                              | Manual, Smart Dehumidification, Clothes Dry, Sleep Mode              |
| Operation                                  | Select                              | Dehumidifier, Air Purifier, Dehumidifier & Air Purifier              |
| Auto louver swing                          | Switch (also the fan's oscillation) |                                                                      |
| Ionizer                                    | Switch                              |                                                                      |
| UV                                         | Switch                              |                                                                      |
| Light indications                          | Select                              | Air humidity indication off, All indications off, All indications on |
| Mute device sounds                         | Switch                              |                                                                      |
| Child lock                                 | Lock                                |                                                                      |
| Timer                                      | Select                              | cancel, 1h–8h                                                        |
| Tank full                                  | Binary sensor                       |                                                                      |
| Problem                                    | Binary sensor (diagnostic)          | Reports other fault codes                                            |

## Installation

1. Install [Tuya Local](https://github.com/make-all/tuya-local) in Home Assistant.
2. Copy `inventor_comfort_dehumidifier.yaml` into `custom_components/tuya_local/devices/` under your Home Assistant configuration directory.
3. Restart Home Assistant.
4. Add the dehumidifier in Tuya Local, and select **Inventor Comfort (`inventor_comfort_dehumidifier`)** when asked for the device type.

Each user supplies their own device connection details (device ID, IP address and local key) in Home Assistant. None are included in this repository.

For more information on how to add an Inventor device to Home Assistant, see the [Inventor A/C integration thread](https://community.home-assistant.io/t/inventor-a-c-integration/1013278) on the Home Assistant Community forum.

For more on how profiles work, see the [Tuya Local device profile documentation](https://github.com/make-all/tuya-local/blob/main/custom_components/tuya_local/devices/README.md).

## Credits and license

This profile was adapted from Tuya Local's [Woods WDD90 dehumidifier profile](https://github.com/make-all/tuya-local/blob/main/custom_components/tuya_local/devices/wood_wdd90_dehumidifier.yaml). It's distributed under the MIT license from the upstream [make-all/tuya-local](https://github.com/make-all/tuya-local) project. See [`LICENSE.md`](LICENSE.md).
