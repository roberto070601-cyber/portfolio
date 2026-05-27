# [Roberto Carlos Barajas] | Electrical Engineer
**Hardware Integration • Test Operations • Power Systems**
San Joaquin, CA | [robertocbarajas11@gmail.com] | 

---

## About Me
I am an Electrical Engineering graduate from California State University, Fresno, specializing in the design, testing, and implementation of complex hardware systems. My engineering philosophy revolves around a hands-on approach: translating raw schematics into highly optimized, physical architectures. From precision PCB layout and structural battery pack manufacturing to industrial-grade electromechanical test operations, I focus on building reliable hardware that safely operates under demanding real-world conditions.

As a bilingual engineer fluent in both English and Spanish, I leverage clear, precise technical communication to collaborate across multi-disciplinary teams, coordinate factory floor operations, and draft professional documentation. Whether debugging an isolated data-acquisition telemetry loop or operating 220V industrial machinery, I thrive in fast-paced environments that require rapid problem-solving and rigorous safety execution.

---

## Technical Skill Inventory

| Hardware & Fabrication | Testing & Automation | Software & Tools |
| :--- | :--- | :--- |
| • High-Voltage Battery Assembly<br>• Capacitive Spot Welding<br>• Precision Soldering & Crimping<br>• Custom Cable Harnessing<br>| • Hardware-in-the-Loop (HITL)<br>• Data Acquisition (DAQ) Setup<br>• Transistor-Level Circuit Analysis<br>• Calibration & Root Cause Analysis<br>• Industrial Safety Operations | • C / C++ (STM32, ESP32)<br>• Python (Test Automation)<br> • NI Multisim / Ultiboard<br>• LaTeX (Technical Reporting) |

---

## Flagship Projects

### 1. Dual-Microcontroller 10S3P Battery Management System
*Custom STM32/ESP32 power delivery network featuring pure nickel spot welding, galvanic isolation, and automated web-server telemetry dashboards.*

**The Objective**
* Engineered and assembled a custom Battery Management System (BMS) to monitor, balance, and protect a 36V, 9Ah lithium-ion power system utilizing a 10S3P configuration of Samsung INR18650-30Q cells.
* Designed a dual-microcontroller architecture: an STM32 handles strict real-time analog sensing and safety cutoffs, while a galvanically isolated ESP32 manages high-level data logging and wireless telemetry.

**Hardware Assembly & Architecture**
* **Physical Cell Integration:** Constructed the structural battery pack using custom capacitive spot welding. Routed pure nickel strips in a serpentine layout to minimize series resistance and prevent localized cell heating during high-current draw.
* **Custom PCB Layout:** Designed the monitoring and controller boards adhering to IPC-2221 standards. Implemented strategic ground plane separation and used an Everlight EL3H7-G optocoupler to ensure a 3750 Vrms galvanic barrier between the high-voltage battery domain and the 3.3V logic domain.
* **Thermal Management:** Engineered a dedicated passive balancing board utilizing AO3400A MOSFETs and 18-ohm, 2W surface-mount bleed resistors to safely dissipate excess charge and maintain strict voltage equilibrium.

**Test Execution & Failure Analysis**
* **Load Testing & Validation:** Executed a 10A constant current (CC) continuous discharge test. Verified the hardware's safety response by capturing the undervoltage protection circuit triggering precisely at the 30.0V threshold, successfully severing the discharge contactors.
* **Root Cause Analysis (Thermal Short):** During initial integration, the passive balancing board suffered a short circuit due to an unevenly cut aluminum heat sink contacting live pins. Diagnosed the failure, machined a flush, symmetrical heat sink block, and revised the mounting layout to permanently resolve the thermal interface issue.
<table>
  <tr>
    <td align="center">
      <img width="400" alt="Screenshot 2026-05-26 at 12 30 53 PM" src="https://github.com/user-attachments/assets/7985ff5d-07c6-431f-964b-1030d3b2b0f4" />
      <br>
      <em>Figure 1: Controller Board and Batttery Monitoring Board Sucessfully displaying the data Pack Data.</em>
    </td>
    <td align="center">
      <img width="400" alt="Screenshot 2026-05-26 at 12 31 09 PM" src="https://github.com/user-attachments/assets/42b619a9-980c-4b4d-95a6-79bad97833e1" />
      <br>
      <em>Figure 2:User Dashboard Showcasing Invdividual Cell Voltages. total pack voltage, and temperature of the cells..</em>
    </td>
  </tr>
   <tr>
    <td align="center">
      <img width="1029" height="407" alt="Screenshot 2026-05-26 at 12 32 08 PM" src="https://github.com/user-attachments/assets/181d48b2-7863-4dd0-a97e-cba735853c4d" />
      <br>
      <em>Figure 3: Spot Welded Nickel Strips onto Cells.</em>
    </td>

  <tr>
    <td align="center">
      <img width="690" height="465" alt="Screenshot 2026-05-26 at 12 32 21 PM" src="https://github.com/user-attachments/assets/708210de-58c7-4317-9145-f2b6cc13d987" />
      <br>
      <em>Figure 4: completed 10S3P battery pack.</em>
    </td>


