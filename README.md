# Fuel Level Monitoring System with Blynk

Welcome to the **Fuel Level Monitoring System with Blynk** project! This project is designed to help you monitor fuel levels in a tank in real-time using an ultrasonic sensor, an ESP32 microcontroller, and the Blynk IoT platform. It’s a great tool for individuals, small businesses, or anyone looking to automate fuel level monitoring and control.

---

## 📌 **Overview**

This project uses an **ultrasonic sensor** to measure the fuel level in a tank and displays the data on an **LCD screen** and the **Blynk app**. It also includes **LED indicators** to visually represent the fuel level and a **relay module** to control a motor or pump based on user input. The system is ideal for applications such as fuel tanks, water tanks, or any liquid storage system.

---

## 🚀 **Key Features**

- **Real-Time Fuel Level Monitoring**: Measure and display fuel levels using an ultrasonic sensor.
- **Blynk IoT Integration**: Monitor and control the system remotely via the Blynk app.
- **LCD Display**: View fuel levels and system status on a 16x2 LCD screen.
- **LED Indicators**: Visual representation of fuel levels (Very Low, Low, Medium, Full).
- **Motor/Pump Control**: Control a motor or pump using a relay module via the Blynk app.
- **Customizable**: Easily adjust the tank's maximum height and fuel level thresholds.

---

## 🛠️ **Hardware Requirements**

- **ESP32 Microcontroller**
- **Ultrasonic Sensor (HC-SR04)**
- **16x2 I2C LCD Display**
- **Relay Module**
- **LEDs (4x)**
- **Resistors (for LEDs)**
- **Breadboard and Jumper Wires**
- **Power Supply (5V)**
- **Motor/Pump (optional)**

---

## 📂 **Project Setup**

### 1. **Hardware Connections**

| Component       | ESP32 Pin |
|-----------------|-----------|
| Ultrasonic Trig | GPIO 12   |
| Ultrasonic Echo | GPIO 13   |
| Relay           | GPIO 14   |
| LED1            | GPIO 2    |
| LED2            | GPIO 4    |
| LED3            | GPIO 5    |
| LED4            | GPIO 18   |
| I2C LCD SDA     | GPIO 21   |
| I2C LCD SCL     | GPIO 22   |

### 2. **Blynk Setup**
1. Download the **Blynk app** from the App Store or Google Play.
2. Create a new project in the Blynk app.
3. Add the following widgets:
   - **Gauge** (Virtual Pin V0) to display fuel level.
   - **Button** (Virtual Pin V1) to control the relay/motor.
4. Copy the **Auth Token** from the Blynk app and paste it in the `auth[]` variable in the code.

### 3. **Code Configuration**
- Replace the following placeholders in the code with your credentials:
  - `auth[]`: Your Blynk Auth Token.
  - `ssid[]`: Your Wi-Fi SSID.
  - `pass[]`: Your Wi-Fi password.
- Adjust the `MaxLevel` variable to match the height of your tank in centimeters.

---

## 🛠️ **Software Requirements**

- **Arduino IDE**
- **Blynk Library** (Install via Arduino Library Manager)
- **LiquidCrystal_I2C Library** (Install via Arduino Library Manager)
- **ESP32 Board Package** (Install via Arduino Board Manager)

---

## 📜 **How It Works**

1. The **ultrasonic sensor** measures the distance to the fuel surface in the tank.
2. The distance is converted into a fuel level percentage and displayed on the **LCD** and **Blynk app**.
3. **LEDs** indicate the fuel level:
   - **Very Low**: Only LED1 is ON.
   - **Low**: LED1 and LED2 are ON.
   - **Medium**: LED1, LED2, and LED3 are ON.
   - **Full**: All LEDs are ON.
4. The **relay module** can be controlled via the Blynk app to turn a motor or pump ON/OFF.

---

## 🚀 **Installation Steps**

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/Fuel-Level-Monitoring-System.git
   ```

2. **Open the Code**:
   - Open the `Fuel_level_monitoring_with_blynk.ino` file in the Arduino IDE.

3. **Upload the Code**:
   - Select the correct board (ESP32) and port in the Arduino IDE.
   - Upload the code to your ESP32.

4. **Power Up the System**:
   - Connect the hardware as per the wiring diagram.
   - Power up the ESP32 and wait for it to connect to Wi-Fi and Blynk.

5. **Monitor and Control**:
   - Open the Blynk app to monitor fuel levels and control the relay.

---

## 🤝 **Contributing**

We welcome contributions from the community! If you'd like to improve this project, please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bugfix:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your message here"
   ```
4. Push your branch:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Open a pull request and describe your changes.

---

## 📜 **License**

This project is licensed under the **MIT License**. Feel free to use, modify, and distribute it as per the license terms.

---

## 🙏 **Acknowledgments**

- Special thanks to the **Blynk community** for providing an excellent IoT platform.
- Inspired by the need for efficient fuel management in various industries.

---



---

Thank you for checking out the **Fuel Level Monitoring System with Blynk**! We hope this project helps you streamline your fuel monitoring processes and achieve greater efficiency. Happy tinkering! 🚀
