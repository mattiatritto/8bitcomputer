# What is RAM

**RAM** (*Random Access Memory*) is a temporary memory where the CPU stores data. When the power is off, data in RAM are deleted.

## Implementation of a Static RAM

In our computer, we're going to build a **static RAM** (because Dinamic RAM needs a refreshing circuit).

We're using two 74LS189 chips in series (RAM chip with 4 bit address each one), two 74LS04N (because, for some reason, 74LS189 outputs are inverted) a tristate buffer, and a register that stores the address.


The entire circuit is designed to **manually address memory** or, in future developments, to **automatically taking data from the BUS**.

RAM chip schematics:

![alt text](https://github.com/mattiatritto/8bitcomputer/blob/master/4-RAM/images/RAM-chip.png)
