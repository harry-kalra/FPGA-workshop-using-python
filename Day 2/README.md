# 📘 FPGA Workshop – Day 2

## 🧠 Overview

Day 2 focuses on implementing multiple **logic operations and code conversions** using switch inputs and displaying results on LEDs through the PYNQ framework.

---

## 📂 Code Explanation

### 🔹 1. Setup & Initialization

* `BaseOverlay('base.bit')` loads the FPGA design and enables access to LEDs and switches
* Initial LED blink sequence verifies that the board is working properly

---

### 🔹 2. Logic Gates Implementation

* Reads two switch inputs:

  * `switch1`, `switch2` → values are `0` or `1`

* Performs multiple logic operations:

  * AND → `switch1 & switch2`
  * OR → `switch1 or switch2`
  * NOR → `not(switch1 or switch2)`
  * NAND → `not(switch1 & switch2)`

* Each result controls a specific LED:

  * LED 0 → AND
  * LED 1 → OR
  * LED 2 → NOR
  * LED 3 → NAND

* LEDs turn ON/OFF based on the result, and outputs are printed to the console

---

### 🔹 3. Binary to Gray Code Conversion

* Takes 2-bit binary input from switches

* Converts to Gray code using:

  * `gray1 = switch1`
  * `gray0 = switch1 ^ switch2` (XOR)

* Outputs:

  * LED 0 → MSB
  * LED 1 → LSB

* Prints Gray code values for understanding

---

### 🔹 4. Binary to Excess-3 Conversion

* Reads 2-bit binary input (`A`, `B`)

* Applies Excess-3 logic:

  * `E0 = not B`
  * `E1 = not(A ^ B)` (XNOR)
  * `E2 = A | B`
  * `E3 = 0`

* Outputs mapped to LEDs:

  * LED 0 → E0
  * LED 1 → E1
  * LED 2 → E2
  * LED 3 → E3

* Displays both input and converted output in the console

---

## ⚠️ Notes

* All programs run in an infinite loop (`while True`)
* Stop execution manually using `Ctrl + C`XOR

---