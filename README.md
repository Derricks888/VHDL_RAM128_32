<p align="center">
  <img src="https://github.com/Derricks888/VHDL_RAM128_32/blob/main/docs/header.png?raw=true" width="850" alt="VHDL RAM128×32 Simulation Project Banner">
</p>

---

# 🧠 128×32 Single-Port RAM in VHDL

[![Simulation Status](https://img.shields.io/badge/Simulation-Passed-brightgreen)]()
[![Tool](https://img.shields.io/badge/ModelSim-Intel_10.5b-blue)]()
[![Language](https://img.shields.io/badge/VHDL-2008-orange)]()
[![License](https://img.shields.io/badge/License-MIT-lightgrey)]()

---

## 📘 Overview

This project implements a **128-word × 32-bit single-port RAM** in **VHDL**.  
It supports **synchronous write** and **asynchronous read** operations, following a typical FPGA-style behavioral model.

The design was verified with a custom testbench using **ModelSim–Intel FPGA Edition 10.5b**.

---

## 🌟 Entity Declaration

```vhdl
ENTITY RAM128_32 IS
  PORT (
    address : IN  STD_LOGIC_VECTOR (6 DOWNTO 0);
    clock   : IN  STD_LOGIC := '1';
    data    : IN  STD_LOGIC_VECTOR (31 DOWNTO 0);
    wren    : IN  STD_LOGIC;
    q       : OUT STD_LOGIC_VECTOR (31 DOWNTO 0)
  );
END RAM128_32;
