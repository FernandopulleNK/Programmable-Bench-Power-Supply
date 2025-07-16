# Smart Programmable Bench Power Supply  
*(Individual Project – EN2160 Electronic Design Realization)*  

---

## 📖 Project Overview
A **smart, programmable dual-channel bench power supply** for electronics prototyping and testing.  
Designed to combine **high accuracy, advanced features, and cost-effectiveness**, this system addresses the gap between **expensive lab-grade instruments** and **limited low-cost models**.

---

## 💡 Motivation
Reliable bench power supplies are essential in any hardware development environment.  
- **Professional-grade supplies** offer exceptional performance but cost several hundred dollars.  
- **Budget alternatives** lack accuracy, programmability, and safety features.  

This project delivers an **affordable, modular, and precise programmable power supply**, featuring **touchscreen UI**, **PC control**, and **advanced power management**.

---

## ✅ Key Features
- **Dual Outputs:**  
  - Mode 1: 24V / 3A  
  - Mode 2: 6V / 10A  
- **Control Modes:** Constant Voltage (CV) & Constant Current (CC)  
- **Precision:**  
  - Voltage: 5mV (6V mode), 30mV (24V mode)  
  - Current: 1mA (3A mode), 10mA (10A mode)  
- **Interfaces:**  
  - 5” Touchscreen  
  - Windows GUI over USB  
- **Advanced:**  
  - Battery emulation  
  - Programmable charging profiles  
  - Data logging  

---

## 📐 Project Specifications
| Parameter            | Value                                  |
|----------------------|----------------------------------------|
| Channels            | 2                                      |
| Modes               | 24V/3A & 6V/10A                       |
| Voltage Resolution  | 5mV (6V), 30mV (24V)                  |
| Current Resolution  | 1mA (3A), 10mA (10A)                  |
| Display             | 5” Touchscreen                        |
| Connectivity        | USB for PC GUI                        |
| MCU                 | STM32H743 (Cortex-M7, 480MHz)         |

<img width="700" height="963" alt="Hardware Architecture - Block diagram" src="https://github.com/user-attachments/assets/b73d6dce-b184-4ece-a6cd-b3dd50cfc6a4" />


---

## 🛠 Methodology & Engineering Approach

### 1️⃣ **Modular PCB Architecture**
The system is split into **three custom PCBs**:
- **Power Distributor PCB:** AC to DC conversion, buck regulation, auxiliary rails  
- **Output Interface PCB:** Linear regulation, sensing, filtering, and relays  
- **Controller Unit PCB:** STM32 MCU, UI interface, and control logic  

**Why Modular?**
- Better EMI performance  
- Easier debugging and testing  
- Thermal isolation between power and control sections  
- Scalable and maintainable design  

---

## 🔍 Hardware Details

---

### **1. Power Distributor PCB**
**Functions:**
- AC-DC rectification, filtering  
- High-current buck regulation  
- Auxiliary power rails (12V & 7V)  
- Relays for buck bypass mode  

**Block Diagram:**  

 <img width="700" height="914" alt="Power Distributor PCB - Block Diagram" src="https://github.com/user-attachments/assets/d290f37e-f387-40ff-9647-15cdca63ae22" />


**PCB Layout:** 

<img width="400" height="400" alt="Power Distributor PCB Layout - Top Layer" src="https://github.com/user-attachments/assets/e93f41e9-bede-4ab4-b2be-e0aac31080c0" />
<img width="400" height="400" alt="Power Distributor PCB Layout - Top Inner Layer" src="https://github.com/user-attachments/assets/d5ce6681-371e-4e1b-af04-bc639c326360" />
<img width="400" height="400" alt="Power Distributor PCB Layout - Bottom Layer" src="https://github.com/user-attachments/assets/e9b5f7ba-7eba-4ac8-8932-0f4bdc4d5226" />
<img width="400" height="400" alt="Power Distributor PCB Layout - Bottom Inner Layer" src="https://github.com/user-attachments/assets/dab874da-8073-404b-beba-46f8d0ac555e" />


