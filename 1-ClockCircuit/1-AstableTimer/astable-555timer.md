# Computer clock - 555 timer

For the 8 bit computer, we want to build a **clock circuit** that regulate all the other components of our machine.


## 555 Oscillator circuit

![Schematics](https://github.com/mattiatritto/8bitcomputer/blob/master/1-ClockCircuit/1-AstableTimer/images/555circuit-image.png)

In the **555 Oscillator circuit** above, pin 2 and pin 6 are connected together allowing the circuit to re-trigger itself on each and every cycle 
allowing it to operate as a free running oscillator. 

During each cycle capacitor, C charges up through both **timing resistors**, R1 and R2
but discharges itself only through resistor, R2 as the other side of R2 is connected to the discharge terminal, pin 7.

Then the capacitor charges up to 2/3 Vcc (the upper comparator limit) which is determined by the **0.693(R1+R2)C** combination 
and discharges itself down to 1/3 Vcc (the lower comparator limit) determined by the **0.693(R2 * C)** combination. 

This results in an output waveform whose voltage level is approximately equal to Vcc – 1.5V 
and whose output **ON** and **OFF** time periods are determined by the capacitor and resistors combinations.


## Some improvements to the oscillator circuit

1. To **reduce noise**, on pin 5 is recommended a 0.01 micro Farad capacitor.
2. To **smooth transitions** between LOW and HIGH, a 0.1 micro Farad capacitor between GND and Vcc is recommended.
3. To **prevent some accidental resets**, put Vcc voltage on pin 4.
4. To **regulate timing**, put a potentiometer (1MOhm) in series with a 1KOhm resistor (base resistor) instead of R2.
