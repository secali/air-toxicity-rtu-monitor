<div align="center">

# 🏭 Air Toxicity Industrial RTU Monitor

**Autonomous Remote Terminal Unit (RTU) for multi-gas atmospheric toxicity sensing and automated hazard alerting.**

[![Hardware](https://img.shields.io/badge/Hardware-Arduino%20Uno%20%2F%20Mega-00979D?logo=arduino&logoColor=white)](https://www.arduino.cc/)
[![Language](https://img.shields.io/badge/Language-C%2B%2B-00599C?logo=c%2B%2B&logoColor=white)](https://isocpp.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

</div>

---

## 📌 Problem Statement & Solution

In industrial and enclosed environments, the silent buildup of toxic gases poses immediate safety risks. 

This project implements an **embedded RTU (Remote Terminal Unit)** utilizing microcontrollers, gas sensor arrays (MQ series), and multi-stage actuators to provide:
1. Continuous atmospheric sampling and PPM threshold calculation.
2. Immediate hardware-level acoustic/optical alarms upon limit breach.
3. Automated relay triggering for forced ventilation extraction systems.

---

## 🔌 Circuit & Hardware Setup

```text
[ Gas Sensors (MQ-x) ] ──(Analog In)──> [ Arduino RTU ]
                                              │
                    ┌─────────────────────────┴─────────────────────────┐
                    ▼                                                   ▼
         [ Optical/Buzzer Alarms ]                         [ Relay Exhaust Actuators ]
```

---

## 📄 License

MIT License © [Sergio Cañete (secali)](https://github.com/secali)
