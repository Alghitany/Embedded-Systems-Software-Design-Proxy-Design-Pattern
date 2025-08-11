# Motor Safety Proxy for Arduino Motor Control

## 📌 Overview
This project implements a **Safety Proxy design pattern** on an **Arduino Uno** to control a **DC motor** with enhanced safety features.  
The proxy intercepts motor commands, ensuring they are executed **only** if safety conditions are met—such as no active emergency stop or mechanical limit switch triggered.  

This approach improves **safety, modularity, and maintainability** in embedded motor control systems.

🔗 **View and simulate the project on Tinkercad:**  
[Safety Proxy for Motor/Actuator Control - Tinkercad Simulation](https://www.tinkercad.com/things/9F0yStgIGw5-safety-proxy-for-motoractuator-control/editel?returnTo=https%3A%2F%2Fwww.tinkercad.com%2Fdashboard&sharecode=xSW-dDwg1-uTYr5bYmEzm2RoNlxCVOWcu2Ye993JZ-I)

---

## ✨ Features
- **Proxy Pattern** enforces safety checks before any motor command.
- **Emergency Stop Button** for instant motor shutdown.
- **Limit Switch** to prevent mechanical overrun.
- **LED Indicators** for motor running status and fault conditions.
- **PWM Speed Control** for precise motor speed adjustment.
- **Serial Command Interface** for control and debugging.
- **Layered Architecture** separating motor control logic from safety logic.

---

## 🛠 Hardware Requirements
- Arduino Uno
- L293D Motor Driver IC
- DC Motor
- Limit Switch (Normally Open)
- Emergency Stop Button (Normally Open)
- 2x LEDs (Motor running, Fault)
- Resistors for LEDs
- Breadboard and jumper wires

---

## 🔌 Pin Mapping
| Signal               | Arduino Pin |
|----------------------|-------------|
| Motor IN1            | 7           |
| Motor IN2            | 6           |
| Motor Enable (PWM)   | 9           |
| Limit Switch Input   | 2           |
| Emergency Stop Input | 3           |
| Motor Running LED    | 10          |
| Fault LED            | 11          |

---

## 💻 Software Requirements
- Arduino IDE 1.8.x or later
- Standard Arduino libraries (no external dependencies)
- Simulation Environment: **Tinkercad** (optional)

---
## 🎮 Serial Commands
| Command           | Description |
|-------------------|-------------|
| `f`               | Move forward |
| `r`               | Move reverse |
| `s`               | Stop motor |
| `v<number>`       | Set speed (0-255) |
| `enable`          | Enable motor control |
| `disable`         | Disable motor control |

---

## ⚙️ Setup & Usage
1. **Assemble hardware** according to the provided wiring schematic.
2. **Upload** the Arduino sketch via Arduino IDE.
3. **Open Serial Monitor** at `9600` baud rate.
4. **Control the motor** using commands from the table above.
5. **Test safety features** by pressing the emergency stop or limit switch.

---

## 🧪 Testing
✅ **Motor responds** correctly to forward/reverse/stop commands.  
✅ **Emergency Stop** instantly halts motor and activates fault LED.  
✅ **Limit Switch** stops motion when triggered.  
✅ **LED Indicators** reflect motor and fault states.

---

## 📖 Full Documentation
You can view the **complete detailed documentation** for this project (design, requirements, diagrams, testing results, and future work) here:  
[📄 View Full Project Documentation (PDF)](https://github.com/user-attachments/files/21712417/Motor.Safety.Proxy.Arduino.Documentation.pdf)

---

## 📷 Arduino UNO DC Motor Control System Wiring and Functional Diagram
Below is the wiring and functional diagram for the Arduino UNO DC Motor Control System with safety features:  
<img width="1536" height="1024" alt="Arduino UNO DC Motor Control System Wiring and Functional Diagram" src="https://github.com/user-attachments/assets/8fb53e38-0cad-43ae-9e36-d6d135640f9c" />

---

## 🔌 Circuit Diagram
The following circuit diagram shows the complete wiring setup for the Motor Safety Proxy project:  
<img width="606" height="452" alt="Circuit" src="https://github.com/user-attachments/assets/a0b6de8e-cff2-4ce1-b438-edb166178ddc" />

---

## 📊 System Block Diagram
The following block diagram illustrates the functional flow of the Motor Safety Proxy system:  
<img width="1536" height="1024" alt="Block Diagram" src="https://github.com/user-attachments/assets/aaf34282-a6ef-44c3-874e-8a36b896a28e" />

---

## 🏗 Class Diagram
The following class diagram illustrates the object-oriented structure of the Motor Safety Proxy software architecture:  
<img width="1536" height="1024" alt="Class Diagram" src="https://github.com/user-attachments/assets/b0eed467-3441-4995-ac71-62fc35e27850" />

---

## 🚀 Future Enhancements
- Wireless remote control interface.
- Interrupt-driven safety checks (non-blocking).
- LCD display for real-time system status.
- Support for multiple motors.

---

## 📜 License
This project is open-source. You are free to use, modify, and distribute with proper attribution.
