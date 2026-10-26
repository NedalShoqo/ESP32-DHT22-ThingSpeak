# ESP32 Environmental Monitoring with ThingSpeak

A simple IoT demonstration that turns temperature and humidity measurements into live, cloud-based charts. The project combines an **ESP32**, a **DHT22 sensor**, and **ThingSpeak** to show how sensor readings can move from a microcontroller to an online dashboard.

## Project at a Glance

| | |
| --- | --- |
| **Microcontroller** | ESP32 |
| **Sensor** | DHT22 (temperature and humidity) |
| **Development environment** | Wokwi simulator / Arduino framework |
| **Connectivity** | Wi-Fi |
| **Cloud platform** | ThingSpeak |
| **Update interval** | Approximately 25 seconds |

## System Overview

```text
   DHT22 Sensor
   Temperature + Humidity
           |
           v
        ESP32
   Read and process values
           |
           v
       Wi-Fi
   Send measurements
           |
           v
       ThingSpeak
   Store data and plot trends
```

Screenshots of the **Wokwi circuit**, **ThingSpeak graphs**, and **successful Serial Monitor output** are also used to document the result.

<img width="1010" height="179" alt="image" src="https://github.com/user-attachments/assets/49c7b26d-105d-43c6-a99f-29eb338e3a4e" />
<img width="1261" height="409" alt="image" src="https://github.com/user-attachments/assets/2ac9fe86-12cc-4a0e-a646-fdb0e45e6fff" />


## Wokwi
<img width="755" height="509" alt="image" src="https://github.com/user-attachments/assets/268fd08c-9144-4926-8c36-4d06247cd747" />
<img width="1249" height="776" alt="image" src="https://github.com/user-attachments/assets/7744ac6e-f982-44d0-938e-1e4c24c817a0" />

## What the Project Demonstrates

- **Sensor acquisition:** The ESP32 reads temperature and relative humidity from the DHT22.
- **Wireless connectivity:** The board establishes a Wi-Fi connection for cloud communication.
- **Remote data logging:** Measurements are periodically transmitted to ThingSpeak.
- **Live visualization:** Two time-series charts present the readings as they arrive.
- **Basic monitoring:** Changes in the simulated environment can be observed remotely.

## Hardware and Services

- ESP32 development board
- DHT22 temperature and humidity sensor
- Jumper wires (or virtual connections in Wokwi)
- Wi-Fi connection
- ThingSpeak channel with two enabled data fields

## Cloud Data Mapping

| ThingSpeak field | Measurement | Unit |
| --- | --- | --- |
| Field 1 | Temperature | °C |
| Field 2 | Relative humidity | % |

Each successful update creates a new entry in the ThingSpeak channel. As more entries arrive, the charts illustrate how the measured values change over time.

## Typical Operation

1. The ESP32 starts and establishes a Wi-Fi connection.
2. The DHT22 provides temperature and humidity readings.
3. The program checks that the readings are valid.
4. Both values are sent to the corresponding ThingSpeak fields.
5. The next reading is taken after the configured interval.
6. The dashboard displays the received measurements on separate charts.

## Learning Outcomes

This project provides hands-on practice with digital sensors, ESP32 programming, Wi-Fi networking, cloud-based IoT services, periodic data transmission, and time-series visualization.

## Useful Resources

- [Wokwi - Online Electronics Simulator](https://wokwi.com/projects/478940200841296897)
- [ThingSpeak - IoT Analytics Platform](https://thingspeak.mathworks.com/channels/3551364)
---


## Student Information

- **Name:** Nedal Shoqo
- **University ID:** 12217300
- **Project:** ESP32 to ThingSpeak (IoT LAB #1)

*An educational IoT project exploring the path from physical sensing to cloud visualization.*
