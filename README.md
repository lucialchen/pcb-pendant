# 555timerCES PCB
## Description

This repository contains the design files and documentation required to reproduce a single-layer PCB that drives a blinking LED using a 555 timer in astable mode.

The board was designed in KiCad and fabricated using CNC isolation milling, then assembled with through-hole components powered by a CR2032 coin cell.

This README provides the minimum technical information required for a third party to replicate the board and achieve the same functionality.

---

## Required Equipment
- Carvey CNC
- PCB v bit
- 0.8 mm drill bit
- 1/8 inch double flute straight end mill bit
- Single-sided copper board
- Soldering iron + solder
- Precision tweezers
- Cutters

---

## Required Materials
- 1× 555 timer IC
- 3× Resistors (Default: 4.7k R1, 68k R2, 470R R3)
- 2× Ceramic capacitors (Default: 4.7u C1, 10n C2)
- 1× LED
- 1× CR2032 coin cell battery holder
- 1× CR2032 battery

The exact values of R1, R2, and C1 determine how fast the LED blinks.  
You can adjust them to get the timing you want.

Use this calculator to experiment with values:

https://www.allaboutcircuits.com/tools/555-timer-astable-circuit/


---

## Fabrication Instructions
Import the provided design files into Easel software for CNC compatibility.

### 1. Mill Traces

Use the provided front copper file: 555timerCES-F_Cu.gbr

Use the PCB v bit for isolation tracing.

Double click the traces in Easel to adjust cut depth parameters in Easel. Recommended to start with 0.08mm depth and gradually increase so as to fully isolate traces.

---

### 2. Drill Holes

Use provided drill file: 555timerCES-PTH.drl

Switch to a 0.8 mm drill bit.

Utilize the "add depth" feature in Easel to add 0.2mm. If the CNC does not drill all the way through the board, precision/pointed tweezers can be used to cut the holes through the rest of the board. 

---

### 3. Cut Board Outline

Use the provided edge cuts file: 555timerCES-Edge_Cuts.gbr

Switch drill bit to a 1/8 inch double flute straight end mill bit.

Again set: add depth = +0.2 mm

---

## Assembly

After cutting out the outline shape and sanding down the edges, solder the following components to the board using the solder iron according to their positioning on the traces:

1. R1, R2, R3
2. C1, C2
3. 555 timer (U1)
4. LED
5. Battery holder

---

## Operation

Insert a CR2032 battery to make the LED blink continuously.










