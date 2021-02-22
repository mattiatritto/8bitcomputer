# Manual clock

Sometimes we want to **control the clock manually**. We want to just push a button on each time we want the clock to advance one clock tick (for debigging purposes).

We could use a simple push button to control the clock manually. The problem is that sometimes **buttons bounce** and they produce an unpleasent effect: in our case the clock advances two or even three clock ticks!

So we build a **debounce circuit** to avoid that buttons contacts bounce.

## Monostable 555 timer


Circuit Schematics: 
![alt text](https://github.com/mattiatritto/8bitcomputer/blob/master/1-ClockCircuit/2-MonostableTimer/images/monostable555.png)

When a negative (0 Volts) pulse is applied to the trigger input (PIN 2) of the monostable configured 555 Timer oscillator, the internal comparator detects this input and sets the state of the flip-flop changing the output from a LOW state to a HIGH state. This action in turn turns OFF the discharge transistor connected to PIN 7, thereby removing the short circuit across the external timing capacitor C1.


This action allows the timing capacitor to start to charge up through resistor R1 until the voltage across the capacitor reaches the threeshold (PIN 6) voltage of 2/3 Vcc set up by the internal voltage divider network. At this point the comparators output goes HIGH and RESETS the flip-flop back to its original state which in turn turns ON the transistor and discharges the capacitor to ground through PIN 7. This causes the output to change its state back to the original stable LOW value awaiting another trigger pulse to start the timing process over again. So the **Monostate Multivibrator has only ONE stable state**.


The Monostable 555 Timer circuit **triggers on a negative-going pulse applied to PIN 2** and this trigger pulse must be much shorter than the output pulse width allowing time for the timing capacitor to charge and then discharge instantly. Once triggered, the 555 Monostable will remain in this **HIGH unstable output state until the time period set up by the R1 x C1 network has elapsed**. The ammount of time that the output voltage remains HIGH is given by the following time constant equation:

            ***tau = 1.1 x R1 x C1***


## Sitography

[Electronics tutorial](https://www.electronics-tutorials.ws/waveforms/555_timer.html)
