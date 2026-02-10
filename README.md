# Satellite RauSAT-2.0

RauSAT-2.0 is an educational CubeSat-standard nanosatellite prototype developed to demonstrate
environmental monitoring, wireless data transmission, and ground station visualization using
low-cost open-source hardware.

---

## Project Overview

The RauSAT-2.0 project was developed by the student of Nazarbayev Intellectual School
(Kyzylorda, Kazakhstan) as an applied research project in the field of aerospace engineering
and environmental monitoring.

The satellite prototype is designed to collect real-time environmental and positional data,
transmit it via radio communication, and visualize the received information at a ground station
through a web-based interface.

---

## Mission Objectives

- Measure environmental parameters:
  - Temperature
  - Atmospheric pressure
  - Altitude
  - Illumination level
- Determine satellite position and speed using GPS
- Transmit sensor data via nRF24L01 radio communication
- Receive and process data at a ground station
- Visualize real-time data on a web dashboard
- Enable further data delivery to external services (e.g., Telegram bot)

---

## System Architecture

### Satellite Segment
- Arduino Nano (ATmega328)
- BMP180 temperature and pressure sensor
- BH1750 light intensity sensor
- MPU6050 accelerometer and gyroscope
- HMC5883 magnetometer
- NEO-6M GPS module
- nRF24L01+PA+LNA radio module
- Solar panels and battery system

### Ground Station
- ESP32 / ESP8266 microcontroller
- nRF24L01 radio receiver
- Wi-Fi communication
- Embedded web server for data visualization

---

## Repository Structure

RauSAT-2.0/

│
├── satellite/

│ └── satellite_firmware.ino # On-board satellite firmware (Arduino)

│
├── ground_station/

│ └── ground_station.ino # Ground station firmware (ESP32 / ESP8266)

│
├── docs/

│ └── RauSAT_2.0_Report.pdf # Full technical report and documentation

│
└── README.md

---

## Principle of Operation

1. On-board sensors collect environmental and GPS data
2. Data is packed into arrays by the Arduino Nano
3. Information is transmitted via radio communication
4. The ground station receives radio packets
5. Data is processed and displayed on a web interface
6. Data can be forwarded to external services

---

## Documentation

A detailed description of the system architecture, hardware selection, schematics,
3D models, experiments, and results is available in the GitHub documentation:

Documentation_RauSat 2.0.pdf

A 3-minute overview video explaining the satellite's mission and development process:
https://www.youtube.com/watch?v=wAqawTeeiBA




