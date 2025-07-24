
# 🚰 Tank Storage Control System (TSCS) – SCADA Simulation in TIA Portal

A complete SCADA simulation project for a liquid storage and transfer system, developed using Siemens TIA Portal v15.1 and WinCC RT Advanced. This project models a smart fluid distribution network with centralized priority logic, operator controls, alarm safety features, and real-time SCADA monitoring — ideal for automation portfolios or academic demonstrations.

---

## 📚 Table of Contents

- [🚀 Project Overview](#-project-overview)
- [📦 Features](#-features)
- [🏗️ System Architecture](#️-system-architecture)
- [🛠️ Installation](#-installation)
- [▶️ How to Run](#️-how-to-run)
- [🧰 Technologies & Requirements](#-technologies--requirements)
- [📁 Project Structure](#-project-structure)


---

## 🚀 Project Overview

This project simulates an automated **tank storage control system** with multiple storage units (reservoirs) and a central high-capacity master reservoir. The system controls pumps and valves to maintain levels and distribute fluids intelligently. With full HMI/SCADA visualization, alarm handling, and operator access management, it replicates an industrial environment.

---

## 📦 Features

- 🔄 **Automated Liquid Management** with reservoir prioritization
- 🔐 **User Access Roles**: Admin and Operator control levels
- 📡 **Real-Time Monitoring** with WinCC Runtime Advanced
- 🚨 **Dynamic Alarm System** with pop-ups and blinking indicators
- 📈 **Trend Chart** for fluid level visualization
- ✋ **Manual Overrides** through HMI faceplates
- 🛡️ **Safety Interlocks** to prevent overpressure and faults

---

## 🏗️ System Architecture

- **Reservoirs**: 3 Secondary Tanks (140, 150, 160), 1 Main Tank (170)
- **Sensors**: Analog level transmitters (4-20 mA)
- **Actuators**: 
  - Inlet/Outlet Solenoid Valves (SV1x01 / SV1x02)  
  - Pumps (Pump110A, Pump770A, Pump771A)
- **HMI Screens**:
  - Login Interface
  - Storage Overview
  - Individual Tank Screens
  - Trend & Alarm Views

---

## 🛠️ Installation

### Requirements

- Siemens TIA Portal v15.1+
- WinCC RT Advanced
- Windows 10 or 11 (64-bit)
- Factory I/O (optional for 3D simulation)

### Setup

```bash
git clone https://github.com/yourusername/Liquid-Storage-Control-System.git
````

1. Open TIA Portal and load:

   * `SCADA_project.ap15_1`
2. (Optional) Import PLCM archive from:
   `AdditionalFiles/PLCM/plcmArchive.pma15_0`
3. Simulate with PLCSIM or deploy to a real S7-1200 controller.
4. Launch WinCC Runtime to run the HMI.

---

## ▶️ How to Run

### Login

| Role          | Username     | Password    |
| ------------- | ------------ | ----------- |
| Administrator | `admin_1`    | `1234`      |
| Operator      | `operator_1` | `Salam1234` |

### Operation Flow

1. System checks fluid levels.
2. Priority is given to filling the **Main Reservoir (170)**.
3. If it's full, secondary tanks can be filled manually using Pump110A.
4. Monitoring is done via overview/trend pages.
5. Manual override via faceplates for pump/valve testing.

### Shutdown

1. Stop Pump110A (secondary reservoir pump).
2. Activate Pump771A to discharge the main tank.
3. Remaining fluid from secondary tanks drains into the main tank.

---

## 🧰 Technologies & Requirements

* 💻 **Platform**: Siemens TIA Portal v15.1
* 🧠 **Control Logic**: Ladder & Structured Text
* 🎛️ **HMI**: WinCC Runtime Advanced (PC Station)
* ⚙️ **Target Hardware**: S7-1200 / Virtual Controller
* 🧪 **Tested on**: Windows 10 Pro, 16GB RAM, Intel i7

---

## 📁 Project Structure

```plaintext
Liquid-Storage-Control-System/
├── SCADA_project.ap15_1                # TIA Portal main project
├── AdditionalFiles/
│   └── PLCM/plcmArchive.pma15_0        # Optional PLCM archive
├── IM/                                 # HMI, Runtime and intermediate files
├── Logs/                               # PLC tag logs and conversion data
├── System/                             # Project metadata and structure
└── README.md                           # This documentation
```

---

> *“Industrial automation is intelligence in motion — this project is proof.”*

```

---

Would you prefer a more industrial name like **"Smart Liquid Terminal System"**, **"HydroControl SCADA"**, or **"FluidOps"** instead of "Liquid Storage Control System"? I can regenerate the README with your preferred naming.
```
