# ESP32-Based Smart Safety System for Flame Detection and Crowd Management

**Embedded Systems | Mechatronics | IoT | Safety-Critical Automation**

---

## 📌 Project Overview

Industrial and public infrastructure environments such as **battery rooms, warehouses, laboratories, and public venues** are vulnerable to **fire hazards, gas accumulation, and unsafe overcrowding**.  
This project presents a **dual-node, ESP32-based smart safety system** that integrates **real-time hazard detection, autonomous actuation, access control, and cloud-based monitoring**.

The system is designed with **independent yet complementary nodes** for **flame detection** and **crowd management**, ensuring **reliable, scalable, and safety-oriented decision-making** at the edge, with visualization and monitoring through an **IoT dashboard**.

---

## 🏗️ System Architecture

The solution follows an **Edge–Fog–Cloud architecture**:

- **Edge Layer (ESP32 Nodes):**  
  Real-time sensing, calibration-based thresholding, decision logic, and actuation
- **Fog Layer:**  
  Local preprocessing and event-driven decision execution with minimal latency
- **Cloud Layer (ThingsBoard):**  
  System monitoring, telemetry visualization, and historical analysis

The two nodes operate independently while following a common safety logic framework.

---

## 🔥 Node 1: Flame Detection & Gas Safety Node

### Functionality
- Flame detection using a **flame sensor**
- Gas and air-quality monitoring using a **calibrated MQ-135 sensor**
- **Buck-converter-based power regulation** for stable operation
- Real-time system status display on an **OLED**
- Audible alert via **buzzer**
- **MOSFET-driven water pump activation** when hazard thresholds are exceeded

### Safety Logic
1. Sensor data is continuously sampled and filtered
2. Calibrated thresholds are applied to avoid false triggering
3. On hazard detection:
   - Visual warning displayed on OLED
   - Buzzer activated
   - Water pump automatically triggered for fire suppression
4. System status is transmitted to the IoT dashboard

---

## 👥 Node 2: Crowd Management & Access Control Node

### Functionality
- **IR-based people counting** for entry/exit tracking
- **Calibrated load cell** used for occupancy estimation and validation
- **DHT11 sensor** for temperature and humidity monitoring
- OLED-based real-time visualization
- Buzzer alerts for overcrowding conditions
- **Servo-controlled gates** to automatically regulate entry when limits are exceeded

### Control Logic
1. IR sensors count people entering and exiting
2. Load cell readings validate occupancy data
3. Environmental conditions are monitored in parallel
4. When crowd thresholds are exceeded:
   - Entry gates are automatically closed
   - Audible and visual alerts are triggered
   - Event status is logged to the cloud dashboard

---

## 📊 IoT Dashboard (ThingsBoard)

The system integrates with a **ThingsBoard IoT dashboard** for:
- Real-time telemetry visualization
- Hazard and crowd-status monitoring
- Event logging and trend analysis
- Remote supervision of safety conditions

The dashboard serves as a **decision-support and monitoring interface** rather than a control dependency, ensuring safety actions remain functional even without cloud connectivity.

---

## 🔧 Calibration & Reliability

All sensors were **experimentally calibrated** to ensure consistent and reliable behavior:
- MQ-135 gas sensor baseline calibration
- Load cell calibration using known weights(250g)
- IR counter validation for accuracy
- Threshold tuning through controlled test cases

Calibration data ensures the system operates **robustly under real-world conditions**, reducing false alarms and improving safety response accuracy.

---

## 📂 Repository Structure

├── flame_detection_node/
│ ├── firmware
│ ├── hardware
│ ├── calibration
│ └── documentation
│
├── crowd_management_node/
│ ├── firmware
│ ├── hardware
│ ├── calibration
│ └── documentation
│
├── architecture/
│ ├── edge_fog_cloud_diagram
│ ├── flame_node_block_diagram
│ └── crowd_node_block_diagram
│
├── iot_dashboard/
│ └── thingsboard_dashboard
│
├── media/
│ ├── demo_videos
│ └── system_images
│
└── docs/
├── system_overview
├── decision_logic
└── calibration_methodology


---

## 🧠 Skills Demonstrated

- Embedded systems design using **ESP32**
- Sensor interfacing and calibration
- Safety-critical decision logic
- Power regulation and actuator control
- Servo-based access control mechanisms
- Edge–Cloud IoT integration
- Real-time visualization and monitoring
- System-level thinking and modular design

---

## 📈 Results & Observations

- Reliable detection of flame and hazardous gas conditions
- Accurate crowd estimation through sensor fusion
- Autonomous safety response without human intervention
- Stable system behavior under continuous operation
- Clear real-time visualization for monitoring and analysis

---

## 🚀 Future Improvements

- Integration of MQTT-based inter-node communication
- Predictive analytics using historical IoT data
- Camera-based crowd density estimation
- Redundant sensing for higher fault tolerance
- Industrial-grade enclosure and EMI protection

---

## 📜 License

This project is licensed under the **MIT License**, allowing reuse with attribution.

---

## 👤 Author

**Manash Pratim Ghosh**  
M.Tech Mechatronics Engineering  
Embedded Systems | Control | IoT | Safety Automation



