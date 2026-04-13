# ESPHome JBD (Redodo / PowerQueen) BMS Monitor (BLE)

This project provides a robust ESPHome integration for monitoring **Redodo LiFePO4 batteries** and other **JBD-based BMS** (Jiabaida) via Bluetooth Low Energy. It is compatible with both **12V and 24V** configurations.

## Supported Hardware
* **Batteries**: Redodo & PowerQueen 12V/24V LiFePO4 with Bluetooth, or any battery using JBD BMS.
* **Controller**: ESP32 (DevKit V1, WROOM, etc.) - Bluetooth is required.

## Features
* 📊 **Dynamic Cell Monitoring**: Automatically reports voltage for each cell (4S for 12V, 8S for 24V).
* 🔋 **Full Battery Stats**: Total Voltage, Current, SOC (%), and Cycle count.
* 🌡️ **Health & Safety**: Temperature monitoring and BMS status.
* 🛠️ **Diagnostics**: Integrated Web Interface for standalone monitoring without Home Assistant.

## How to use
1. Copy `secrets.yaml.example` to `secrets.yaml`.
2. Fill in your WiFi credentials and the **MAC address** of your BMS.
3. Flash the ESP32:
   ```bash
   esphome run esp_redodo_bms.yaml

## 🏠 Integration
* **Home Assistant**: Automated discovery via the native ESPHome API.
* **Other Systems**: Supports MQTT, Prometheus, and REST API for integration with Node-RED, OpenHAB, or custom dashboards.
* **Standalone**: Real-time dashboard available via the ESP32's web interface (IP address).

## Credits & Acknowledgments
* This project is based on the [BMS_BLE-HA](https://github.com/patman15/BMS_BLE-HA/) repository by **patman15**.
* Technical architecture, security hardening (secrets management), and documentation assisted by **Gemini (Google AI)**.
* Support for SOH (State of Health) and full capacity monitoring added by **aiolos**.
* Verified compatibility with PowerQueen 24V batteries (thanks to **aiolos**).