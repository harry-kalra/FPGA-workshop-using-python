# FPGA Workshop - Day 3

## Overview

Day 3 moves into **combinational arithmetic design** using the **PYNQ-Z2** board.  
The notebook for this day demonstrates a **Half Adder**, where two switch inputs are read and the FPGA shows:

* **Sum** on one LED
* **Carry** on another LED

This is a nice step up from basic logic gates because it shows how simple Boolean operations can be combined to build useful digital circuits.

---

## Code Explanation

### 1. Setup & Initialization

* `BaseOverlay('base.bit')` loads the base FPGA design
* LEDs and switches become accessible through the PYNQ framework
* A short LED blink sequence is used at the start to confirm the board is active

---

### 2. Reading Inputs

* Two slide switches are used as inputs:

  * `switch1 = base.switches[1].read()`
  * `switch2 = base.switches[0].read()`

* Each switch gives a binary value:

  * `0` -> OFF
  * `1` -> ON

---

### 3. Half Adder Logic

The Half Adder produces two outputs:

* **Sum** using XOR:

  * `sum = switch1 ^ switch2`

* **Carry** using AND:

  * `carry = switch1 and switch2`

This means:

* Sum becomes `1` when the inputs are different
* Carry becomes `1` only when both inputs are `1`

---

### 4. LED Output Mapping

* **LED 0** displays the **Sum**
* **LED 1** displays the **Carry**

If the result is `1`, the corresponding LED turns ON.  
If the result is `0`, the LED turns OFF.

The console also prints:

* `"sum = 1"` when Sum is active
* `"carry = 1"` when Carry is active

---

### 5. Continuous Execution

* The program runs inside `while True:`
* This keeps the FPGA reading switches continuously in real time
* Any change in the switch position is immediately reflected on the LEDs

---

## Half Adder Truth Table

| Input A | Input B | Sum | Carry |
|--------|--------|-----|-------|
| 0 | 0 | 0 | 0 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 1 |

---

## Notes

* The current notebook for Day 3 shows the **Half Adder** implementation
* The program runs continuously using an infinite loop
* Stop execution manually using `Ctrl + C`

---
