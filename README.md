# ESPHome / Home Assistant based Water Tank Distance Monitor for A0221AT

This repository contains the ESPHome configuration for **Tank-Z**, an ESP32-based water tank level monitor that uses a serial (UART) ultrasonic distance sensor to measure water levels and integrates seamlessly with Home Assistant. Device is A0221AT which is based on **UART Controlled output**.

## Features
- **ESP32 DevKit** board compatibility using the robust `esp-idf` framework.
- **Custom UART communication** logic to trigger and read clean distance data from the sensor.
- **Home Assistant API & OTA** support for secure updates and tracking.
- **Fallback Hotspot** configuration for easy troubleshooting if connection fails.


<img width="716" height="716" alt="AT" src="https://github.com/user-attachments/assets/b401f5e4-0696-4582-bfa1-7642ca8a4a50" />

## Product Datasheet
https://www.dypcn.com/uploads/A02-Datasheet.pdf

## Hardware Connections
- **Board:** ESP32 DevKit
- **Sensor RX Pin:** GPIO16 (Connects to Sensor TX)
- **Sensor TX Pin:** GPIO17 (Connects to Sensor RX)
- **Baud Rate:** 9600

## How to Use


1. Clone or copy the `tank-z.yaml` file into your ESPHome environment.
2. Open the file and replace the following placeholder values with your actual credentials:
   - `YOUR_HOME_ASSISTANT_API_ENCRYPTION_KEY`
   - `YOUR_OTA_PASSWORD`
   - `YOUR_WIFI_SSID`
   - `YOUR_WIFI_PASSWORD`
   - `YOUR_FALLBACK_HOTSPOT_PASSWORD`
  
## Hardware Stability Note
I connected a 100µF electrolytic capacitor and a 0.1µF ceramic capacitor in parallel between VCC and GND. This decoupling mechanism stabilizes the power supply and successfully prevents the sensor readings from jumping.

<img width="921" height="850" alt="Screenshot_56" src="https://github.com/user-attachments/assets/6c78b3bd-fde4-488c-b8ba-6e1f165d8a70" />

