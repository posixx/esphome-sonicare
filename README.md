# ESPHome package for Philips Sonicare Bluetooth-enabled toothbrushes

## Package roots and Thanks
First of all I'd like to thank [@v6a](https://github.com/v6ak) and [@iamjosh](https://github.com/iamjoshk) for the job, they've already done. This package is a fork of [@v6a's package](https://github.com/v6ak/esphome-collection/blob/main/packages/sonicare.yaml), which is based on [@iamjosh's original code](https://github.com/iamjoshk/home-assistant-collection/tree/main/ESPHome/Sonicare).

## What is it?
This package provides a support of Philips Sonicare Bluetooth-enabled toothbrushes for any ESP32-based device, which supports a Ble-connectivity (esp32_ble_tracker conponent). It also addresses some issues happening with original versions like connection stability and add some extra sensors.

Following sensors are currently supported:
1. Connection status
2. Battery level
3. Active time
4. Current status (Off, Standby, Run, Charge, Shutdown, Validate, LightsOut)
5. Selected mode (Clean, White+, Gum Health, Deep Clean)
6. Selected strength (1, 2, 3)
7. Brush head installed (Adaptive Clean, Adaptive White, Tongue Care, Adaptive Gums, N/A)

All these sensors could be used in Home Assistant as part of Esphome intergration.

## How to use it?
### Prerequisites:
1. Your Esp32 device supports Bluetooth Low Energy connection
2. "esp32_ble_tracker" component is added to your yaml-config for a esp32 device

### Installation
1. In oder to use this package you need to add it as a remote package or download it and add it as a local package.
2. Provide required variables:
   - mac: "00:00:00:00:00:00" (BLE-Mac address of you Sonicare toothbrush)
   - id: "my_brush"
   - name: "My Brush"

Here is an example with a remote package:
```
packages: 
  brush_1:
    url: https://github.com/andrecall/esphome-sonicare
    files:
      - path: packages/sonicare.yaml
        vars:
         mac: "00:00:00:00:00:00"
         id: "my_brush"
         name: "My Brush"
```

Further information about ESPHome packages you can find at [ESPHome website](https://esphome.io/components/packages.html)
