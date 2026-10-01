<h1 align="center">Custom PIC-Based Telemetry & Sensor Board</h1>

<p align="center">
  <b>Mixed-Signal Hardware Design & Motion Sensing Node</b><br>
  <i>Showcasing Schematic Capture, EMI-Aware PCB Layout, and Real-Time Kinetic Sensing</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Altium_Designer-A59B6A?style=for-the-badge&logo=altium&logoColor=white" alt="Altium"/>
  <img src="https://img.shields.io/badge/Microchip_PIC-ED1C24?style=for-the-badge&logo=microchip&logoColor=white" alt="PIC"/>
  <img src="https://img.shields.io/badge/Embedded_C-A8B9CC?style=for-the-badge&logo=c&logoColor=black" alt="Embedded C"/>
</p>

<div align="center">
  
  **[View the Complete Schematic (PDF)](./schematic/MotionBoard_Sch.pdf)** 

</div>

---

## 🎯 Project Overview

A standalone mixed-signal hardware node powered by an 8-bit **Microchip PIC Microcontroller**. This board captures real-time 3-axis spatial orientation data using an analog accelerometer and translates kinetic movement into dynamic visual feedback via an RGB driver stage. The project emphasizes industrial schematic capture best practices, power integrity, and EMI-aware routing.

## 🛠️ Hardware & Software Stack

* **Microcontroller:** Microchip PIC Series (8-bit)
* **Firmware:** Embedded C
* **Sensors:** 3-Axis Analog Accelerometer
* **EDA Tool:** Altium Designer (Schematic Capture, PCB Layout, BOM Management)

---

## ⚙️ System Architecture & Hardware Design

The hardware architecture is designed with a strict focus on isolating high-frequency noise from sensitive analog traces.

1. **Power Regulation:** Input voltage is stepped down and stabilized using a 5V LDO regulator, featuring an input reverse polarity protection circuit to safeguard the ICs.
2. **Signal Integrity:** 100nF decoupling capacitors are strategically placed immediately adjacent to the MCU VDD pins to filter high-frequency switching noise. Analog accelerometer traces are routed short and strictly isolated from high-speed oscillator clock lines.
3. **Actuation Stage:** Real-time spatial data dictates the output of a Common Anode RGB LED, driven by a dedicated BJT transistor stage to handle the current load safely without stressing the MCU's GPIO pins.

---

## 📂 Repository Structure

* **[`datasheets/`](./datasheets):** Contains Datasheets used in the Schematic.
* **[`layout/`](./layout):** Altium Designer PCB Layout files (`.PcbDoc`)
* **[`schematic/`](./schematic):** Altium Designer files including Schematics (`.SchDoc`) and high-resolution PDF schematics.

---
*Created by Abdullah Ajmal - February 2026*
