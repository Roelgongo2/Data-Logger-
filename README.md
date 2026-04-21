🧪 DHT22 Data Logger (Arduino)

A complete embedded system that reads environmental data using a DHT22 sensor, displays it in real-time on an OLED screen, and logs it to an SD card in CSV format for later analysis.

🚀 Features
📡 Reads temperature and humidity from DHT22
💾 Logs data to SD card (CSV format)
🖥 Displays live data on SSD1306 OLED
⏱ Non-blocking timing using millis()
⚠ Basic error handling for sensor and SD card
📊 Ready for data analysis (Python, Excel, etc.)
🔌 Hardware Used
Arduino Uno
DHT22 Temperature & Humidity Sensor
SSD1306 OLED Display (I2C)
SD Card Module (SPI)
MicroSD Card
🔗 Wiring
Component	Pin	Arduino
DHT22	DATA	D2
OLED	SDA / SCL	A4 / A5
SD Card	CS	D10
SD Card	MOSI / MISO / SCK	D11 / D12 / D13
📂 Output Format

Data is saved in data.csv:

time_seconds,temperature_c,humidity_percent
10,23.4,45.2
20,23.5,44.9
🧠 How It Works
The system reads sensor data every 10 seconds
Data is:
displayed on OLED
printed to Serial Monitor
saved to SD card
Timing is controlled using millis() to avoid blocking the system
⚠ Error Handling
Detects failed DHT22 readings
Detects SD card initialization errors
Prevents writing invalid data
🔧 Possible Improvements
Add RTC module (DS3231) for real timestamps
Improve data filtering (remove noisy readings)
Add buttons for start/stop logging
Send data wirelessly (WiFi/Bluetooth)
Create real-time dashboard
📈 Next Step

Use the generated CSV file to:

plot graphs (Python / Excel)
analyze trends
build a full monitoring system
🧠 Learning Outcomes

This project covers:

Embedded programming (Arduino)
Sensor integration
SPI & I2C communication
Data logging systems
Real-time display systems
