# copperminds

Thoughts, notes and learnings from working with electronics and embedded systems.

---

## Posts

Resonance, Damping, and Filter Design in Automotive Electronics

LC filters without damping resistors exhibit a resonant peak at their natural frequency, which can cause overshoot in the time domain. Introducing a series resistor reduces the peak and stabilizes the response.

In my MATLAB simulations:
Frequency Domain (Bode Plot)
R = 0 Ω → High resonance, oscillatory step response
Moderate R → Reduced peak, faster settling
High R → Smooth response, reduced selectivity
For comparison, a simple RC filter shows no resonance and a gentle roll-off. The main difference is that RC filters provide a gradual attenuation with simpler implementation, while LC filters have a sharper cutoff and higher selectivity but can oscillate without damping.

Time Domain (Step Response) – Without damping, the LC circuit rings like a spring. With proper damping, oscillations vanish and the system stabilizes quickly.

This has direct relevance in automotive systems. Damping prevents ringing during transients and reduces EMI stress. In EV motor drives, it helps stabilize voltage and maintain torque quality. The concept is similar in suspension systems, where the damping ratio balances stability and responsiveness.

A design insight from TI is the use of second order Butterworth filter, It provides a flat passband to preserve signal amplitude, a steep roll-off to reject high-frequency noise, and minimal phase distortion to maintain control system stability.

Ref : https://lnkd.in/gsC2G-Ma