**3D View:**  
<img width="420" height="817" alt="Power Distributor PCB 3D View - Side View 02" src="https://github.com/user-attachments/assets/5e952f2d-e80f-4d60-bcba-8e8fabf7c06c" />
<img width="500" height="804" alt="Power Distributor PCB 3D View - Side View 01" src="https://github.com/user-attachments/assets/6f35362c-bc2d-4d4a-81f5-615525b0226f" />



---

### **2. Output Interface PCB**
**Functions:**
- Linear regulation using MJH6284G power BJT  
- Voltage & Current sensing (INA226)  
- Low-pass LC filter for ripple suppression  
- Relay-based shunt switching for range selection  

**Block Diagram:**  

 <img width="1686" height="670" alt="Output Interface PCB - Block Diagram" src="https://github.com/user-attachments/assets/e2d53257-4aee-4854-a01e-8ef445b4b84c" />


**PCB Layout:** 

<img width="400" height="939" alt="Output Interface PCB Layout - Top Layer" src="https://github.com/user-attachments/assets/436f51fa-f43b-4c5c-b7da-391588aa11da" />
<img width="400" height="937" alt="Output Interface PCB Layout - Top Inner Layer" src="https://github.com/user-attachments/assets/980e21c7-872e-402b-adbd-1beef56d5874" />
<img width="400" height="937" alt="Output Interface PCB Layout - Bottom Layer" src="https://github.com/user-attachments/assets/85ccb009-2601-4f50-b37e-80e0c3986a75" />
<img width="400" height="940" alt="Output Interface PCB Layout - Bottom Inner Layer" src="https://github.com/user-attachments/assets/8aee27e6-e114-458c-a376-8468a9265b1e" />
 
 

**3D View:**  

 <img width="1000" height="870" alt="Output Interface PCB 3D View - Side View " src="https://github.com/user-attachments/assets/62876d59-c65f-4121-b9f4-1ddc07585489" />
<img width="500" height="999" alt="Output Interface PCB 3D View - Bottom View " src="https://github.com/user-attachments/assets/c4f00e34-cf26-4a4c-ba80-952d202d9e87" />
<img width="500" height="999" alt="Output Interface PCB 3D View - Top View " src="https://github.com/user-attachments/assets/b5e36722-7831-4427-8872-270ffa1aba89" />


---

### **3. Controller Unit PCB**
**Functions:**
- STM32H743 MCU for real-time control  
- DAC outputs for voltage reference  
- I²C, SPI, UART communication to PCBs & GUI  
- Touchscreen & encoder interface  
- USB CDC for PC control  

**Block Diagram:** 

<img width="700" height="800" alt="Controller Unit PCB - Block Diagram" src="https://github.com/user-attachments/assets/61bc9ec9-3af0-4ea6-8678-951fe56d8629" />



**PCB Layout:**  

<img width="400" height="922" alt="Controller Unit PCB Layout - Top Layer" src="https://github.com/user-attachments/assets/d34c07d7-27ab-4e7c-a4eb-e8be88862431" />
<img width="400" height="921" alt="Controller Unit PCB Layout - Top Inner Layer" src="https://github.com/user-attachments/assets/2c0b94e2-121f-4bc8-a447-c9006694f49d" />
<img width="400" height="920" alt="Controller Unit PCB Layout - Bottom Layer" src="https://github.com/user-attachments/assets/19143034-f379-425d-a08d-14e001fc8e36" />
<img width="400" height="925" alt="Controller Unit PCB Layout - Bottom Inner Layer" src="https://github.com/user-attachments/assets/40db2b78-5c72-436f-912d-329c487857d7" />


**3D View:**  

<img width="500" height="999" alt="Controller Unit PCB 3D View - Top View" src="https://github.com/user-attachments/assets/a18da3da-b437-4703-875f-8736ee297895" />
<img width="500" height="1000" alt="Controller Unit PCB 3D View - Bottom View" src="https://github.com/user-attachments/assets/da6ceda9-e31f-44bb-aae9-5f499dc8228d" />
<img width="1000" height="925" alt="Controller Unit PCB 3D View - Side View" src="https://github.com/user-attachments/assets/75223888-c5fe-47f3-92a3-5162ddd2505f" />


---
