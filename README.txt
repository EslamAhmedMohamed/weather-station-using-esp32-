# ESP32 Weather Station

This project involves creating a weather station using an ESP32 microcontroller, a DHT11 humidity and temperature sensor, a BMP180 pressure sensor, and an SD card module for data logging. The weather station provides real-time sensor readings and allows users to set threshold values for temperature, humidity, pressure, and altitude. If any of these values exceed the set thresholds, an alert email is sent using the ESP32 MailClient library.

## Hardware Setup

### DHT11 Sensor
- Connect Pin 1 (VCC) to 3.3V of ESP32
- Connect Pin 2 (Data) to D15 of ESP32
- Connect Pin 4 (GND) to GND of ESP32

### BMP180 Sensor
- Connect Vin to 3.3V of ESP32
- Connect GND to GND of ESP32
- Connect SCL to Pin 22 (SCL) of ESP32
- Connect SDA to Pin 21 (SDA) of ESP32

### SD Card Module
- Connect GND to GND of ESP32
- Connect VCC to VIN of ESP32
- Connect MISO to Pin G19 of ESP32
- Connect MOSI to Pin G23 of ESP32
- Connect SCK to Pin G18 of ESP32
- Connect CS to Pin G5 of ESP32

## Software Setup

### Libraries
Make sure to install the required libraries using the Arduino Library Manager:
- Adafruit_Sensor
- Adafruit_BMP085
- DHT
- WiFi
- WebServer
- SPI
- SD
- ESP32_MailClient

### Configuration
- Update the Wi-Fi credentials in the `setup` function.
- Set your Gmail credentials and recipient email address in the `sendAlertEmail` function.

## Usage

1. Upload the code to your ESP32 board.
2. Open the Serial Monitor to view ESP32 IP address.
3. Connect to the Wi-Fi network displayed in the Serial Monitor.
4. Open a web browser and enter the ESP32 IP address to view real-time sensor readings.
5. Set threshold values using the provided form.
6. Monitor sensor readings and receive email alerts if thresholds are exceeded.

## Data Logging

Sensor readings are logged to an SD card in a file named `weather_data.txt`.

## Contributions

Contributions to improve and extend this project are welcome! Feel free to fork and create pull requests.


