README
📌 DHT22 Data Logger

This project is an embedded system that collects environmental data using a DHT22 sensor and stores it on an SD card in CSV format for later analysis.

⚙️ Features
Reads temperature (°C) and humidity (%)
Logs data every 60 seconds
Saves data to datalog.csv on SD card
Uses non-blocking timing (millis())
Handles sensor and SD card errors
Outputs logs to Serial Monitor
🧰 Hardware Used
Arduino Uno
DHT22 sensor
SD card module
SD card (FAT16/FAT32)
Breadboard & jumper wires
10kΩ resistor
🔌 Wiring
DHT22
VCC → 5V
GND → GND
DATA → Pin 2
10kΩ resistor between VCC and DATA
SD Card Module (SPI)
VCC → 5V
GND → GND
CS → Pin 10
MOSI → Pin 11
MISO → Pin 12
SCK → Pin 13
📂 Data Format

Data is saved in CSV format:

time_sec,temperature_c,humidity
0,24.1,58.2
60,24.3,57.9
120,24.2,58.1
🚀 How It Works
Initializes sensor and SD card
Creates datalog.csv if it doesn’t exist
Reads data every 60 seconds
Saves each reading to SD card
Prints logs to Serial Monitor
⚠️ Common Issues
SD card not detected → check wiring & format
Sensor returns NaN → wiring or missing pull-up resistor
File not saving → ensure SD module CS pin is correct
🔧 Future Improvements
Add RTC module for real timestamps
Store min/max values
Visualize data with Python
Use ESP32 for wireless logging
