# ESP32-S3 PCB Design with Temperature Sensor and RGB LED

## Overview

This project focuses on designing a custom PCB using the **ESP32-S3-MINI-1-N8** microcontroller. The PCB integrates an **ENS210** temperature and humidity sensor, a **WS2812B RGB LED** for visual feedback, and a power regulation system using the **TLV75801 LDO** voltage regulator. The design also includes **TVS protection diodes** for USB input safety.

The PCB was designed using **KiCad** and is tailored for applications that require environmental sensing and LED indication, powered through USB with proper surge protection.

## Features

- **ESP32-S3-MINI-1-N8**: A powerful microcontroller for managing sensors, RGB LED, and communication.
- **ENS210 Temperature & Humidity Sensor**: Provides accurate temperature and humidity readings.
- **WS2812B RGB LED**: Addressable LED for visual indication based on temperature readings.
- **TLV75801 LDO Regulator**: Provides a stable 3.3V output from the USB 5V input.
- **USB Surge Protection**: Includes **D3V3XA4B10LP TVS diodes** for protecting the USB input from overvoltage or surge.

## Schematic Design

The schematic was created using **KiCad** and includes the following blocks:

1. **ESP32-S3 Microcontroller**: 
   - Handles the processing and communication.
   - I²C interface to the ENS210 sensor.
   - GPIO control for the WS2812B RGB LED.

2. **ENS210 Temperature & Humidity Sensor**:
   - Connected via the I²C bus.
   - Powered by 3.3V from the regulator.

3. **WS2812B RGB LED**:
   - Data pin connected to GPIO48 of the ESP32.
   - Powered by the 3.3V rail.

4. **TLV75801 LDO**:
   - Regulates 5V USB input to a stable 3.3V output for all components.

5. **TVS Diodes**:
   - Protect the USB power input from surges.

## PCB Layout

The PCB layout includes:

- **Compact design**: Minimizes the space required while keeping all components well-organized.
- **Optimized power and ground planes**: Ensures stable operation and reduces noise.
- **Via stitching**: Improves ground plane integrity.
- **Thermal relief pads**: Used for better heat dissipation where needed.
- **USB Input Protection**: TVS diodes are placed near the USB input to provide surge protection.

# STATUS: ONGOING
