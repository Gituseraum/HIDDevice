#!/usr/bin/env python3
# This script prints the full README.md content.
# You can run it to regenerate README.md automatically.

readme = r"""
# 🛩️ Blue Pill USB HID Joystick  
### 2‑Axis + 4‑Button Flight Simulator Controller

This project turns an **STM32 Blue Pill (STM32F103C8)** into a **USB HID joystick** using the Arduino STM32 core and USBComposite HID library.

It provides:

- 2 analog axes (X/Y) using potentiometers  
- 4 digital buttons  
- USB HID joystick recognized by Windows, Linux, and macOS  
- Smooth ADC → HID mapping  
- Fully open‑source firmware  

---

## ✨ Features

- USB HID Joystick (no drivers required)  
- 2 analog axes (0–255 HID range)  
- 4 buttons (active‑low, internal pull‑ups)  
- Low‑latency USB reports  
- Clean, readable, well‑commented firmware  

---

## 🧰 Hardware Required

- STM32F103C8 “Blue Pill”  
- 2× 10k potentiometers  
- 4× momentary push buttons  
- USB Mini‑B cable  
- Jumper wires  

---

## 🔌 Wiring

### **Analog Axes**
| Function | Pin | Notes |
|---------|-----|-------|
| X Axis  | PA0 | Potentiometer wiper |
| Y Axis  | PA1 | Potentiometer wiper |

Outer legs → **3.3V** and **GND**

### **Buttons**
| Button | Pin | Wiring |
|--------|------|--------|
| BTN1 | PB0 | Connect to GND (internal pull‑up enabled) |
| BTN2 | PB1 | Connect to GND |
| BTN3 | PB10 | Connect to GND |
| BTN4 | PB11 | Connect to GND |

---

## 🛠️ Software Setup

1. Install **Arduino IDE**  
2. Install **STM32duino core**  
3. Select board:  
   **Tools → Board → Generic STM32F103C8**  
4. Set USB mode to:  
   **USB Composite (HID)**  
5. Install the **USBComposite** library  
6. Upload using HID bootloader or ST‑Link  

---
