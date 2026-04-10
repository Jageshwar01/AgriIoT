# 🌾 AgriIoT – Smart Agriculture Monitoring System

> A fully deployed IoT-based smart farming platform that automates irrigation and provides real-time farm monitoring via a Flutter mobile app. **Live and actively used by real farmers.**

---

## 📱 Overview

AgriIoT is an end-to-end smart agriculture monitoring system built to solve a real problem — farmers spending time and water on manual irrigation when sensors can do it smarter. The system monitors soil moisture, temperature, and humidity in real time, automatically controls a water pump, and gives farmers full remote control through a mobile app.

---

## ✨ Features

- 🌡️ **Real-time monitoring** — temperature, humidity, and soil moisture via DHT11 and soil moisture sensors
- 💧 **Automated irrigation** — water pump controlled automatically by ESP32 based on live soil moisture readings
- 📱 **Flutter mobile app** — remote monitoring and manual control from anywhere
- 🔔 **Smart alerts** — push notifications when readings go abnormal or irrigation is needed
- ☁️ **Firebase sync** — all sensor data logged and synced to Firebase real-time database
- 🔥 **Fire & smoke detection** — MQ-2 gas/smoke sensor and flame sensor continuously monitor for fire incidents; triggers buzzer alarm and instant push notification alert to farmer's phone
- 📊 **Data visualization** — historical charts and trend analysis in the app
- ✅ **Field tested** — validated on real test rigs and actual farm conditions

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Microcontroller | ESP32 |
| Sensors | DHT11 (Temp & Humidity), Soil Moisture Sensor |
| Hardware Control | Water Pump Motor via Relay |
| Database | Firebase Real-time Database |
| Mobile App | Flutter (Dart) |
| Notifications | Firebase Cloud Messaging (FCM) |
| Platform | Android |

---

## 🏗️ System Architecture

```
[DHT11 Sensor] ────┐
[Soil Sensor] ─────┤
                   ├──► [ESP32 Microcontroller] ──► [Firebase Database] ──► [Flutter App]
[MQ-2 Sensor] ─────┤         │
[Flame Sensor] ────┘         ├──► [Water Pump Relay]
                              └──► [Buzzer Alarm]
```

---

## 🎯 Objectives

- Design and implement a smart agriculture monitoring system for real-time analysis of farm environmental data
- Automate irrigation by controlling a water pump based on soil moisture data
- Enable remote monitoring and control via a mobile application for optimal farm management
- Provide farmers with timely alerts and insights for data-driven decision-making
- Improve water usage efficiency and promote sustainable farming practices

---

## ⚙️ How It Works

1. **ESP32** continuously reads data from DHT11 (temperature & humidity), soil moisture, MQ-2 gas/smoke, and flame sensors
2. If soil moisture drops below threshold → ESP32 triggers the water pump relay automatically
3. If fire or smoke is detected → ESP32 instantly triggers the **buzzer alarm** and sends an **emergency push notification** to the farmer's phone
4. All sensor readings are pushed to **Firebase real-time database** every few seconds
5. The **Flutter app** pulls live data from Firebase and displays it to the farmer
6. Farmer can also **manually control** the water pump from the app
7. **Push notifications** are sent when readings are abnormal or irrigation begins/ends

---

## 📲 Mobile App Screenshots

![Dashbord](https://github.com/user-attachments/assets/4ec0d3a1-47f0-41da-a66d-60d8c55b994a)
![Motor_Control](https://github.com/user-attachments/assets/91012604-bf5b-4afd-a922-07ee1c7b7c5b)
![Graph](https://github.com/user-attachments/assets/3eec3fa9-fd70-464f-8af7-90b9ade6a85e)
![Motor_Control](https://github.com/user-attachments/assets/0175c621-7ad5-4a5b-b379-b526cdf9ea14)
![Soil_condition](https://github.com/user-attachments/assets/6cc346d3-cbac-4e87-9aaf-3c69f0d02dfa)

---

## 🔧 Hardware Requirements

- ESP32 Development Board
- DHT11 Temperature & Humidity Sensor
- Soil Moisture Sensor
- MQ-2 Gas & Smoke Sensor
- Flame Sensor
- Buzzer Module (alarm)
- Water Pump + Motor Relay Module
- Power Supply (5V)
- Jumper Wires & Breadboard

---

## 🚀 Getting Started

### Firebase Setup
1. Create a Firebase project at [firebase.google.com](https://firebase.google.com)
2. Enable Real-time Database
3. Enable Firebase Cloud Messaging for notifications
4. Download `google-services.json` and place in `/android/app/`

### ESP32 Setup
1. Install Arduino IDE
2. Add ESP32 board support
3. Install libraries: `DHT sensor library`, `Firebase ESP32 Client`
4. Update WiFi credentials and Firebase URL in the code
5. Upload to ESP32

### Flutter App Setup
```bash
git clone https://github.com/Jageshwar01/AgriIoT.git
cd AgriIoT/app
flutter pub get
flutter run
```

---

## 📊 Project Status

| Component | Status |
|-----------|--------|
| ESP32 Firmware | ✅ Complete |
| Firebase Integration | ✅ Complete |
| Flutter Mobile App | ✅ Complete & Live |
| Automated Irrigation | ✅ Complete |
| Fire & Smoke Detection | ✅ Complete |
| Buzzer Alarm System | ✅ Complete |
| Push Notifications | ✅ Complete |
| Field Testing | ✅ Done |

## 🌍 Impact

- Actively used by real farmers for day-to-day farm management
- Reduces water wastage through sensor-based automated irrigation
- Enables remote farm monitoring — farmers don't need to be physically present
- Scalable and cost-effective solution suitable for small and medium farms

## 👨‍💻 Developer

**Jageshwer Vishwakarma**
- 🌐 Portfolio: [mydronekart.com](https://mydronekart.com)
- 💼 LinkedIn: [linkedin.com/in/jageshwar-380b2b257](https://linkedin.com/in/jageshwar-380b2b257/)
- 🐙 GitHub: [github.com/Jageshwar01](https://github.com/Jageshwar01)
- 📧 jageshwarkumar15@gmail.com

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

> *Built to solve a real problem for real farmers. If this project helped you, give it a ⭐*
