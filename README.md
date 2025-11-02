# ⚡ ESP32 AD8232 OLED ECG Monitor

This project implements a single-lead Electrocardiogram (ECG) monitor using the AD8232 Heart Rate Sensor, an ESP32 microcontroller, and a 128x64 I2C OLED display.

It reads the amplified heart signal, calculates the Beats Per Minute (BPM), and displays both the BPM and a real-time ECG trace directly on the OLED, eliminating the need for a PC or Processing IDE.

## 📌 Hardware Components

* **Microcontroller:** ESP32 Development Board
* **ECG Sensor:** AD8232 Heart Rate Monitor
* **Display:** 128x64 I2C SSD1306 OLED Display
* **Electrode Pads:** 3-Lead ECG cable and pads

## 🔌 Wiring Diagram (ESP32)

| Component Pin | ESP32 Pin | Function |
| :---: | :---: | :--- |
| **AD8232 OUTPUT** | **GPIO 34 (ADC1\_CH6)** | Analog ECG Signal |
| **AD8232 LO+** | **GPIO 32** | Leads Off Positive |
| **AD8232 LO-** | **GPIO 33** | Leads Off Negative |
| **AD8232 3.3V** | **3.3V** | Power Supply |
| **AD8232 GND** | **GND** | Ground |
| **OLED SDA** | **GPIO 21** | I2C Data |
| **OLED SCL** | **GPIO 22** | I2C Clock |
| **OLED VCC** | **3.3V** | Power Supply |
| **OLED GND** | **GND** | Ground |

## 📚 Libraries Required

Ensure these libraries are installed via the Arduino Library Manager:

1.  **Adafruit SSD1306** (For OLED control)
2.  **Adafruit GFX Library** (For graphics core)

## ⚙️ Calibration Note

The **`threshold`** value used for BPM calculation is critical and may need tuning based on your specific sensor placement and body type:

```cpp
int threshold = 550; // Adjust this value.
