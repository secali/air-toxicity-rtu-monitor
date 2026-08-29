# 🏭 Industrial Air Toxicity RTU Monitor

[![C++](https://img.shields.io/badge/C%2B%2B-Embedded-00599C?style=flat-square&logo=cplusplus&logoColor=white)](https://isocpp.org/)
[![Arduino](https://img.shields.io/badge/Hardware-Arduino%20Uno-00979D?style=flat-square&logo=arduino&logoColor=white)](https://www.arduino.cc/)
[![Sensors](https://img.shields.io/badge/Sensors-MQ--Series%20Gas-FF4500?style=flat-square)](#)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)

> **Cyber-physical Remote Terminal Unit (RTU) for real-time hazardous gas detection, PPM threshold evaluation, and autonomous acoustic/visual emergency actuation.**

---

## 🎯 Overview

Designed for industrial safety and enclosed environment monitoring, this project implements a standalone embedded RTU node capable of sampling analog gas sensors (MQ series for Carbon Monoxide, LPG, and toxic smoke), computing moving-average PPM concentrations, and triggering immediate fail-safe actuators when danger thresholds are breached.

### 🌟 Key Capabilities
- **Real-Time Sampling Loop**: Continuous ADC sensor reading with rolling average calibration to filter out environmental noise.
- **Multi-Level Threshold Alarms**:
  - 🟢 **Normal**: Green LED heartbeat telemetry.
  - 🟡 **Warning**: Yellow LED pulse & logging alert.
  - 🔴 **Hazard (Critical)**: Continuous Red strobe, piezo buzzer siren, and relay cut-off trigger.
- **Hardware Schematic & Circuit Specs**: Includes complete wiring diagram and documentation.

---

## 🔌 Hardware Architecture & Pinout

```
  [ MQ-2 / MQ-7 Gas Sensor ] ───( Analog In A0 )───┐
                                                   ▼
                                        [ Arduino Uno / Nano ]
                                        ( Firmware: sketch.ino )
                                                   │
     ┌──────────────────┬──────────────────────────┼─────────────────────────┐
     ▼                  ▼                          ▼                         ▼
[ Green LED ]      [ Yellow LED ]             [ Red LED ]             [ Piezo Buzzer ]
( Pin 8 - OK )     ( Pin 9 - Warn )           ( Pin 10 - Alert )      ( Pin 11 - Siren )
```

---

## 🚀 Getting Started

1. Open `sketch.ino` in the **Arduino IDE** or **PlatformIO**.
2. Connect your Arduino board via USB and configure the target COM port.
3. Review PPM threshold constants in the header of `sketch.ino`.
4. Compile and upload firmware to the microcontroller.
5. Open Serial Monitor at **9600 baud** to view live telemetry and sensor PPM readouts.


---

## 👨‍💻 Author & Professional Profile

**Sergio Cañete Linares**  
*Senior QA Automation Engineer (SDET) | Software Developer in Test & AI-Driven Testing*

Specializing in scalable test automation architectures, microservices API testing, event-driven systems (Kafka), custom MCP servers, and multi-agent AI testing orchestration.

- 💼 **LinkedIn**: [linkedin.com/in/secali](https://www.linkedin.com/in/secali)
- 🐙 **GitHub**: [@secali](https://github.com/secali)
- 📧 **Email**: [sergio13896@gmail.com](mailto:sergio13896@gmail.com)
- 📍 **Location**: Spain
