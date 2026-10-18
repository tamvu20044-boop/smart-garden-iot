# 🌱 Smart Garden IoT System

An IoT system model for monitoring and automatically controlling a smart garden using the ESP32 microcontroller, MQTT communication protocol, and a real-time Web Dashboard.

---

## 👥 Group 5 Members (Da Nang University of Science and Technology)
* **Instructor:** Dr. Van Phu Tuan
* **Contributors:**
  * Dang Van Thinh (22DT1)
  * Ho Van Trung (22DT1)
  * Nguyen Tam Vu (22DT1) - *Embedded & IoT Developer*
  * Phan Thi Hoang Ngan (22DT1)
  * Luu Tran Hong Khuyen (22DT5)

---

## 📋 Project Overview
This project was developed to automate plant care, reducing manual effort and saving water compared to traditional methods. The system features:
* **Real-time Environmental Monitoring:** Continuously tracks temperature, air humidity, soil moisture, and light intensity.
* **Smart Automation:** Automatically activates the water pump when the soil is dry, turns on the cooling fan when the temperature is high, or switches on the grow light when brightness is low based on predefined thresholds.
* **Remote Control:** Allows users to manually monitor and toggle devices via the Web Dashboard using the MQTT protocol.

---

## 🖼️ Hardware Implementation

<img width="690" height="450" alt="Hardware Model" src="https://github.com/user-attachments/assets/0c4c087c-556c-4fb3-8ccf-2af937fa25e5" />

---

## 📊 Web Dashboard Interface

<img width="966" height="528" alt="Web Dashboard" src="https://github.com/user-attachments/assets/fb702820-22f6-4764-a5ff-71448014f17d" />

---

## ⚙️ System Block Diagram & Source Code Structure

```text
[ Soil Moisture Sensor ] ──┐
[ DHT11 Sensor         ] ──┼──> [ ESP32 Microcontroller ] ──> [ 16x2 LCD Display ]
[ Light Sensor         ] ──┘          │                              │
                                      ├──> [ Relay & Devices ] ──> (Pump, Fan, Light)
                                      └──> [ MQTT Protocol   ] ──> [ Web Dashboard ]

Nhom5_HTN/
│
├── MQTT/
│   └── MQTT.ino         # Main source code for ESP32 to connect to Wi-Fi, read sensors, and process MQTT
├── testmqtt/
│   └── subscriber.js    # Data processing script for the subscriber/web server
└── README.md
