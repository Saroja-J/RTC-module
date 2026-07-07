# ⏰ Real-Time Clock (RTC) Module

## 📖 Overview

The **Real-Time Clock (RTC) Module** is designed around the **DS1307 RTC IC** to provide accurate timekeeping for embedded systems. It communicates with the host controller using the **I²C interface** and maintains time even when the main power supply is disconnected using a **CR2032 backup battery**.

In addition to real-time clock functionality, the module includes an **AT24CS01 EEPROM** for storing non-volatile configuration data and a **DS18B20 digital temperature sensor** interface for environmental monitoring.

---

## ✨ Features

- DS1307 Real-Time Clock
- CR2032 Backup Battery Support
- I²C Communication Interface
- 32.768 kHz Crystal Oscillator
- AT24CS01 I²C EEPROM
- DS18B20 Temperature Sensor Interface
- Power Status LED
- Compact and Expandable Design

---

## 🛠️ Hardware Components

| Component | Description |
|-----------|-------------|
| DS1307 | Real-Time Clock IC |
| 32.768 kHz Crystal | RTC Oscillator |
| CR2032 Battery Holder | Backup Power |
| AT24CS01 | 1-Kbit EEPROM |
| DS18B20 | Digital Temperature Sensor |
| Pull-up Resistors | I²C Bus Pull-ups |
| LED | Power Indicator |

---

## 📷 Schematic

<p align="center">
   <img width="1327" height="442" alt="Image" src="https://github.com/user-attachments/assets/00456204-96a5-4e44-a267-f9d02905b3d8" />
</p>

---

## 🏗️ Hardware Architecture

```text
                 +5V
                  │
        ┌─────────────────┐
        │    DS1307 RTC   │
        │                 │
Crystal ── X1/X2          │
Battery ── VBAT           │
        │                 │
        │ SDA      SCL    │
        └────┬────────┬───┘
             │        │
             │        │
      ┌───────────────┐
      │  AT24CS01     │
      │   EEPROM      │
      └───────────────┘
             │
             │
         ESP32 MCU
             │
      DS18B20 Sensor
```

## ⚡ Power Specifications

| Parameter | Value |
|----------|-------|
| Input Voltage | 5V |
| Backup Voltage | 3V (CR2032) |
| Communication | I²C |

---

## 📋 Applications

- Data Logging
- IoT Devices
- Smart Home Automation
- Industrial Controllers
- Attendance Systems
- Battery-backed Embedded Systems
- Time Scheduling Applications

---

## 📌 Design Highlights

- Battery-backed real-time clock
- External 32.768 kHz crystal for accurate timing
- Shared I²C bus for RTC and EEPROM
- Digital temperature monitoring
- Low component count
- Easy integration with ESP32

---

## 🚀 Future Improvements

- Upgrade to DS3231 for higher accuracy
- Add ESD protection
- Add reverse polarity protection
- Configurable EEPROM address selection
