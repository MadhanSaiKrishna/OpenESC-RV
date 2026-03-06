# OpenESC-RV
### An Open-Source RISC-V Based BLDC Electronic Speed Controller (ESC)

OpenESC-RV is an open-source Electronic Speed Controller (ESC) architecture built around a lightweight RISC-V processor. The project aims to provide a fully programmable, open hardware platform for controlling Brushless DC (BLDC) motors with modern digital protocols such as **DShot**, while remaining compatible with open-source ASIC and FPGA design flows.

The system integrates a RISC-V CPU with dedicated motor-control peripherals including PWM generation, sensor interfaces, and safety monitoring. This architecture enables real-time control of BLDC motors in applications such as **drones, robotics, research platforms, and embedded control systems**.

---

## Motivation

During participation in the **CanSat competition**, we required a **compact, reliable, and low-cost ESC capable of bidirectional BLDC motor control** using modern digital protocols such as **DShot**.

However, most available ESCs were either:

- **Proprietary and closed-source**, preventing modification or deeper integration
- **Optimized for commercial drone stacks**, not research platforms
- **Expensive or difficult to integrate** into custom embedded systems
- **Limited in documentation**, making hardware/software co-design difficult

For research applications such as **satellite payload mechanisms, reaction wheels, propulsion experiments, and small robotics platforms**, a programmable ESC with open architecture is extremely valuable.

This project aims to address that gap by creating a **fully open-source ESC architecture that researchers and students can study, modify, and integrate into their own hardware systems.**

---

## Project Goals

The main objectives of OpenESC-RV are:

- Provide an **open hardware ESC architecture**
- Enable **bidirectional BLDC control using modern digital protocols**
- Support **programmable control using a RISC-V processor**
- Provide a **reproducible open-source silicon design**
- Serve as a **reference design for motor-control ASICs and FPGA implementations**

---

## System Overview

OpenESC-RV integrates a RISC-V processor with specialized motor-control hardware blocks to enable efficient and deterministic BLDC control.

### Core Components

**1. RISC-V Processing Core**

A lightweight RV32I processor executes:

- Motor control algorithms
- Control loops
- Communication protocols
- Telemetry and diagnostics

---

**2. Motor Control Hardware**

Dedicated hardware peripherals handle timing-critical tasks such as:

- Multi-channel PWM generation
- Dead-time insertion
- Duty-cycle modulation
- Commutation control

---

**3. DShot Interface**

The controller supports modern digital ESC communication protocols including:

- **DShot150**
- **DShot300**
- **DShot600**

Features include:

- Bidirectional communication
- Telemetry support
- Error detection

---

**4. Sensor Interfaces**

The system supports multiple sensing methods:

- Hall sensor interface
- Current sensing
- Voltage monitoring
- Optional encoder interface

---

**5. Safety and Monitoring**

Motor control systems require robust protection mechanisms.

The system includes:

- Overcurrent protection
- Undervoltage monitoring
- Thermal shutdown hooks
- Watchdog timer
- Emergency motor cutoff

---

**6. Communication Interfaces**

External control and telemetry interfaces include:

- UART
- SPI
- Debug interface

---


## Potential Applications

OpenESC-RV can be used in several research and embedded systems domains:

- Drone propulsion systems
- Robotics platforms
- Reaction wheel controllers
- CubeSat / CanSat payload mechanisms
- Laboratory motor control experiments
- Embedded motor control ASICs

---

## License

This project is released under the **Apache 2.0 License**.

---

## Acknowledgements

This project description and proposal README.md file is generated using ChatGPT using the following existing open source designs:   
RISC-V ESC Base on CH32V203F8U6:- https://github.com/openwch/RISC-V_ESC  
Ibex RISC-V Core:- https://github.com/lowRISC/ibex 