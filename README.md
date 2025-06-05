# 📚 RFID-Based Attendance Monitoring System

An automated attendance tracking system using RFID technology. This project utilizes RFID tags assigned to individuals, an RFID reader to scan the tags, and a microcontroller (Arduino Uno) to log attendance data with timestamps. It provides a fast, accurate, and contactless method for attendance monitoring in institutions and organizations.

---

## 📝 Description

The RFID-Based Attendance Monitoring System allows students or employees to mark their attendance by scanning their unique RFID cards. Each scan records the RFID tag ID and timestamp, displaying the result on an LCD and optionally storing it for future reference. The system ensures quick identification, reduces manual entry errors, and enables real-time logging.

---

## 🔧 Features

- 📛 Unique RFID tag identification
- 📆 Real-time date and time stamping (with optional RTC module)
- 🖥 LCD display for scan confirmation
- 💾 Optional data logging to SD card or serial monitor
- 🚫 Unauthorized tag detection alert
- ⏱ Fast and contactless operation

---

## 🧩 Components Used

| Component                 | Quantity |
|--------------------------|----------|
| Arduino Uno              | 1        |
| RFID Reader (RC522)      | 1        |
| RFID Tags/Cards          | Multiple |
| 16x2 LCD with I2C Module | 1        |
| Buzzer (optional)        | 1        |
| RTC Module (DS3231)      | 1 (optional) |
| SD Card Module (optional)| 1        |
| Breadboard & Jumpers     | As needed |

---

## 🔌 Wiring Overview

| Component        | Arduino Pin |
|------------------|-------------|
| RC522 SDA        | D10         |
| RC522 SCK        | D13         |
| RC522 MOSI       | D11         |
| RC522 MISO       | D12         |
| RC522 RST        | D9          |
| LCD SDA          | A4          |
| LCD SCL          | A5          |
| Buzzer (opt.)    | D8          |
| RTC SDA/SCL      | A4/A5       |
| SD Card Module   | SPI Pins    |

> Note: Use the SPI library for RFID reader and I2C library for LCD/RTC.

---

## 🚀 Getting Started

1. Clone this repository or download the ZIP file.
2. Open the code in Arduino IDE.
3. Install required libraries:
   - MFRC522
   - LiquidCrystal_I2C
   - RTClib (if using RTC)
   - SPI, Wire (built-in)
4. Upload the sketch to your Arduino board.
5. Open Serial Monitor to view attendance logs (if enabled).
6. Scan RFID tags/cards to mark attendance.

---

## 💻 Code Overview

- Initializes RFID reader and LCD
- Reads RFID tag UID on scan
- Compares against authorized UIDs
- Displays message on LCD and logs data
- Optional: logs to SD card or serial port with timestamp

---

## 📸 Demo / Screenshots

_Add photos or videos of your working project here._

---

## 💡 Future Enhancements

- Web-based dashboard for viewing logs
- Wi-Fi support using ESP8266/ESP32
- Email/SMS notifications on scan
- Integration with school management software

---

## 📄 License

This project is licensed under the MIT License. Feel free to use and modify it for educational or personal use.

---

## 🙌 Credits

- RFID MFRC522 Library by Miguel Balboa
- RTClib by Adafruit
- Inspired by automation needs in education and workplace environments
