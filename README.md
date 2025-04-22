# Real-Time Voice Command Recognition on ESP32 with OLED Display

This project runs a TinyML model trained using Edge Impulse on an ESP32 board to recognize spoken voice commands. The recognized command is displayed in real-time on a SH1106 128x64 OLED screen using the U8g2 library.

## 🛠️ Hardware Used

- ESP32 Dev Module
- INMP441 I²S Microphone
- SH1106 128x64 OLED Display (I2C)
- Jumper wires and Breadboard
- USB cable for programming

## 📦 Software Requirements

- Arduino IDE
- ESP32 board support (via Boards Manager)
- Edge Impulse model exported as Arduino library
- Libraries to install via Library Manager:
  - `U8g2`
  - `Adafruit SSD1306`
  - `Adafruit GFX`

## 📁 File Contents

- `edge_impulse_oled_display.ino`: Main sketch that runs inference and shows results on OLED.
- Trained model ZIP from Edge Impulse should be installed as an Arduino library.

## 🔌 Wiring Instructions

### OLED Display (I2C)
| OLED Pin | ESP32 Pin |
|----------|-----------|
| VCC      | 3.3V      |
| GND      | GND       |
| SDA      | GPIO21    |
| SCL      | GPIO22    |

### INMP441 Microphone (I2S)
| Mic Pin | ESP32 Pin |
|---------|-----------|
| VCC     | 3.3V      |
| GND     | GND       |
| SCK     | GPIO25    |
| WS      | GPIO26    |
| SD      | GPIO17    |
| L/R     | GND       |

## 🚀 How to Run the Project

1. Open Arduino IDE.
2. Install required libraries (`U8g2`, `Adafruit SSD1306`, `Adafruit GFX`).
3. Add your Edge Impulse ZIP as a library (`Sketch → Include Library → Add .ZIP Library...`).
4. Open `edge_impulse_oled_display.ino`.
5. Select the correct ESP32 board and COM port under Tools.
6. Click **Upload**.
7. Open Serial Monitor at 115200 baud for logs.
8. Speak one of the trained commands near the microphone.
9. Watch the OLED display update in real-time with the predicted label.

## ✅ Notes

- Model must be trained on 1-second audio clips and exported with Edge Impulse's "Arduino library" format.
- Ensure your Edge Impulse project includes the correct microphone input settings (16kHz, mono, etc).
- You can customize the font, position, and display format using U8g2’s extensive APIs.

## 📷 Demo Link
Include photos or video demo of your setup in action.

https://drive.google.com/drive/folders/1DJyjVCoRY8r977VBq4hr7fjYT17MtLwN?usp=sharing

---

Author: Prithvi Halagere Lokesha | University of Florida | MS in AI Systems
