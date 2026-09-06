# PLC Automatic Water Tank Control System

## Overview

This project is an automatic water tank filling and protection system developed using PLC Ladder Logic.

The system automatically controls a water pump based on low-level and high-level sensors. It also includes safety and fault-handling functions to protect the system during abnormal operating conditions.

## Software & Hardware

- RSLogix Micro Starter Lite
- RSLogix Emulate 500
- RSLinx Classic
- Allen-Bradley MicroLogix 1100
- Ladder Logic (LD)

## Main Features

- Automatic water tank filling
- START/STOP control with system latch
- Low-level and high-level detection
- 5-second pump start delay
- Automatic pump shutdown at high level
- 30-second filling timeout protection
- Emergency stop protection
- Motor overload protection
- Fault alarm and manual reset
- RUN, LOW LEVEL, and FULL status indicators

## System Operation

When the system is started and a low water level is detected, a filling request is activated. After a 5-second delay, the pump starts automatically.

The pump continues filling the tank until the high-level sensor is activated, then the pump stops.

If the tank does not reach the high level within 30 seconds while filling, the system generates a fault. Emergency stop and motor overload conditions also stop the pump and activate the fault protection.

## Simulation & Testing

The project was tested using RSLogix Emulate 500.

Three simulation tests were performed:

1. [Normal Operation](Videos/01_Normal_Operation.mp4) — Automatic filling from low level to high level.
2. [Timeout Fault](Videos/02_Timeout_Fault.mp4) — Verification of the 30-second filling timeout and alarm.
3. [Safety & Reset](Videos/03_Safety_and_Reset.mp4) — Verification of protection and fault reset operation.

## What I Learned

Through this project, I practiced:

- PLC Ladder Logic programming
- Digital I/O control
- Latching and unlatching logic
- Timer instructions
- Automatic sequence control
- Fault and protection logic
- PLC simulation and testing
- Troubleshooting
