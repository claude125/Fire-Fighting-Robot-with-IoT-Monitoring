# Smart Fire Fighting Robot with IoT Monitoring

![Fire Fighting Robot](fire-robot.jpg)

An intelligent robotic system designed to automatically detect and extinguish fire while providing real-time monitoring through an IoT platform.

The robot uses **NodeMCU (ESP8266)** with flame sensors to detect fire and automatically activate a water pump to suppress the fire. The system also publishes environmental data and robot status to an **IoT dashboard for remote monitoring**.

---

# Project Motivation

Fire accidents can occur unexpectedly and often require firefighters to enter dangerous environments to control the fire and rescue victims. This exposes emergency responders to serious risks.

Inspired by the **Rusumo Border fire accident reported by The New Times on August 21, 2018**, this project proposes a **Smart Fire Fighting Robot** capable of automatically detecting fire and responding quickly without putting human lives in danger.

The system improves:

- Fire emergency response time
- Safety for firefighters
- Real-time situational awareness through IoT monitoring

---

# System Architecture


Flame Sensors → NodeMCU Controller → Fire Detection Logic → Water Pump Activation → IoT Monitoring Platform


---

# System Architecture Diagram

```mermaid
flowchart LR

A[Flame Sensors] --> B[NodeMCU ESP8266 Controller]
B --> C[Fire Detection Algorithm]
C --> D[Water Pump System]
B --> E[Water Level Sensor]
B --> F[IoT Cloud Platform]
F --> G[Monitoring Dashboard]
F --> H[Alert Notifications]

Key Features
Automatic Fire Detection

The robot uses flame sensors to detect the presence of fire.

Automatic Fire Suppression

When fire is detected, the system automatically activates a water pump to extinguish the fire.

IoT Monitoring

The system publishes real-time information to an IoT platform including:

fire detection status

robot operational status

water tank level

Remote Monitoring Dashboard

Users can monitor the robot through an online dashboard that displays live system data.

Alert Notifications

The system can send alerts when fire is detected.

Hardware Components

The robot is built using the following hardware:

NodeMCU (ESP8266)

Flame sensor module

Water pump

Water tank

Motor driver module

DC motors

Robot chassis

Water level sensor

Rechargeable battery

Software Components

The software architecture includes:

Embedded firmware for NodeMCU

Fire detection logic

IoT communication system

Monitoring dashboard

Technologies used:

Arduino IDE

Embedded C / C++

MQTT / IoT platforms (Blynk / ThingSpeak)

WiFi communication

Project Structure

smart-fire-fighting-robot
│
├── firmware
├── robot-control
├── iot-monitoring
├── hardware
├── images
│ ├── fire-robot.jpg
│ └── architecture.png
├── README.md

Applications

This system can be used in:

warehouses

factories

industrial facilities

residential buildings

airports

hazardous environments

Future Improvements

Future development may include:

AI-based fire detection using computer vision

autonomous navigation

thermal camera integration

multi-robot fire response systems

integration with emergency services

Author

Claude Dusengimana
Senior Network & Security Engineer | IoT Researcher
Kigali, Rwanda

LinkedIn
https://linkedin.com/in/dusengimana-claude
