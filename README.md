# Carry Look-Ahead Adder (CLA) in Verilog

## Overview

This project implements **4-bit** and **16-bit Carry Look-Ahead Adders (CLA)** using Verilog HDL.

Carry Look-Ahead Adders improve addition speed by generating carry signals in parallel instead of waiting for carries to ripple through each bit, making them significantly faster than Ripple Carry Adders.

---

## Features

- 4-bit Carry Look-Ahead Adder
- 16-bit Carry Look-Ahead Adder
- Hierarchical design
- Structural Verilog implementation
- Modular and reusable code

---

## Project Structure

```
.
├── cla4.v       // 4-bit Carry Look-Ahead Adder
├── cla16.v      // 16-bit Carry Look-Ahead Adder using four 4-bit CLAs
└── README.md
```

---

## 4-bit CLA

Inputs

- a[3:0]
- b[3:0]
- cin

Outputs

- sum[3:0]
- cout

The design computes:

- Propagate (P)
- Generate (G)
- Carry signals
- Sum outputs

using carry look-ahead equations.

---

## 16-bit CLA

The 16-bit adder is built using four instances of the 4-bit CLA.

```
        CLA0
Cin ─────►

        CLA1

        CLA2

        CLA3

                Cout
```

Each 4-bit block generates its carry output, which becomes the carry input of the next block.

---

## Advantages

- Faster than Ripple Carry Adder
- Modular design
- Easy to scale
- Suitable for digital VLSI design

---

## Applications

- Arithmetic Logic Units (ALU)
- Processors
- Digital Signal Processing
- FPGA Designs
- ASIC Designs

---

## Language

- Verilog HDL

---

## Author

Nikhil Mani Reji
