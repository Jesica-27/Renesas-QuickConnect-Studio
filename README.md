# 🔌 Renesas QuickConnect Studio Experiments

This repository contains a collection of **embedded systems experiments and projects** developed using the  
**Renesas QuickConnect Beginner Kit v2.0** and **Renesas QuickConnect Studio (QCStudio)**.

These projects demonstrate the fundamentals of **microcontroller programming, GPIO control, and interrupt-based applications** using Renesas RA series microcontrollers.

---

## 📋 Table of Contents

- Introduction  
- Hardware & Software Requirements  
- Getting Started with QuickConnect Studio  
- Project List  
- Build & Flash Procedure  
- Future Scope  
- Author  

---

## 📘 Introduction

Renesas QuickConnect Studio is a rapid prototyping platform that helps in reducing development time and simplifies embedded application development.  

This repository documents and implements a set of **beginner-level embedded experiments** such as:

- LED blinking
- External LED control
- Button (switch) interfacing
- Sequential LED control
- Interrupt-based LED toggling

These experiments help in building a **strong foundation in embedded systems development** using Renesas RA MCUs.

---

## 🧰 Hardware & Software Requirements

### 🔧 Hardware
- Renesas QuickConnect Beginner Kit v2.0 (BGK-RA6E2)
- USB Cable

### 💻 Software
- Renesas QuickConnect Studio (QCStudio)
- SEGGER J-Flash Lite
- Embedded C Toolchain
- Windows 10/11

---

## 🚀 Getting Started with QuickConnect Studio

1. Launch **Renesas QuickConnect Studio**
2. Login using your **MyRenesas account**
3. Click **Create New Project**
4. Select:


Application Configuration → IoT → Other → Blink LEDs (Baremetal)

5. Enter project name and create project
6. Click **Build Project**
7. After build:
- Go to `Debug` folder
- Select the `.srec` file
- Flash it using **SEGGER J-Flash Lite**

---

## 🧪 Projects Implemented

### ✅ Project 1: Blinking Inbuilt (Onboard) LED

- Blinks the onboard LED using GPIO
- Verifies toolchain, board, and build process

---

### ✅ Project 2: Blinking External LED

- Uses an external LED connected to pin **P105**
- Pin configuration is verified from:


ra_cfg/fsp_cfg/bsp/bsp_pin_cfg.h

- Demonstrates external GPIO control

---

### ✅ Project 3: Blinking Inbuilt LED + External LED

- Blinks multiple LEDs **sequentially**
- Demonstrates multi-GPIO control and timing logic

---

### ✅ Project 4: Toggle External LED using Button (Interrupt)

- Uses **External IRQ (ICU)**
- Button press toggles LED state
- Uses:
- `icu_ep.c`
- `icu_ep.h`
- Demonstrates:
- Interrupt configuration
- GPIO output control
- State toggling logic

---

## 🔨 Build & Flash Procedure

1. Click **Build QCStudio Project**
2. Go to:


Project → Debug → *.srec file

3. Connect board using USB
4. Open **SEGGER J-Flash Lite**
5. Select device and flash the `.srec` file
6. Reset board and observe output

---

## 🗂 Repository Structure

```text
Renesas-QuickConnect-Projects/
│
├── Beginner/
│   ├── BuiltIn LED/
│   ├── External_LED_Blinking/
│   ├── Blinking Inbuilt LED1 + LED2 + External LED/
│   └── Switch_with_LED/
│
├── Intermediate/   (coming soon)
├── Advanced/       (coming soon)
└── README.md

🎯 Learning Outcomes

GPIO configuration and control

LED and Switch interfacing

External interrupt handling

Embedded C project structure

Renesas RA MCU development workflow

🚀 Future Scope

This repository will be expanded with:

UART, I2C, SPI communication

Timers and PWM

ADC and sensor interfacing

Low-power modes

FreeRTOS projects

IoT and Edge AI applications
