# 🗑️ Smart Bin – Wi-Fi Controlled Trash Bin

This project implements a **Wi-Fi Controlled Smart Trash Bin** using the **Raspberry Pi Pico W**. The bin is equipped with an **ultrasonic sensor** to measure the fill level, a **BMP280 sensor** for temperature monitoring, and a **servo motor** to control the lid. The bin can be monitored and controlled remotely via a web interface. 🌐

## 🚀 Technologies Used
- **MicroPython** – The programming language used on Raspberry Pi Pico W.  
- **Raspberry Pi Pico W** – Wi-Fi enabled microcontroller.  
- **HC-SR04 Ultrasonic Sensor** – Measures the fill level of the trash bin.  
- **BMP280 Sensor** – Monitors ambient temperature. 🌡️  
- **Servo Motor** – Controls the trash bin lid. 🤖  
- **Webserver (Socket)** – Allows remote control via a web interface. 🌐

## 🏆 Features
- **Web Interface**: View sensor data (distance and temperature) and control the trash bin lid. 💻
- **Distance Measurement**: Detects the fill level using the ultrasonic sensor. 📏
- **Temperature Monitoring**: Measures the ambient temperature using the BMP280 sensor. 🌡️
- **Lid Control**: Open or close the trash bin lid remotely via the web interface. 🔄
- **Warning Alerts**: The LED and buzzer activate when the bin is full. 🚨

## 🛠️ API Endpoints

The smart bin supports RESTful API requests:

| **Endpoint** | **Description**               | **Example Usage**       |
|--------------|-------------------------------|-------------------------|
| `/open`      | Opens the bin lid             | `GET /open`             |
| `/close`     | Closes the bin lid            | `GET /close`            |
| `/sensor`    | Fetches sensor data (distance and temperature) | `GET /sensor`           |

## ⚙️ Usage
- **Open Lid**: Click the "Open Lid" button on the web interface to open the trash bin lid. 🔓
- **Close Lid**: Click the "Close Lid" button to close the lid. 🔒
- **Sensor Data**: View the fill level and temperature data on the web interface. 📊

## 📝 Instructions
1. Flash the code onto your **Pico W** microcontroller. You can choose between two similar programs: one allows HTTP requests, while the other does not. Both can be used, but the version with HTTP requests enables GET requests.
2. Build your smart bin according to the diagram provided in the documentation.
3. Ensure that the **Wi-Fi connection** is set up correctly. Update the network name (SSID) and password in the MicroPython code.
4. Use **Thonny IDE** (or any other IDE of your choice) to run the code on your **Pico W**. 
   - After running the code, the IP address of your **Pico W** will be displayed by the software. For other IDEs, you can make the **Pico W** visible by using special extensions in **VS Code** or other IDEs. (Note: future IDEs might provide standard support for **Pico W**).
5. Access the server by entering the IP address in a browser to control the bin.

## 🛠️ Hardware Components
- **Raspberry Pi Pico W**: The microcontroller used for the smart bin.  
  [PICO W Datasheet](https://www.optimusdigital.ro/ro/placi-raspberry-pi/12394-raspberry-pi-pico-w.html)  
- **HC-SR04 Ultrasonic Sensor**: Used to measure the distance and fill level of the trash bin.  
  [HC-SR04 Datasheet](https://www.optimusdigital.ro/ro/senzori-senzori-ultrasonici/9-senzor-ultrasonic-hc-sr04-.html)  
- **BMP280 Sensor**: Used to monitor ambient temperature.  
  [BMP280 Datasheet](https://www.optimusdigital.ro/ro/senzori-senzori-de-presiune/1666-modul-senzor-de-presiune-barometric-bmp280.html)  
- **SG90 Servo Motor**: Controls the lid of the trash bin.  
  [SG90 Servo Datasheet](https://www.optimusdigital.ro/ro/motoare-servomotoare/26-micro-servomotor-sg90.html)  
- **Piezo Buzzer**: Emits sound alerts when the trash bin is full.  
  [Piezo Buzzer Datasheet](https://www.optimusdigital.ro/ro/audio-buzzere/12247-buzzer-pasiv-de-33v-sau-3v.html)

## 🖼️ Photos

Here are some photos of the project setup and the smart bin in action:
![prototype](https://github.com/user-attachments/assets/df8cf20b-cd81-4aaf-879f-cbb2ef517982)
![WhatsApp Image 2025-02-19 at 21 03 37_69640598](https://github.com/user-attachments/assets/88105615-b149-4df8-b0b4-c48ff5f30924)


## ⚡ Electrical Circuit

Here’s the schematic of the electrical circuit for connecting the components to the Raspberry Pi Pico W:
![circuit](https://github.com/user-attachments/assets/68070817-f2a4-4e04-b60b-a2394a39bbc8)


