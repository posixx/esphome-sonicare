# ESPHome package for Philips Sonicare Bluetooth-enabled toothbrushes

## Package roots and Thanks
First of all I'd like to thank @v6a and @iamjosh, cause this package is a fork of @v6a' package, which is based on @iamjosh' original code.

## What is it?
This package provides a support of Philips Sonicare Bluetooth-enabled toothbrushes for any ESP32 based device, which supports a Ble-connectivity (esp32_ble_tracker conponent).
Following sensors are currently supported:
1. Connection status
2. Battery level
3. Active time
4. Current status (Off, Standby, Run, Charge, Shutdown, Validate, LightsOut)
5. Selected mode (Clean, White+, Gum Health, Deep Clean)
6. Selected strength (1, 2, 3)
7. Brush head installed (Adaptive Clean, Adaptive White, Tongue Care, Adaptive Gums, N/A)

All these sensors could be used in Home Assistant as part of Esphome intergration.
