# 📘 FPGA Workshop – Day 1

## 🧠 Overview

Day 1 introduces basic interaction with FPGA hardware using Python (PYNQ). The program reads switch inputs and controls LEDs by implementing a simple **AND gate**.

---

## 📂 Code Explanation

### 🔹 1. Setup & Initialization

* `BaseOverlay('base.bit')` loads the FPGA design and enables access to LEDs and switches
* Initial LED blink sequence checks if the board is working correctly

---

### 🔹 2. Continuous Execution

* `while True:` keeps the program running continuously
* Ensures real-time interaction between switches and LEDs

---

### 🔹 3. Reading Inputs

* `base.switches[0].read()` and `[1].read()` read switch states
* Each switch returns:

  * `0` → OFF
  * `1` → ON

---

### 🔹 4. AND Logic Implementation

* `switch1 & switch2` performs AND operation
* Output is `1` only when both switches are ON

---

### 🔹 5. LED Control

* If result is `1`:

  * LED 0 turns ON
  * Console prints `"output and = true"`

* Otherwise:

  * LED 0 turns OFF
  * Console prints `"output and = false"`

---

## ⚠️ Notes

* Program runs in an infinite loop (`while True`)
* Stop execution using `Ctrl + C`
---