</table>

### 2. Transistor-Level Active Filter Design & Simulation
*A mathematical and discrete simulation analysis of a two-pole low-pass Butterworth filter utilizing the internal macro-stages of an LM741 op-amp.*

**The Objective**
* Designed, calculated, and simulated a Sallen-Key two-pole low-pass Butterworth filter targeting a precise high-frequency cutoff.
* Executed advanced Bode plot simulations to verify the frequency response, confirming the mathematical expectation of a -40 dB/decade roll-off past the cutoff frequency to achieve a maximally flat magnitude response in the passband.

**Transistor-Level Analysis & Simulation**
* **Beyond Ideal Models:** Rather than relying on a standard "black box" ideal op-amp model, the filter was constructed and simulated using the massive internal transistor-level equivalent circuit of the LM741.
* **Stage-by-Stage Verification:** Analyzed how specific discrete internal stages dictate macro-level filter performance. This included verifying the high-impedance differential input stage, evaluating the dominant pole stabilization provided by the gain stage's internal Miller compensation capacitor, and mapping the signal through the class-AB complementary output stage.

**Component Selection & Mathematical Validation**
* Derived the necessary passive component values using standard Butterworth capacitor ratios (C3 = 1.414C and C4 = 0.707C) to perfectly shape the filter's damping factor and quality factor (Q).

<table>
  <tr>
    <td align="center">
      <img width="704" height="381" alt="Screenshot 2026-05-26 at 1 32 07 PM" src="https://github.com/user-attachments/assets/da1fbf64-4dc5-41b4-b851-47d20fc74b60" />
      <br>
      <em>Figure 4: The standard ideal representation of the two-pole low-pass filter.</em>
    </td>
    <td align="center">
      <img width="1199" height="575" alt="Screenshot 2026-05-26 at 1 34 36 PM" src="https://github.com/user-attachments/assets/d0f90e27-fb16-4c2a-ac34-42110d8c645f" />
      <br>
      <em>Figure 5: The filter simulated using the full discrete transistor-level architecture of the LM741.</em>
    </td>
  </tr>
  <tr>
    <td align="center" colspan="2">
      <img width="1128" height="531" alt="Screenshot 2026-05-26 at 1 36 08 PM" src="https://github.com/user-attachments/assets/923b943a-a6da-490b-9858-85905dc0056b" />
      <br>
      <em>Figure 6: AC Sweep Bode plot confirming the -40 dB/decade magnitude roll-off. </em>
    </td>
  </tr>
</table>

### 3. Electromechanical Test Operations: DC Shunt-Wound Generators
*Characterization of a 300W industrial generator platform under 220V load testing, transient analysis, and magnetic field polarity manipulation.*

**The Objective**
* Characterized the electromechanical performance and load characteristics of a 300W industrial DC Shunt-wound generator under varying rotational speeds, excitation currents, and polarity states.

**Test Infrastructure & Execution**
* **Hardware-in-the-Loop Integration:** Safely wired and operated a mechanical test bed utilizing 210V-220V input supplies, coupling guards, and variable load resistors.
* **Data Acquisition (DAQ):** Configured ActiveServo software, alongside digital multimeters and field regulators, to capture real-time telemetry from the rotating machinery. 

