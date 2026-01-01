# CMOS NAND Gate Simulation using KiCad and ngspice

## Overview
This project demonstrates the design and transient simulation of a CMOS NAND gate using discrete NMOS and PMOS transistors in KiCad 9.  
The objective is to understand CMOS logic operation at the transistor level and verify the NAND truth table using time-domain (transient) simulation.

---

## Objective
- Design a CMOS NAND gate using PMOS pull-up and NMOS pull-down networks  
- Apply pulse inputs to generate all logic combinations  
- Verify NAND gate logic behavior using transient waveforms  

---

## Tools Used
- KiCad 9 (Schematic capture + ngspice simulation)  
- Generic NMOS and PMOS SPICE models  

---

## Circuit Description
- Two PMOS transistors connected in parallel to VDD (pull-up network)  
- Two NMOS transistors connected in series to GND (pull-down network)  
- Output taken from the common node between pull-up and pull-down networks  

---

## Simulation Setup

### Power Supply
- VDD = 5 V DC source  

### Input Sources
- Two independent PULSE voltage sources  
- Different pulse delays used to generate all four input combinations  
  (00, 01, 10, 11)

### Analysis
- Transient analysis performed using ngspice  
- Output and input waveforms observed to verify logic behavior  

---

## Results
- Output goes LOW only when both inputs are HIGH  
- Output remains HIGH for all other input combinations  
- NAND truth table behavior successfully verified  

| A | B | Output |
|---|---|--------|
| 0 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

---

## Issues Faced
- SPICE netlist errors due to rescued symbols and incorrect model paths  
- Incorrect pulse timing caused only extreme logic states to appear  

### Solutions
- Replaced rescued symbols with proper SPICE-compatible symbols  
- Added correct simulation directives  
- Phase-shifted pulse input sources  

---

## Limitations
- Ideal transistor models  
- No layout or parasitic extraction  
- No delay or noise margin analysis  
- Educational / learning-focused project  

---

## Learnings
- CMOS NAND gate operation at transistor level  
- Importance of pulse timing in transient simulations  
- KiCad + ngspice simulation workflow and common pitfalls  

---

## Author
Jay Bauti
