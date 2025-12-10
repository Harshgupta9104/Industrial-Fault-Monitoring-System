# Industrial Fault Monitoring System

A simple IoT-based system that monitors important industrial conditions such as temperature, humidity, gas levels, fire, and motion. The system uses NodeMCU ESP8266 and multiple sensors to detect faults in real-time. When a fault occurs, it triggers a buzzer and LED alert and sends live data to an MQTT-based dashboard for remote monitoring.

🚀 Features

Real-time monitoring of temperature, humidity, gas levels, motion, and flame

Instant alerts via buzzer, OLED display, and optional mobile dashboard

LoRa/ESP32/ESP8266-based communication for long-range data transfer

Fault detection with threshold-based warning system

Lightweight and scalable design for industrial use

## 📦 Components Used

**ESP32 Dev Module** – Main microcontroller for processing sensor data

**DHT22 / DHT11 Sensor** – Temperature & humidity measurement

**MQ135 Gas Sensor** – Air quality & hazardous gas detection

**Flame Sensor** – Fire/flame detection

**PIR Motion Sensor** – Human/abnormal movement detection

BME280 Sensor – Temperature, humidity & pressure

0.96" OLED Display (I2C) – Real-time status display

Buzzer – Fault alert and alarm indication

Breadboard – For temporary prototyping

Jumper Wires (M-M / M-F) – Sensor and module connections

Micro USB Cable – To upload code and power the microcontroller

5V/3.3V Power Supply / Adapter – Stable power source

## 🛠️ How It Works
The Industrial Fault Monitoring System works by continuously reading data from multiple sensors connected to the ESP32. The ESP32 processes these readings and sends them to a web-based dashboard using the MQTT protocol. The dashboard displays the real-time status and analysis of all sensor data.

Below is the clear step-by-step working:

1️⃣ Sensor Data Collection

The ESP32 reads values from the following sensors:

DHT22 → Temperature & humidity

MQ135 → Harmful gas level / air quality

Flame Sensor → Fire detection

PIR Sensor → Human motion detection

These sensors provide continuous real-time data to the ESP32.

2️⃣ ESP32 Processing

The ESP32 checks all sensor values and compares them with safe thresholds.

Examples:

High temperature → possible overheating

High MQ135 value → gas leak or poor air quality

Flame detected → fire alert

Motion detected → intrusion alert

If any parameter goes beyond safe limits, ESP32 identifies it as a fault.

3️⃣ Local Alerts

When a fault is detected, ESP32 immediately activates:

Buzzer → audio alert

LED → visual warning

This ensures nearby workers know something is wrong instantly.

4️⃣ MQTT Communication

ESP32 sends (publishes) sensor readings and alerts to an MQTT broker using Wi-Fi.

Example topics:

## 🖥️ Dashboard Integration

Dashboard Integration

Built as a web-based interface that provides real-time monitoring and analysis.

The ESP32 publishes JSON sensor data to an MQTT broker; the dashboard connects over MQTT over WebSocket and subscribes to the same topics.

The dashboard displays live temperature, humidity, motion status, gas level, and fire alerts.

Active faults are highlighted visually (color change / flashing card) and logged in an alert panel so operators can quickly spot and respond to issues.


✅ Benefits of the System

Real-time Monitoring
Continuously checks temperature, humidity, gas levels, motion, and fire conditions without manual supervision.

Instant Fault Alerts
Any abnormal condition triggers a buzzer, LED alert, and dashboard notification, ensuring quick action.

Remote Visibility
Using MQTT and a web dashboard, users can monitor the factory environment from anywhere.

Low Cost & Easy to Deploy
Uses ESP32 and common sensors, making the system affordable and simple to install.

Enhances Industrial Safety
Helps prevent accidents by detecting issues early, such as gas leaks, rising temperature, or fire hazards.

Scalable System Design
More sensors or new features can be added anytime without changing the core architecture.

Supports Industry 4.0
Integrates IoT, automation, and live data visualization — matching modern industrial monitoring standards.

