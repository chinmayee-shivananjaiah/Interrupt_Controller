Register-Based Interrupt Controller

A Verilog-based register-controlled interrupt controller designed to manage multiple interrupt sources and generate a single interrupt output based on enable and priority conditions.

Project Overview

The interrupt controller supports multiple interrupt sources such as:

- Timer
- GPIO
- UART
- SPI

The design provides interrupt status monitoring, interrupt enable/masking, interrupt clearing, and priority-based interrupt handling.

Features

- Multiple interrupt sources
- Interrupt Enable Register (IER)
- Interrupt Status Register (ISR)
- Interrupt Acknowledge/Clear Register (IACR)
- Interrupt masking
- Interrupt clearing
- Priority-based interrupt handling
- Single "IRQ_OUT" generation
- Verilog testbench for functional verification
- Web-based output visualization

Working

When an interrupt source becomes active, the controller checks whether that interrupt is enabled.

The enabled interrupts are evaluated according to their priority. The highest-priority active interrupt is selected, and the controller generates a single "IRQ_OUT" signal.

Interrupts can be masked using the interrupt enable mechanism and cleared through the interrupt clear mechanism.

Interrupt Sources

Interrupt| Source
Timer| Timer event
GPIO| GPIO event
UART| UART event
SPI| SPI event

Files

Interrupt_Controller/
│
├── interrupt_controller.v
├── interrupt_controller_tb.v
├── README.md
│
└── Output/
    └── Web Dashboard Output

Verification

The design is verified using a Verilog testbench that applies different interrupt conditions and checks the resulting interrupt status and "IRQ_OUT" behavior.

Simulation can be performed using Xilinx Vivado.

Output

The project output is represented using a web-based visualization showing interrupt status, "IRQ_OUT", priority handling, and interrupt activity.

Tools Used

- Verilog HDL
- Xilinx Vivado
- Verilog Testbench
- Web-based output visualization

Author

Chinmayee S
