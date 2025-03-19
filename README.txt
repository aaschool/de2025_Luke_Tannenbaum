Free Beer Alarm

This project scans WhatsApp Web for messages containing the phrase "free beer" and triggers an Arduino-based alarm system. It uses Selenium to monitor WhatsApp messages and PySerial to send a signal to the Arduino, activating an LED and a buzzer when "free beer" is mentioned.

Features
- Monitors WhatsApp Web for specific keywords.
- Sends a signal to an Arduino when the keyword is detected.
- Displays a desktop notification using Plyer.

Requirements
- Python 3
- Google Chrome
- ChromeDriver
- Selenium
- WebDriver Manager
- PySerial
- Plyer

Installation

1. Clone the repository:
   git clone https://github.com/yourusername/free-beer-alarm.git
   cd free-beer-alarm

2. Install dependencies:
   pip install selenium webdriver-manager pyserial plyer

3. Ensure ChromeDriver is installed:
   python -m webdriver_manager.chrome

4. Set up WhatsApp Web:
   - Open WhatsApp on your phone.
   - Navigate to "Linked Devices" and scan the QR code when prompted.

5. Connect the Arduino:
   - Ensure the NodeMCU (ESP8266) or Arduino is connected via USB.
   - Upload the appropriate Arduino sketch.

Usage

Run the Python script:
   python free_beer_alarm.py

The program will:
- Open WhatsApp Web and wait for you to scan the QR code.
- Continuously scan for messages containing "free beer."
- Trigger an alarm on the Arduino and display a desktop notification when detected.

Hardware Setup

Components:
- NodeMCU V3 (ESP8266) or Arduino
- Breadboard
- LED
- Buzzer
- Button

Wiring:
Component    | NodeMCU (ESP8266) Pin
------------|-----------------------
Button       | D1
LED          | D2
Buzzer       | D3

Troubleshooting

No Messages Detected:
- Ensure WhatsApp Web is open and logged in.
- Check the XPath in the script (WhatsApp may change its UI).
- Use the Chrome Developer Console (Ctrl + Shift + I on Windows, Cmd + Option + I on Mac) to inspect message elements.

No Port Detected for Arduino:
- Run "ls /dev/cu.*" on macOS or "python -m serial.tools.list_ports" to find the correct port.
- Ensure the Arduino is properly connected.

License
This project is open-source under the MIT License.
