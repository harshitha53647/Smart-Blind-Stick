🚶 Smart Blind Stick

An IoT-based assistive device designed to help visually impaired people detect obstacles and water hazards while walking. The system uses an Arduino UNO, ultrasonic sensor, water sensor, buzzer, and vibration motor to provide alerts to the user.

📸 Project Preview



📌 Project Overview

The Smart Blind Stick is an IoT-based assistive technology project developed to improve the safety and mobility of visually impaired users.

The system continuously monitors the surroundings using sensors and provides alerts when an obstacle or water hazard is detected.

The project can identify:

🚧 Obstacles in the user's path

💧 Water on the walking path

🚧💧 Both obstacle and water simultaneously

✅ Safe condition when nothing is detected


✨ Features

🚧 Real-time obstacle detection

💧 Water hazard detection

🔊 Audio alerts using a buzzer

📳 Vibration alerts

🔄 Continuous sensor monitoring

⚡ Arduino-based implementation

💰 Low-cost hardware design

♿ Designed as an assistive technology for visually impaired people


🛠️ Components Used

Component	Purpose

Arduino UNO	Main microcontroller
Ultrasonic Sensor	Detects obstacles
Water Sensor	Detects water
Buzzer	Provides audio alerts
Vibration Motor	Provides vibration alerts
Breadboard	Circuit connections
Jumper Wires	Connects components
Battery/Power Supply	Powers the system


🔌 Pin Configuration

Component	Arduino Pin

Ultrasonic TRIG	Digital Pin 9
Ultrasonic ECHO	Digital Pin 10
Buzzer	Digital Pin 7
Vibration Motor	Digital Pin 6
Water Sensor	Analog Pin A0


⚙️ Working Principle

1. Obstacle Detection

The ultrasonic sensor sends an ultrasonic pulse and measures the time taken for the echo to return.

The distance is calculated using:

Distance = Duration × 0.034 / 2

If an obstacle is detected within 50 cm, the system considers it an object hazard.

The vibration motor is activated and the buzzer produces an alert.

2. Water Detection

The water sensor is connected to analog pin A0.

The program uses a threshold value of:

waterValue > 300

If the sensor reading is greater than 300, water is considered detected.

The buzzer produces a repeating alert to warn the user.

3. Obstacle + Water Detection

If both an obstacle and water are detected:

The vibration motor is activated.

The buzzer produces two different tones.

This provides a distinct warning to the user.


4. Nothing Detected

When no obstacle or water is detected:

Buzzer is turned OFF.

Vibration motor is turned OFF.


🔔 Alert Conditions

Condition	Buzzer	Vibration

🚧 Obstacle only	1500 Hz tone	ON
💧 Water only	Repeating 800 Hz tone	OFF
🚧💧 Obstacle + Water	1200 Hz + 1800 Hz tones	ON
✅ Nothing detected	OFF	OFF


🔄 System Flow

START → Initialize Arduino and Sensors → Read Ultrasonic Sensor → Check for Obstacle → Read Water Sensor → Check for Water → Activate Appropriate Alert → Repeat

💻 Software & Technologies

Arduino UNO

Arduino IDE

Embedded C/C++

Ultrasonic Sensing

Water Detection

IoT / Embedded Systems


📂 Project Structure

Smart-Blind-Stick/

├── smart_blind_stick.ino
├── README.md
├── Images/
│   ├── smart_blind_stick_1.jpg
│   ├── smart_blind_stick_2.jpg
│   ├── smart_blind_stick_3.jpg
│   └── smart_blind_stick_4.jpg
└── Demo/
└── smart_blind_stick_demo.mp4

🚀 How to Run

1. Install the Arduino IDE.


2. Connect the Arduino UNO to your computer.


3. Open smart_blind_stick.ino.


4. Connect the components according to the pin configuration.


5. Select Arduino UNO as the board.


6. Select the correct COM port.


7. Upload the program.


8. Open the Serial Monitor at 9600 baud.


9. Test the ultrasonic sensor by placing an object within 50 cm.


10. Test the water sensor using a small amount of water.


11. Observe the buzzer and vibration alerts.



📊 Serial Monitor

The system displays sensor readings through the Serial Monitor.

Example:

Distance: 35
Water: 120

The distance value represents the approximate distance detected by the ultrasonic sensor, while the water value represents the analog reading from the water sensor.

📷 Project Images

Arduino and Wiring



Arduino Setup



Complete Smart Blind Stick



Sensor and Stick Setup



🎥 Project Demonstration

The demonstration video shows the working Smart Blind Stick prototype and its sensor-based alert system.

▶️ Watch the Smart Blind Stick Demo

🎯 Applications

The Smart Blind Stick can be useful for:

Visually impaired people

Obstacle detection

Water/puddle detection

Indoor navigation assistance

Outdoor walking assistance

Assistive technology applications


🔮 Future Improvements

The project can be further enhanced by adding:

📍 GPS-based location tracking

📱 Mobile application integration

🆘 Emergency SOS button

📞 Emergency contact notifications

🗣️ Voice alerts

🤖 AI-based object recognition

📡 IoT/cloud connectivity

🌐 Real-time location sharing

🔋 Improved rechargeable battery system


📈 Future Scope

With additional sensors and AI/IoT capabilities, the Smart Blind Stick could be developed into a more advanced assistive navigation system capable of recognizing different objects, providing voice-based instructions, sharing the user's location, and sending emergency alerts.

👩‍💻 Author

Harshitha Chinmai

B.Tech CSE – AIML

📄 License

This project is created for educational and academic purposes.


---

⭐ If you find this project useful, consider giving this repository a star!
