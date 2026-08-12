🚶 Smart Blind Stick

An IoT-based assistive device designed to help visually impaired people detect obstacles and water hazards while walking. The system uses an Arduino UNO, ultrasonic sensor, water sensor, buzzer, and vibration motor to provide alerts to the user.

📌 Project Overview

The Smart Blind Stick is designed to improve the safety and mobility of visually impaired users.

The system continuously monitors the surroundings using sensors:

🚧 The ultrasonic sensor detects obstacles within 50 cm.

💧 The water sensor detects water on the path.

🔊 The buzzer provides audio alerts.

📳 The vibration motor provides tactile alerts.


The system can identify four different situations:

1. Obstacle detected
2. Water detected
3. Both obstacle and water detected
4. Nothing detected

✨ Features

🚧 Real-time obstacle detection

💧 Water hazard detection

🔊 Different buzzer patterns for different hazards

📳 Vibration alert for obstacle detection

♿ Designed as an assistive technology for visually impaired users

💰 Low-cost and simple hardware

⚡ Arduino-based implementation

🔄 Continuous sensor monitoring


🛠️ Components Used

Component                  	Purpose

Arduino UNO          	Main microcontroller
Ultrasonic Sensor    	Detects obstacles
Water Sensor	        Detects water
Buzzer	              Provides audio alerts
Vibration Motor     	Provides vibration alerts
Breadboard          	Circuit connections
Jumper Wires	        Connects components
Battery              	Power supply


🔌 Pin Connections

Component	                  Arduino Pin

Ultrasonic TRIG	            Digital Pin 9
Ultrasonic ECHO           	Digital Pin 10
Buzzer	                    Digital Pin 7
Vibration Motor           	Digital Pin 6
Water Sensor	              Analog Pin A0


⚙️ How It Works

1. Obstacle Detection

The ultrasonic sensor sends an ultrasonic pulse and measures the time taken for the echo to return.

The distance is calculated using:

Distance = Duration × 0.034 / 2

If an obstacle is detected within 50 cm, the system considers it an object hazard.

The vibration motor is activated and the buzzer produces an alert.

2. Water Detection

The water sensor is connected to analog pin A0.

The code uses a threshold value of:

waterValue > 300

If the sensor value is greater than 300, water is considered detected.

The buzzer produces a repeating alert.

3. Both Obstacle and Water Detected

If both hazards are detected at the same time:

The vibration motor is activated.

The buzzer produces two different tones.

This provides a distinct warning to the user.


4. Nothing Detected

When no obstacle or water is detected:

Buzzer is turned OFF.

Vibration motor is turned OFF.


🔄 System Flow

Start
          ↓
 Initialize Arduino
      and Sensors
          ↓
 Read Ultrasonic
      Sensor
          ↓
  Obstacle < 50 cm?
       ↙       ↘
     Yes        No
      ↓          ↓
 Read Water    Read Water
   Sensor        Sensor
      ↓          ↓
 Water Detected? Water Detected?
   ↙      ↘       ↙      ↘
 Yes      No     Yes      No
  ↓        ↓      ↓        ↓
Both?   Object   Water   Nothing
  ↓      Alert    Alert   Detected
  ↓
Buzzer +
Vibration
          ↓
        Repeat

🔔 Alert Conditions

Condition	                              Buzzer	                      Vibration

Obstacle only                       	1500 Hz                       	ON
Water only	                       Repeating 800 Hz                 	OFF
Obstacle + Water	                 1200 Hz + 1800 Hz	                ON
Nothing detected	                      OFF                         	OFF


💻 Software

The project is programmed using Arduino C/C++.

Tools Used

Arduino IDE

Arduino UNO

Embedded C/C++


📂 Project Structure

Smart-Blind-Stick/
│
├── smart_blind_stick.ino
├── README.md
│
├── Images/
│   ├── smart_blind_stick_1.jpg
│   ├── smart_blind_stick_2.jpg
│   ├── smart_blind_stick_3.jpg
│   └── smart_blind_stick_4.jpg
│
└── Demo/
    └── smart_blind_stick_demo.mp4

🚀 How to Run the Project

1. Install the Arduino IDE.

2. Connect the Arduino UNO to your computer.

3. Open smart_blind_stick.ino.

4. Connect the sensors and components according to the pin configuration.

5. Select the correct Arduino board and COM port.

6. Upload the code to the Arduino UNO.

7. Open the Serial Monitor at 9600 baud.

8. Test the stick by placing an object within 50 cm and by exposing the water sensor to water.


📊 Serial Monitor

The Arduino continuously displays sensor readings such as:

Distance: 35
Water: 120

This can be used to monitor the ultrasonic sensor distance and water sensor value during testing.

🎯 Applications

The Smart Blind Stick can be used as an assistive device for:

Visually impaired people

Obstacle detection

Water/puddle detection

Indoor navigation assistance

Outdoor walking assistance


🔮 Future Improvements

The project can be further improved by adding:

📍 GPS location tracking

📱 Mobile application integration

🆘 Emergency SOS button

📞 Emergency contact notification

🔋 Rechargeable battery system

🗣️ Voice alerts

🤖 AI-based object detection

📡 IoT/cloud connectivity

🌐 Real-time location sharing


📸 Project Images

Arduino and Wiring

Arduino Setup

Complete Smart Blind Stick

Sensor and Stick Setup


🎥 Project Demonstration

The demonstration video shows the working of the Smart Blind Stick prototype, including the sensor-based obstacle and water detection system.

▶️ Watch Smart Blind Stick Demonstration

👩‍💻 Author

Harshitha G

B.Tech CSE – AIML

📄 License

This project is created for educational and academic purposes.


---

⭐ If you find this project useful, consider giving this repository a star!
