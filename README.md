# Programmable-Bench-Power-Supply

  The programmable bench power supply is designed to deliver high precision and flexibility for various electronics testing and development applications. The project involves designing the entire system from the step-down transformer, rectifier bridge, and smoothing capacitors to the final programmable, high-precision output stages. The key features of this power supply are as follows:

### 1. Dual Programmable Outputs
The power supply provides two independent 24V/100W programmable outputs, each with:
Adjustable voltage, current, and power settings.
Programmable voltage, current, and power limiters to ensure safe operation.
High precision regulation to maintain stable output conditions.

### 2. Advanced User Interface with Touch Display
A touchscreen display serves as the primary user interface, offering:
Full control over voltage, current, and power settings.
Access to programmable limit settings for enhanced safety.
Real-time monitoring of voltage, current, and power for both outputs.
Programmable buttons for quick access to predefined settings.

### 3. Windows Application for Remote Control and Data Logging
A dedicated Windows application is developed to provide full remote control and monitoring capabilities, including:
Complete control over both outputs, including setting voltage, current, and power values.
Data logging functionality, capturing real-time data from both channels.
Excel report generation, allowing users to export data for further analysis.
Graphical visualization of voltage, current, and power trends over time.

### 4. Battery Emulation and Charging Capabilities
The power supply integrates battery emulation and charging functions, making it ideal for battery-powered device testing:
Simulates the behavior of a real battery, allowing devices to be tested under varying conditions.
Provides controlled charging of external batteries, with programmable charging profiles.
All battery parameters are adjustable and monitored via the Windows application.

### 5. Data Monitoring and Statistical Analysis
The system provides comprehensive real-time data monitoring, allowing users to:
Track voltage, current, and power values for each output independently.
Perform statistical analysis on recorded data, including mean, peak, and trend analysis.
Generate customized reports with test data for documentation and further study.

### 6. Safety and Protection Features
Built-in protection mechanisms ensure safe operation and longevity of the power supply:
Overvoltage, overcurrent, and overpower protection prevent damage to connected devices.
Short-circuit protection to avoid accidental damage.
Thermal protection with temperature monitoring and automatic shutdown if overheating occurs.

### 7. High Efficiency and Precision
Designed with low-ripple, high-precision regulation for stable output.
Efficient power conversion and heat dissipation mechanisms to ensure reliable operation.

# Architectural Block Diagrams
[Programmable Power  Supply - Schematic.pdf](https://github.com/user-attachments/files/18824577/Programmable.Power.Supply.-.Schematic.pdf)


## 1) Full Product View

![Picture1](https://github.com/user-attachments/assets/557b1166-3b22-4cfe-a259-850a774c2506)


## 2) Module Placement inside the Enclosure

<img width="1413" alt="Module Placement" src="https://github.com/user-attachments/assets/c7ec76e2-fcda-44e5-bafd-599f3b8a5b32" />


## 3) Power Distributor PCB Block Diagram

![Picture2](https://github.com/user-attachments/assets/b5faaac7-c8da-4e33-8f3e-ddff8b69fc9b)


## 4) Power Output Interface PCB Block Diagram

![Picture3](https://github.com/user-attachments/assets/51ce5579-bff1-4567-99e3-1fd16c07ed46)


## 5) Main Controller PCB Block Diagram (STM32H743)

![Picture4](https://github.com/user-attachments/assets/59370acf-60ff-479b-a2ee-78b988ff33c3)



## Conclusion
This programmable bench power supply is a feature-rich, high-precision instrument tailored for professional electronics testing, prototyping, and research applications. With its dual programmable outputs, touchscreen interface, Windows application, battery emulation, and extensive data logging capabilities, it provides a versatile and powerful tool for engineers and researchers.
