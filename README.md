# Embedded Systems Internship – Embrizon Technologies

This repository contains the projects completed during my embedded systems internship at **Embrizon Technologies**. The internship focused on Arduino UNO–based circuit design and simulation, covering digital I/O, multiplexed displays, and serial communication — built and tested using Tinkercad Circuits.

**Intern:** Mallampally Jayantha Siva Srinivas

---

## 📌 Projects

### 1️⃣ Four Digit Seven Segment Display

A digital counter built using an Arduino UNO and a 4-digit seven-segment display, incrementing from `0000` to `9999` and updating every second.

**Key Concepts:** Multiplexing, digit control, segment driving via current-limiting resistors, Arduino timing.

- **Components:** Arduino UNO R3, 4× Anode 7-Segment Display, 4× 220Ω Resistor
- **How it works:** Each digit is multiplexed by rapidly cycling through digit-enable pins (`A0`–`A3`) while updating the shared segment pins (`2`–`9`), creating the illusion that all four digits display simultaneously.
- **Highlights:**
  - Custom 7-segment lookup table for digits 0–9
  - `display_N()` function extracts thousands/hundreds/tens/units and refreshes all digits per cycle
  - `segOutput()` handles per-digit segment writing with decimal point support

🔗 [Simulation Link](https://www.tinkercad.com/things/gtVLoft1qYs-4-digit-seven-segment-display?sharecode=yntc__rN8juy7N93fwunfWVeFKNLCGUSuOp86I6SSpM)
🎥 [Simulation Video](https://drive.google.com/file/d/1q9kUHVJHtnfXuqY6fCwOUf5KSMn6PHov/view?usp=drivesdk)

---

### 2️⃣ LED Control Using Serial Monitor

An Arduino-based system that controls an LED and reports status over the Serial Monitor based on user input commands.

**Key Concepts:** Serial communication, conditional logic, digital output control.

- **Components:** Arduino UNO R3, Pushbutton, Red LED, 220Ω Resistor, 10kΩ Resistor
- **How it works:** The Arduino reads characters sent via the Serial Monitor (9600 baud). Sending `1` turns the LED ON, `0` turns it OFF, and any other input returns an "INVALID INPUT" message — all states are echoed back to the Serial Monitor in real time.

🔗 [Simulation Link](https://www.tinkercad.com/things/1uzBLGjUApQ-led-control-using-serial-monitor?sharecode=6uS7lDJ8ZiqjsiBtcWnx3mdl_GvN9OctoK4r_fdpVuoO)
🎥 [Simulation Video](https://drive.google.com/file/d/1psVigUWtypd_7NEZ4cwWUtDoiXfSxHuL/view?usp=drivesdk)

---

## 🛠️ Tools & Technologies

- **Hardware Platform:** Arduino UNO R3
- **Simulation Tool:** Tinkercad Circuits
- **Language:** Arduino C/C++
- **Concepts Covered:** Multiplexing, digital I/O, serial communication, current-limiting resistor design, conditional control logic

## 🎯 Internship Takeaways

Through this internship, I gained hands-on experience in:
- Designing and simulating embedded circuits before physical prototyping
- Writing efficient, pin-minimal multiplexing code for multi-digit displays
- Implementing serial-command-driven control systems
- Debugging real-time hardware-software interaction in a simulated environment

## 🚀 Future Scope

- Extend the seven-segment counter with push-button/sensor-based control
- Add remote monitoring via serial or wireless communication
- Build a stopwatch/countdown timer variant of the display project

---

*Internship completed at Embrizon Technologies — Embedded Systems Track*
