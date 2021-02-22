## Bistable 555 timer

As well as the one shot 555 Monostable configuration above, we can also produce a **Bistable device** with the operation and output of the 555 Bistable.

The 555 Bistable is one of the simplest circuits we can build using the 555 timer oscillator chip. The bistable configuration does not use any RC timing network to produce an output waveform so **no equations are required** to calculate the time period of the circuit. Consider the Bistable 555 Timer circuit below

Circuit Schematics: 
![alt text](https://github.com/mattiatritto/8bitcomputer/blob/master/1-ClockCircuit/3-BistableTimer/images/bistable-555.png)


The switching of the output waveform is achieved by controlling the trigger and reset inputs of the 555 timer which are held HIGH by the two pull-up resistors (R1 and R2). By taking the trigger input (PIN 2) LOW, switch in set position, changes the output state into the HIGH state and by taking the reset input (PIN 4) LOW, switch in reset position, changes the output into the LOW state.

The 555 timer circuit will remain in either state indefinitely and is therefore bistable. Then the Bistable 555 timer is stable in both states, HIGH and LOW. The threshold input (PIN 6) is connected to ground to ensure that it cannot reset the bistable circuit as it would in a normal timing application.



## Sitography

- [Electronics tutorial](https://www.electronics-tutorials.ws/waveforms/555_timer.html)