**Data Analysis & Physical Validation**
* **Load Characterization:** Executed constant-speed load testing at 2000 RPM to map the generator's power curve. Identified the system's peak power limit of 148.7W at 1.2A of armature current, correctly attributing the subsequent voltage collapse to internal ohmic losses and armature reaction. 
* **Electromagnetic Validation:** Verified theoretical electromagnetic principles on physical hardware by reversing the exciter winding polarity, successfully observing the output voltage cleanly invert from 187.5V to -187.1V.

<table>
  <tr>
    <td align="center">
      <img width="338" height="455" alt="Screenshot 2026-05-26 at 1 58 23 PM" src="https://github.com/user-attachments/assets/d72255cd-3148-4640-aa6b-0760f6297adc" />
      <br>
      <em>Figure 7: Hardware-in-the-loop test bench configuration for the 300W DC generator, detailing the 220V armature and excitation circuit routing.</em>
    </td>
    <td align="center">
      <img width="428" height="249" alt="Screenshot 2026-05-26 at 1 59 58 PM" src="https://github.com/user-attachments/assets/ce442c4b-56f7-422b-8322-8ab7d0b64240" />
      <br>
      <em>Figure 8: Load characteristics DAQ telemetry at 2000 RPM, demonstrating peak power output before armature reaction dominance.</em>
    </td>
  </tr>
</table>

### 4. PLC Automated Carwash Project

**Authors:** Roberto Barajas, Jesus Barajas, Eduardo Lopez  
**Course:** ECE 119L Programmable Logic Controllers (Fall 2025)

## 📌 Project Overview
This project simulates an automated car wash system using a Programmable Logic Controller (PLC). It controls a full wash cycle utilizing timers, counters, and ladder logic to manage different stages of the wash. The system also allows the user to select between Tier 1 and Tier 2 wash modes.

## 🛠️ Hardware and Software
* **Software:** PLC Simulator Online
* **Hardware / I/O:** PLC Trainer push buttons (Start, Stop, Tier 1, Tier 2, Reset) and Indicator lights (Water, Soap, Wax, Blower, Conveyor, Status)

## ⚙️ PLC Control Logic
The system is built on standard PLC ladder logic principles:
* **Start/Stop Latch:** Controls overall system power.
* **Memory Bits:** Stores the user's selection for a Tier 1 or Tier 2 wash.
* **TON Timer:** Runs a complete 50-second wash cycle.
* **CTU Counter:** Tracks the number of completed wash cycles.
* **Comparison Logic:** Controls physical outputs based on the elapsed time of the TON timer.

## ⏱️ Wash Sequence and Timing (50-Second Cycle)
Outputs turn ON/OFF automatically using timer comparisons:
* **0 - 10 s:** Water (Pre-rinse)
* **10 - 25 s:** Soap
* **25 - 35 s:** Water (Final rinse)
* **35 - 40 s:** Wax *(Tier 2 only)*
* **40 - 50 s:** Blower (Drying)

## 🚦 Indicators & Maintenance Features
* **Red Light:** Indicates the system is active during a wash.
* **Green Light:** Indicates the wash is complete and the system is ready for the next car.
* **Car Counter:** Increments after each successful wash cycle.
* **Maintenance Light:** Illuminates when the car counter reaches its preset limit, signaling that maintenance is required.

## 🔗 Live Simulation
You can view and interact with the live PLC ladder logic simulation here:  
[PLC Simulator Online - Automated Car Wash](https://app.plcsimulator.online/DsDal2aZeSw7DnuKzXVI)
---


* [📄 **Download Professional Resume**](Roberto_Barajas_Resume.pdf)
* [📘 Download Full Technical Report: 10S3P Battery Management System] (https://drive.google.com/file/d/1Crthiedf52XxD71sAHAsho0QbnKb91As/view?usp=sharing)
* [📗 **Download Simulation Analysis: Transistor-Level Active Filter**](ECE_138_Filter_Simulation.pdf)
* [📙 **Download Lab Data & Telemetry: DC Shunt-Wound Generators**](DC_Generator_Lab_Data.pdf)
