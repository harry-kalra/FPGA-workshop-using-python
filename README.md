# 🚀 FPGA Workshop Project | PYNQ-Z2

<p align="center">
  <b>Hands-on FPGA Development using Python & Digital Logic Design</b><br>
  Built on the PYNQ-Z2 (Zynq-7000 SoC)
</p>

---

## 📌 Project Overview

This repository showcases practical FPGA experiments performed using the **PYNQ-Z2 development board**.
The project focuses on building a strong foundation in **digital logic design** through real-time hardware interaction.

Unlike purely theoretical learning, this project demonstrates how inputs from physical switches are processed and visualized using LEDs on an FPGA board.

---

## 🎯 Key Highlights

* ⚡ Real-time hardware interaction using FPGA
* 🧠 Strong foundation in digital logic design
* 🐍 Python-based control using PYNQ framework
* 🔌 Hands-on experience with embedded systems
* 🛠️ Beginner-friendly yet conceptually strong implementation

---

## 🧩 Concepts Implemented

### 🔹 Digital Logic Design

* AND, OR, NOT, NAND, NOR, XOR gates
* Truth table-based implementation

### 🔹 Code Conversion

* Binary → Gray Code
* Gray → Binary

### 🔹 Arithmetic Circuits

* Half Adder
* Half Subtractor

### 🔹 Data Routing

* 2:1 Multiplexer (MUX)

---

## 🛠️ Tech Stack

| Category     | Technology Used      |
| ------------ | -------------------- |
| Hardware     | PYNQ-Z2 FPGA Board   |
| Architecture | Xilinx Zynq-7000 SoC |
| Programming  | Python (PYNQ)        |
| Interface    | Jupyter Notebook     |

---

## ⚙️ System Workflow

```text
Switch Inputs → Logic Processing → LED Outputs
```

```python
while True:
    read_inputs()
    apply_logic()
    update_leds()
```

---

## 📁 Project Structure

```bash
FPGA-Workshop/
│
├── Day 1/   # Basic Logic Gates
├── Day 2/   # Code Conversion
├── Day 3/   # Adders & Multiplexer
├── Day 4/   # Practice / Extended Work
└── README.md
```

---

## ▶️ Getting Started

### 1️⃣ Setup

* Connect PYNQ-Z2 board to your system
* Power using USB

### 2️⃣ Run

* Open Jupyter Notebook (PYNQ environment)
* Upload or open project files
* Execute cells

### 3️⃣ Test

* Use switches as input
* Observe LED outputs

---

## 📸 Demo
![frontside of pynq](https://github.com/user-attachments/assets/0acf8364-8553-484d-a77f-71ae326f6944)
![backside of pynq](https://github.com/user-attachments/assets/7753080f-aecc-45d3-8950-72f287107f07)
---

## ⚠️ Important Notes

* Programs run continuously using `while True`
* Use **Ctrl + C** to stop execution
* Ensure stable power supply to the board

---

## 📚 Learning Outcomes

* Practical understanding of FPGA-based systems
* Implementation of combinational circuits
* Exposure to hardware-software co-design
* Confidence in working with embedded platforms

---

## 🔮 Future Improvements

* Full Adder & Full Subtractor
* Sequential circuits (Flip-Flops, Counters)
* Verilog/VHDL implementations
* Hardware acceleration projects
* Integration with sensors or IoT

---

## 🤝 Contributing

Contributions are welcome!
Feel free to fork this repository and improve implementations or add new experiments.

---

## ⭐ Show Your Support

If you found this project helpful:

* ⭐ Star this repository
* 🍴 Fork it
* 📢 Share with others

---

<p align="center">
  💡 <i>Learning by building is the best way to master hardware design.</i>
</p>
