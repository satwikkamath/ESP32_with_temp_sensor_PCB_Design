# ESP32-S3 with Temperature Sensor, RGB LED, and Power Regulation

## Overview

This project uses an **ESP32-S3-MINI-1-N8** microcontroller to interface with an **ENS210** temperature and humidity sensor and a **WS2812B RGB LED**. The power supply is regulated by the **TLV75801 LDO**, and the USB input is protected using **D3V3XA4B10LP TVS diodes**. 

## Components Used

- **ESP32-S3-MINI-1-N8**: Microcontroller for controlling all components.
- **ENS210 Temperature & Humidity Sensor**: Reads temperature and humidity values via I²C.
- **WS2812B RGB LED**: Displays colors based on the temperature sensor readings.
- **TLV75801 LDO**: Regulates the input voltage to 3.3V for the ESP32-S3 and other components.
- **D3V3XA4B10LP TVS Diode**: Protects the USB power input from surges.
- **USB4105 Connector**: Used for powering the circuit via USB.

## Features

- **Temperature and Humidity Monitoring**: Real-time temperature and humidity readings using the ENS210 sensor.
- **RGB LED Control**: The WS2812B LED shows different colors based on temperature values.
  - Blue for cold temperatures.
  - Green for moderate temperatures.
  - Red for hot temperatures.
- **USB Surge Protection**: The D3V3XA4B10LP diodes protect the USB input from voltage surges.
- **Stable Power Supply**: The TLV75801 regulates 5V input to 3.3V for the ESP32-S3 and sensors.

## Hardware Setup

1. **ENS210 Sensor**:
   - SCL (I²C Clock) → GPIO5
   - SDA (I²C Data) → GPIO6
   - 3.3V power → 3V3 pin on ESP32
   - GND → GND on ESP32

2. **WS2812B RGB LED**:
   - Data In → GPIO48
   - 3.3V power → 3V3 pin on ESP32
   - GND → GND on ESP32

3. **Power Supply**:
   - 5V from USB regulated to 3.3V using TLV75801 LDO.
   - USB protected by D3V3XA4B10LP TVS diodes.
