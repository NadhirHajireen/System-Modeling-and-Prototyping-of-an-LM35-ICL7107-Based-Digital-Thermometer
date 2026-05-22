# 🌡️ 2-Digit Digital Thermometer (0–99°C)

A digital thermometer system designed using the **LM35 precision temperature sensor** and **ICL7107 analog-to-digital converter (ADC)** to measure and display temperature directly on **7-segment displays** without using a microcontroller.

---

## 📌 Project Overview

This project implements a complete analog temperature measurement system capable of reading temperatures from **0°C to 99°C**.

The LM35 sensor produces a voltage linearly proportional to temperature (10 mV/°C), and the ICL7107 converts this analog voltage directly into a digital display output.

This system eliminates the need for microcontrollers by using dedicated analog ICs for sensing and display driving.

---

## 🎯 Objective

To design and build a **2-digit digital thermometer** that:

- 🌡️ Measures temperature from 0°C to 99°C  
- 🔌 Uses LM35 as the temperature sensor  
- 📟 Uses ICL7107 for direct 7-segment display driving  
- ⚡ Ensures accurate analog-to-digital conversion through proper voltage scaling  

---

## ⚙️ System Components

- 🌡️ LM35 Precision Temperature Sensor  
- 🔢 ICL7107 ADC with 7-segment driver  
- 📟 Dual 7-segment display  
- 🎚️ Potentiometer (for reference voltage adjustment)  
- 🔋 DC Power Supply  
- 🔌 Passive components (resistors, capacitors)

---

## 🧠 Working Principle

- The **LM35 sensor** outputs an analog voltage proportional to temperature (10 mV/°C)
- The **ICL7107** converts this analog voltage into a numeric display
- The reference voltage (**Vref = 100 mV**) is adjusted so that:
  - 10 mV = 1°C
  - 250 mV = 25°C → Display shows "25"
  - 500 mV = 50°C → Display shows "50"
  - Up to 99°C maximum range

---

## ⚡ System Design Phases

### 🔹 1. Proteus Simulation
- Verified LM35 and ICL7107 integration
- Confirmed correct voltage scaling and display output
- Achieved accurate temperature readings from 0°C to 99°C

---

### 🔹 2. EasyEDA PCB Design
- Designed a professional PCB layout
- Implemented analog star grounding to reduce noise
- Optimized 7-segment display alignment
- Generated final Gerber files for fabrication

---

### 🔹 3. Breadboard Prototype
- Built and tested physical circuit
- Used as intermediate validation before PCB assembly
- Observed unexpected display behavior during testing

---

## 📊 Project Outcome

| Phase              | Status        | Remarks |
|------------------|--------------|---------|
| Proteus Simulation | ✅ Successful | Accurate temperature display with correct scaling |
| PCB Design        | ✅ Completed  | Gerber files generated, layout optimized |
| Breadboard Test   | ❌ Not Functional | Display stuck at "66" regardless of input |

---

## ⚠️ Issue Observed (Breadboard Prototype)

During hardware testing, the display consistently showed **"66"**, regardless of temperature or input voltage.

### 🔍 Possible Causes:
- Improper grounding or noise in analog section  
- Missing or insufficient decoupling capacitors  
- Oscillator instability in ICL7107  
- Voltage reference (Vref) misconfiguration  
- Breadboard parasitic resistance/capacitance effects  

---

## 📈 Key Learnings

- Simulation ≠ real hardware behavior  
- Analog circuits are highly sensitive to noise and grounding  
- Proper PCB design significantly improves stability over breadboard setups  
- Importance of decoupling capacitors in ADC circuits  
- Real-world debugging is essential in analog electronics  

---

## 🚀 Applications

- 🌡️ Temperature monitoring systems  
- 🏭 Industrial sensing applications  
- 🔬 Educational analog electronics experiments  
- 📟 Embedded instrumentation systems  

---

## 👨‍💻 Author

**Nadhir Hajireen**  
🎓 Computer Systems Engineering Student  
🏫 SLIIT  

---

## 📌 Note

This project demonstrates a complete analog-to-digital measurement system using dedicated ICs. It highlights the transition from simulation to PCB design and the challenges encountered during real-world hardware implementation.
