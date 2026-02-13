# Lab 7 Memory and Video in Logisim Evolution

This repository contains my Logisim Evolution designs and report for Lab 7, which focuses on building a small RAM based system and drawing pixels using an RGB Video module. :contentReference[oaicite:2]{index=2}

I complete the work individually and collaborate with a lab partner during the in lab demo by comparing designs and discussing tradeoffs, but the submitted artifacts here reflect my own implementation. {index=4}

## Contents

- `circuits/lab7_part1.circ` RAM write design for Part I
- `circuits/lab7_part2.circ` RGB Video square drawing design for Part II
- `report/lab7_report.tex` and `report/lab7_report.pdf` prelab report with schematics and simulation outputs
- `assets/` screenshots of simulations used in the report

## Requirements

- Logisim Evolution
- The provided starter files from the course for Lab 7

## How to run

1. Open Logisim Evolution
2. Open `circuits/lab7_part1.circ` or `circuits/lab7_part2.circ`
3. Use the built in simulation controls and clock to step through behavior
4. Use Poke to change inputs where applicable

## Part I RAM writing design

Goal
Build a small RAM based module and write increasing values across addresses, then wrap and continue. 

Notes
The Logisim RAM component exposes address, write enable, output enable, and clock, with data in and data out ports.

What to look for
- Address advances each cycle
- Data written increments and wraps as specified
- Output is connected to a seven segment display for visibility during simulation. 

## Part II RGB Video square drawing design

Goal
Draw a filled 16 by 16 square on a 128 by 128 RGB Video display at the input X Y position when Enable is turned on, and support drawing additional squares by toggling Enable between updates. :contentReference[oaicite:8]{index=8}

RGB Video interface summary
The RGB Video component uses Reset, Clock, Write Enable, X Coordinate, Y Coordinate, and a 24 bit 888 RGB Data In value.

Edge behavior
If the square would exceed the bottom or right edge, it wraps around to the top or left side. 
- Enable on for the full draw sequence
- Enable toggled off before changing X and Y
- Reset behavior while Enable is on

## Deliverables

The required deliverables include the report and the two circuit files listed below. 

- `report/lab7_report.tex`
- `report/lab7_report.pdf`
- `circuits/lab7_part1.circ`
- `circuits/lab7_part2.circ`

## Credits

Course materials and lab specification provided by the course staff.
