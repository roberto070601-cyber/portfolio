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
| • High-Voltage Battery Assembly<br>• Capacitive Spot Welding<br>• Precision Soldering & Crimping<br>• Custom Cable Harnessing<br>• Ground Support Equipment (GSE) | • Hardware-in-the-Loop (HITL)<br>• Data Acquisition (DAQ) Setup<br>• Transistor-Level Circuit Analysis<br>• Calibration & Root Cause Analysis<br>• Industrial Safety Operations | • C / C++ (STM32, ESP32)<br>• Python (Test Automation)<br>• Linux Environment Config<br>• NI Multisim / Ultiboard<br>• LaTeX (Technical Reporting) |

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

### 3. Electromechanical Test Operations: DC Shunt-Wound Generators
*Characterization of a 300W industrial generator platform under 220V load testing, transient analysis, and magnetic field polarity manipulation.*
* **The Objective:** [We will fill this in next]
* **Test Infrastructure:** [We will fill this in next]
* **Failure/Limit Analysis:** [We will fill this in next]

---

## Professional Documentation
* [Link to Resume PDF]
* [Link to Downloadable Technical Reports]
