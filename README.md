# 5-Stage Pipelined RISC-V RV32I Processor
A 32-bit 5-stage pipelined RISC-V (RV32I) processor implemented in SystemVerilog, featuring Instruction Fetch, Decode, Execute, Memory, and Writeback stages with a modular RTL design. Includes a register file, ALU, pipeline registers, and load-use hazard detection with pipeline stalls

---

## 1. Project Overview

This project implements a simple 5-stage pipelined RISC-V processor in SystemVerilog.

The processor follows the classic pipeline structure used in many introductory CPU designs:

1. Instruction Fetch
2. Instruction Decode
3. Execute
4. Memory Access
5. Writeback

The goal of this project is to build an interview-relevant RTL design that demonstrates CPU datapath design, pipeline registers, instruction decoding, ALU control, forwarding, load-use hazard handling, branch flushing, and self-checking verification.

This is not intended to be a fully optimized commercial RISC-V core. It is a clean educational RTL implementation focused on understanding and demonstrating core computer architecture concepts.

---

## 2. Project Goals

The main goals of this project are:

- Implement a simple RV32I-based 5-stage pipelined processor.
- Split the design into realistic RTL modules.
- Use pipeline registers between stages.
- Support common arithmetic, logic, load, store, and branch instructions.
- Implement forwarding to resolve most data hazards.
- Implement load-use hazard detection with a one-cycle stall.
- Implement branch flushing for taken branches.
- Create a self-checking SystemVerilog testbench.
- Keep the design simple enough to understand, debug, and explain in interviews.

---

## 3. Processor Architecture

The processor uses a 32-bit datapath.

| Feature | Description |
|---|---|
| ISA | RISC-V RV32I subset |
| Data width | 32 bits |
| Instruction width | 32 bits |
| Register file | 32 registers, each 32 bits |
| Register x0 | Hardwired to zero |
| Pipeline stages | 5 |
| Instruction memory | Simple internal memory |
| Data memory | Simple internal memory |
| Branch resolution | Execute stage |
| Forwarding | EX/MEM and MEM/WB to EX |
| Load-use hazard handling | One-cycle stall |
| Branch prediction | Not implemented |

---

