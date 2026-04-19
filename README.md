# IOT-SMART-SWITCH-WITH-PRI
Smart Motion-Sensing Home Automation (SinricPro + ESP8266)
​This project is an advanced IoT-based Home Automation system using a PIR Motion Sensor and SinricPro. It allows you to control two appliances (e.g., Light and Fan) via mobile app, voice assistants (Alexa/Google Home), and physical manual buttons, all while saving energy automatically.
​🌟 Key Features
​Dual Control: Seamlessly switch between the SinricPro Mobile App and physical push buttons.
​Energy Efficient: Automatically turns OFF all appliances if no motion is detected for 30 seconds.
​State Recovery (Memory): When motion is detected again, the system restores the exact previous state (e.g., if only the fan was on before the timeout, only the fan will turn back on).
​Real-time Sync: Manual button presses instantly update the status in the SinricPro app.
​🛠 Required Components
​NodeMCU ESP8266 (Microcontroller)
​2-Channel Relay Module (Active-Low)
​HC-SR505 (Mini PIR) or HC-SR501 Motion Sensor
​Push Buttons (x2)
​External 5V Power Supply (Recommended for stability)
​🔌 Wiring Diagram
​Follow the table below to connect your components to the NodeMCU:
Note: Connect the second terminal of the push buttons to GND as the code uses internal INPUT_PULLUP.
🚀 Installation Guide
1. SinricPro Setup
Create a free account at SinricPro Portal.
Add two "Switch" devices to your dashboard.
Copy your App Key, App Secret, and the Device IDs for both switches.
2. Arduino IDE Setup
Install the ESP8266 Board in your Arduino IDE (Preferences > Boards Manager).
Install the following libraries via the Library Manager:
SinricPro
WebSockets
ArduinoJson
3. Uploading the Code
Copy the provided .ino file from this repository.
Replace the placeholders (Your_WIFI_Name, Your_Sinric_AppKey, etc.) with your actual credentials.
Connect your NodeMCU and click Upload.
⚠️ Troubleshooting & Tips
PIR Warm-up: The SR505 sensor requires 15–60 seconds of "warm-up" time after powering on. During this time, it may give false triggers or no signal.
Voltage Issues: If the PIR sensor is unresponsive, ensure it is connected to the Vin (5V) pin. 3.3V is often insufficient for reliable motion detection.
Baud Rate: Set your Serial Monitor to 115200 to see the debug logs.
Interference: Keep the PIR sensor at least 10cm away from the ESP8266 antenna to avoid WiFi interference causing false motion triggers.
📄 License
This project is open-source. Feel free to use, modify, and distribute it for personal or educational purposes.
Developed by: Indrjeet from iVCOM
