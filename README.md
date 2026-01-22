# Microprocessor System Design (8086/8088 Architecture)

This project details the hardware design and schematic implementation of a modular microcomputer system based on the Intel x86 architecture. It includes detailed circuit diagrams for the central processing unit, memory interfacing, communication ports, and peripheral management.

## Project Documentation & Schematics

The project is divided into specific hardware modules, documented in the following files:

| File Name | Description |
| :--- | :--- |
| **Documentatie_proiect.pdf** | The comprehensive project report containing the theoretical design, design choices, block diagrams, and operational description of the system. |
| **SCH_PM_proiect_5-Unitatea centrala 2...** | Schematics for the **Central Processing Unit (CPU)** module, including the processor, clock generation, and bus control logic. |
| **SCH_PM_proiect_2-Conectarea memoriei...** | Schematics for the **Memory Subsystem**, detailing the addressing logic and connection of RAM and ROM/EPROM chips. |
| **SCH_PM_proiect_3-Interfata seriala...** | Schematics for **I/O Interfaces**, specifically designing the Serial (USART) and Parallel (PPI) communication ports. |
| **SCH_PM_proiect_4-Periferice...** | Schematics for additional **System Peripherals**, such as interrupt controllers, timers, or DMA controllers. |

## System Architecture

The hardware design is structured into four main subsystems:

### 1. Central Processing Unit (CPU) Module
* **Core:** Designed around an 8086/8088 microprocessor.
* **Bus Management:** Includes address latches (e.g., 8282/8283) to demultiplex the address/data bus and bus transceivers (e.g., 8286/8287) for data flow control.
* **System Control:** Utilizes a Bus Controller (e.g., 8288) to generate system command signals (IOR, IOW, MEMR, MEMW).

### 2. Memory Subsystem
* **Organization:** The memory map is split into Program Memory (ROM/EPROM) for firmware and Data Memory (SRAM/DRAM).
* **Decoding:** Includes logic gates or decoders (e.g., 74138) to select specific memory banks based on the address bus.

### 3. Communication Interfaces
* **Parallel Interface:** Implemented using a Programmable Peripheral Interface (PPI), typically the **Intel 8255**, to support general-purpose I/O.
* **Serial Interface:** Implemented using a Universal Synchronous/Asynchronous Receiver/Transmitter (USART), typically the **Intel 8251**, for RS-232 communication.

### 4. Peripherals & Interrupts
* **Interrupts:** Managed by a Programmable Interrupt Controller (PIC), to handle external hardware requests.
* **Timing:** Includes a Programmable Interval Timer (PIT), for generating baud rates and system ticks.

## Key Components

* **Processor:** Intel 8086 / 8088
* **Clock Generator:** Intel 8284
* **Bus Controller:** Intel 8288
* **Parallel I/O:** Intel 8255
* **Serial I/O:** Intel 8251
* **Interrupt Controller:** Intel 8259

