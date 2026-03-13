<div align="center">

![header](https://capsule-render.vercel.app/api?type=waving&color=0:0d0000,50:1a0500,100:ff4500&height=200&section=header&text=Smart%20Fire%20Fighting%20Robot&fontSize=40&fontColor=ffffff&fontAlignY=38&desc=IoT-Powered%20Autonomous%20Fire%20Detection%20%26%20Suppression%20System&descSize=15&descAlignY=58&animation=fadeIn)

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=14&pause=1500&color=FF6B35&center=true&vCenter=true&width=700&height=40&lines=🔥+Autonomous+Fire+Detection+%26+Suppression;📡+Real-Time+IoT+Monitoring+Dashboard;🤖+NodeMCU+ESP8266+Powered+Robot;💧+Automatic+Water+Pump+Activation;🛡️+Protecting+Lives+%7C+Inspired+by+Rusumo+2018)](https://git.io/typing-svg)

<br/>

![NodeMCU](https://img.shields.io/badge/NodeMCU-ESP8266-00979D?style=for-the-badge&logo=arduino&logoColor=white)
![Arduino](https://img.shields.io/badge/Arduino_IDE-00979D?style=for-the-badge&logo=arduino&logoColor=white)
![MQTT](https://img.shields.io/badge/MQTT-Protocol-660066?style=for-the-badge&logo=eclipse-mosquitto&logoColor=white)
![IoT](https://img.shields.io/badge/IoT-Monitoring-ff4500?style=for-the-badge&logo=thingsboard&logoColor=white)
![C++](https://img.shields.io/badge/Embedded_C++-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![WiFi](https://img.shields.io/badge/WiFi-Communication-1BA0D7?style=for-the-badge&logo=wifi&logoColor=white)

</div>

---

## 🔥 Project Overview

> *"Inspired by the **Rusumo Border fire accident** — The New Times, August 21, 2018 — a tragedy that exposed emergency responders to life-threatening conditions."*

Fire accidents strike without warning and routinely force firefighters into deadly environments. This project answers that challenge with an **autonomous robotic system** that detects, responds to, and suppresses fires — without putting a single human life at risk.

![Fire Fighting Robot](robotic.JPG)

The robot uses a **NodeMCU (ESP8266)** paired with flame sensors to detect fire and immediately activate a water pump for suppression, while simultaneously publishing live status data to an **IoT monitoring dashboard** for remote situational awareness.

---

## 🎯 What This System Solves

| Problem | Solution |
|---|---|
| ⚠️ Firefighters entering dangerous zones | 🤖 Autonomous robot handles first response |
| ⏱️ Slow emergency reaction time | ⚡ Instant sensor-triggered suppression |
| 👁️ No remote situational awareness | 📊 Live IoT dashboard with real-time data |
| 🔔 No early warning system | 🚨 Automated fire alerts on detection |

---

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                  SMART FIRE FIGHTING ROBOT                  │
├─────────────┬──────────────┬──────────────┬─────────────────┤
│  DETECTION  │   CONTROL    │  ACTUATION   │   MONITORING    │
│             │              │              │                 │
│ 🔥 Flame    │ NodeMCU      │ 💧 Water     │ 📡 MQTT Broker  │
│   Sensors   │ ESP8266      │   Pump       │                 │
│             │              │              │ 📊 IoT Dashboard│
│ 💧 Water    │ Fire Logic   │ ⚙️  DC Motors │   (Blynk /     │
│   Level     │ Algorithm    │   + Driver   │   ThingSpeak)   │
│   Sensor    │              │              │                 │
│             │              │ 🚨 Alerts    │ 🔔 Push Alerts  │
└─────────────┴──────────────┴──────────────┴─────────────────┘
```

**Data Flow:**
```
Flame Sensors → NodeMCU Controller → Fire Detection Logic
      ↓                                       ↓
Water Level Sensor              Water Pump Activation
      ↓                                       ↓
      └──────────→ IoT Platform ←─────────────┘
                       ↓
              Remote Dashboard + Alerts
```

---

## ✨ Key Features

<table>
<tr>
<td width="50%">

### 🔍 Automatic Fire Detection
Flame sensors continuously scan the environment. The moment fire is detected, the system triggers the response pipeline instantly — no human intervention needed.

</td>
<td width="50%">

### 💧 Automatic Fire Suppression
On detection, the water pump activates immediately to suppress the fire. The robot navigates toward the source using motor-driven wheels for targeted response.

</td>
</tr>
<tr>
<td width="50%">

### 📡 Real-Time IoT Monitoring
Publishes live system telemetry including fire detection status, operational state, and water tank level to a cloud dashboard accessible from anywhere.

</td>
<td width="50%">

### 🚨 Alert Notifications
Push notifications are sent the instant fire is detected. Stakeholders can monitor status and receive alerts without being physically present.

</td>
</tr>
</table>

---

## 🔧 Hardware Components

```bash
$ cat hardware/bill_of_materials.txt
```

| Component | Role |
|---|---|
| **NodeMCU ESP8266** | Main microcontroller + WiFi communication |
| **Flame Sensor Module** | Infrared-based fire detection |
| **Water Pump** | Fire suppression actuator |
| **Water Tank** | Suppression agent reservoir |
| **Water Level Sensor** | Tank monitoring |
| **Motor Driver Module (L298N)** | DC motor speed & direction control |
| **DC Motors (x2)** | Robot locomotion |
| **Robot Chassis** | Structural frame |
| **Rechargeable Battery** | Portable power supply |

---

## 💻 Software Stack

```bash
$ cat firmware/dependencies.json
```

```json
{
  "ide"          : "Arduino IDE",
  "language"     : "Embedded C / C++",
  "protocol"     : "MQTT",
  "iot_platform" : ["Blynk", "ThingSpeak"],
  "communication": "WiFi (ESP8266)",
  "features"     : [
    "Fire detection logic",
    "Motor control algorithms",
    "IoT data publishing",
    "Remote dashboard integration",
    "Push alert system"
  ]
}
```

---

## 📁 Project Structure

```
smart-fire-fighting-robot/
│
├── 📂 firmware/
│   ├── robot-control/         # Motor & navigation logic
│   └── iot-monitoring/        # MQTT publishing & dashboard sync
│
├── 📂 hardware/
│   ├── schematics/            # Circuit diagrams
│   └── bill_of_materials.txt  # Components list
│
├── 📂 images/
│   ├── robotic.JPG            # Robot photo
│   └── architecture.png       # System diagram
│
└── 📄 README.md
```

---

## 🌍 Applications

This system is deployable in any fire-risk environment:

`🏭 Factories` &nbsp; `🏪 Warehouses` &nbsp; `✈️ Airports` &nbsp; `🏠 Residential Buildings` &nbsp; `⚗️ Labs` &nbsp; `☢️ Hazardous Facilities`

---

## 🚀 Future Improvements

```python
roadmap = [
    "🧠 AI-based fire detection using computer vision",
    "🗺️  Autonomous navigation with obstacle avoidance",
    "🌡️  Thermal camera integration for better detection",
    "🤖 Multi-robot coordinated fire response",
    "🚒 Direct integration with emergency services",
    "🔋 Solar-powered extended operation",
]
```

---

## 👤 Author

<div align="center">

**Claude Dusengimana**
*Senior Network & Security Engineer | IoT Researcher*
📍 Kigali, Rwanda

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/dusengimana-claude)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-161b22?style=for-the-badge&logo=github&logoColor=white)](https://github.com/claude125)
[![Gmail](https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:dusenge125@gmail.com)

</div>

---

<div align="center">

![footer](https://capsule-render.vercel.app/api?type=waving&color=0:ff4500,50:1a0500,100:0d0000&height=100&section=footer&text=Built+to+save+lives&fontSize=16&fontColor=ffffff&fontAlignY=65&animation=fadeIn)

*⭐ Star this repo if it inspired you — every star helps push this research forward.*

</div>
