# Automotive Electronics: Sensors, Actuators & Architecture

## Introduction
Automotive electronics play a central role in **engine control, safety, comfort, and infotainment**.  
Core building blocks include:
- **Sensors**: detect physical parameters (light, sound, pressure, temperature, etc.) and convert them into electrical signals.
- **Actuators**: perform physical/mechanical actions in response to ECU signals.
- **ECUs**: process sensor data and control actuators.

---

## Sensors in Automotive
A **sensor** produces an output signal based on a physical phenomenon.

### Example: Accelerator Pedal
- Modern pedals include **two potentiometer-based resistive circuits**.
- These vary resistance with pedal movement → converted into voltage → sent to the **Engine Control ECU**.
- ECU uses calibration tables to determine throttle valve position.
- **Redundancy**: two sensors ensure safety; if one fails, the system remains operational.

### Common Engine Sensors
- **Crankshaft & Camshaft position sensors** – detect piston/cam positions.
- **Knock sensor** – measures engine vibrations.
- **Coolant/engine temp sensor** – monitors overheating.
- **Airflow & pressure sensors** – for intake management.
- **Oil pressure sensor** – lubrication status.
- **Oxygen/Lambda sensors** – monitor exhaust gases.
- **Exhaust gas temp sensors** – emission control.

### Vehicle-Level Sensors
- Brake fluid level sensors  
- Wheel speed sensors  
- Parking (ultrasonic) sensors  
- Lane departure & night vision cameras  
- Airbag sensors, pedestrian detection (LiDAR, radar, cameras)

---

## Actuators in Automotive
An **actuator** converts ECU signals into mechanical action.

### Examples
- **Throttle valve actuator** – regulates airflow into engine.  
- **Exhaust gas recirculation valve** – reduces emissions.  
- **Wiper motor** – controlled by body ECU.  
- **Fuel pump** – delivers fuel from tank on demand.  
- **Door lock actuators / Power window motors** – convenience systems.  

Sensors → ECU → Actuators is the fundamental control loop.

---

## Engine Control Management (ECM)
- ECM contains **microcontrollers, calibration data, lookup tables**.  
- Controls firing, fuel injection, and spark timing using sensor feedback.  
- **Critical sensors**:  
  - Crankshaft sensor – detects piston position via flywheel & reluctance pickup.  
  - Camshaft sensor – detects valve timing for intake/fuel mixing.  
- **Critical actuators**:  
  - Spark plugs/ignition coils  
  - Throttle valve  

⚠️ If the ECM fails → engine cannot start or run.

---

## Electrical & Electronic Architecture
- ECUs are grouped by **domains**:  
  - Powertrain  
  - Body  
  - Chassis  
  - Safety  
  - Infotainment  
- Communication protocols: **CAN, LIN, FlexRay, Ethernet, MOST**.  
- Evolution from **distributed ECUs → centralized/zonal architectures**.

---

## Wiring Harness
The **wiring harness** interconnects sensors, ECUs, and actuators.

### Key Elements
- **Fuses/Fuse box** – protects circuits from overcurrent.  
- **Connectors & Terminals** – reliable under vibration & heat.  
- **Grounding (KL31)** – entire car body acts as common ground.  
- **Power lines**:  
  - **KL30** – always active (battery direct).  
  - **KL15** – active with ignition ON.  
  - **KL50** – active during cranking (starter motor).  

Harness design must balance **safety, durability, and weight reduction**, especially in EVs.

---

## Summary
Modern vehicles rely on a tight integration of:
- **Sensors** → detect environment & state.  
- **ECUs (ECM, BCM, ABS, etc.)** → process data & decide actions.  
- **Actuators** → execute mechanical operations.  
- **Harness & Architecture** → interconnect everything reliably.  

Electronics now account for **40–50% of a car’s systems**, making them essential for performance, safety, and comfort.

