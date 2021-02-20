## Clock logic

We want to combine the three signals here into one output clock signal.

There is a slide-switch (bistable 555 configuration) to select between automatic clock pulse (astable 555 timer configuration) and manual clock pulse (bistable 555 timer configuration).

Here's the circuit that will do for us the trick:

## Components

I used three basic chips: 74LS04 (inverter), 74LS08 (AND), 74LS32 (OR).


## Future developements

We could use only NAND gates to reduce power consumption and optimize the circuit.