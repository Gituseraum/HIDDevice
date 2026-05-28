# <div align="center">🛩️ Blue Pill USB HID Joystick</div>
### <div align="center">2‑Axis + 4‑Button Flight Simulator Controller</div>

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
- **Springs** (for joystick centering)  
- **Universal joint** (for X/Y gimbal movement)  
- **10 mm steel/aluminum rod** (joystick shaft)  

---

## 🔧 How I Made My Fusion Models

I designed the joystick mechanism in **Autodesk Fusion 360** using these steps:

1. **Created the base plate**  
   - Simple rectangular sketch  
   - Added mounting holes for the Blue Pill and potentiometers  

2. **Designed the gimbal system**  
   - Used a **universal joint** model to allow smooth X/Y rotation  
   - Added mounting brackets for the potentiometer arms  

3. **Added the joystick shaft**  
   - Modeled a **10 mm rod**  
   - Added a top grip and screw hole  

4. **Added centering springs**  
   - Two springs placed at 90°  
   - Anchored to the frame and joystick arm  

5. **Exported STL files**  
   - Printed on a standard FDM printer  
   - Used M3 screws for assembly  

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

## 🔌 Wiring (ASCII Diagram)


      +3.3V ---- Pot X ---- GND
                    |
                   PA0

      +3.3V ---- Pot Y ---- GND
                    |
                   PA1


   PB0 ---- Button 1 ---- GND
   PB1 ---- Button 2 ---- GND
   PB10 --- Button 3 ---- GND
   PB11 --- Button 4 ---- GND


---

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

## 📜 License (MIT)

Copyright (c) 2025

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND.

