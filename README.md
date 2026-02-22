# ESPHome Redodo BMS Monitor (via BLE)

This project allows you to monitor a **Redodo 24V 100Ah LiFePO4 Battery** (or any JBD-based BMS) using an ESP32 and ESPHome via Bluetooth Low Energy (BLE).

## Features
* 📊 Real-time Total Voltage & Current monitoring.
* 🔋 State of Charge (SOC) and Cycle count.
* 🌡️ Temperature monitoring.
* 🧬 Individual Cell Voltage reporting (8 cells for 24V).

## Hardware
* **ESP32** (DevKit V1 or similar).
* **Redodo 24V 100Ah LiFePO4 Battery** with integrated Bluetooth.

## How to use
1. Copy `secrets.yaml.example` to `secrets.yaml`.
2. Fill in your WiFi credentials and the **MAC address** of your BMS.
3. Flash the ESP32:
   ```bash
   esphome run esp_redodo_bms.yaml

## Credits & Acknowledgments
* This project is based on the [BMS_BLE-HA](https://github.com/patman15/BMS_BLE-HA/) repository by **patman15**.
* Technical architecture, security hardening (secrets management), and documentation assisted by **Gemini (Google AI)**.