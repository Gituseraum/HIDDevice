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

## <div align="center">🖼️ Fusion 360 Renders</div>

Upload your renders into the repo and replace the filenames:

![Fusion Render 1](images/fusion_render_1.png)
![Fusion Render 2](images/fusion_render_2.png)

---

## <div align="center">📸 Joystick Photos</div>

Add real photos of your build:

![Joystick Photo 1](images/joystick_photo_1.jpg)
![Joystick Photo 2](images/joystick_photo_2.jpg)

---

## <div align="center">📐 Wiring Diagram (Image)</div>

Add your wiring diagram image here:

![Wiring Diagram](images/wiring_diagram.png)

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
- **Universal joint** (for X/Y gimbal)  
- **10 mm rod** (joystick shaft)  

---

## 🔧 How I Made My Fusion Models

I designed the joystick mechanism in **Fusion 360**:

1. Created the base plate with mounting holes  
2. Designed the gimbal using a **universal joint**  
3. Modeled the **10 mm joystick rod**  
4. Added **centering springs** at 90°  
5. Exported STLs and 3D‑printed the parts  

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

