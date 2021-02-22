# Register Design

## What is a register

A **processor register** is a quickly accessible location available to a computer's processor. Registers usually consist of a small amount of **fast storage**, although some registers have specific hardware functions, and may be read-only or write-only.

In our 8-bit computer, each register contains **8 bit**. For educational purposes, we are going to build 2 registers for general purposes (*register "A" and "B"*) and the IR (*Instruction Register*).

## Register Design

Each single register is composed by two *SN74LS173A* **4-Bit D-Type Registers** with 3-State Outputs and a *74LS245* **3-State buffer**.

We're going to use a 3-State Buffer just because we want to see what's inside the registers (so we're going to put *Output Control* always HIGH and we don't want to always output something into the bus).

The "LOAD" option is related to the register, the "ENABLE" option is related to the octal bus transceiver.

4-Bit register schematics:

![alt text](https://github.com/mattiatritto/8bitcomputer/blob/master/2-Registers/images/4bit-register.png)

Octal Bus Transceiver schematics:

![alt text](https://github.com/mattiatritto/8bitcomputer/blob/master/2-Registers/images/octal-bus-transceiver.png)

## Sitography

[What is a register](https://en.wikipedia.org/wiki/Processor_register)
