### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**
```
1.Initialize the shift register to a known state (e.g., all zeros).

2.Input a bit serially into the shift register.

3.Shift the contents of the register one position to the right (or left).

4.Output the shifted bit from the last stage of the register.

5.Repeat steps 2-4 for each bit you want to input and shift.
```
**UP COUNTER PROGRAM**

<img width="417" height="275" alt="image" src="https://github.com/user-attachments/assets/1a8be187-a16c-49b2-921b-1e59cddcd568" />



Developed by: Teajesh R
RegisterNumber: 25009069



**RTL LOGIC UP COUNTER**

<img width="753" height="256" alt="image" src="https://github.com/user-attachments/assets/385aa2a0-cbc4-425b-883e-2a1d7de3acd4" />




**TIMING DIAGRAM FOR UP COUNTER**

<img width="1918" height="357" alt="image" src="https://github.com/user-attachments/assets/bd9089eb-5ad1-4ead-b313-b36284a7a50e" />



**TRUTH TABLE**

<img width="618" height="811" alt="image" src="https://github.com/user-attachments/assets/5f806c65-775f-4152-9d5f-e1a69bb682ca" />


**DOWN COUNTER PROGRAM**

<img width="508" height="264" alt="image" src="https://github.com/user-attachments/assets/8d016493-f88d-4810-b4c6-f31089d41dec" />


<img width="487" height="254" alt="image" src="https://github.com/user-attachments/assets/068a3043-4f6d-43e0-88e5-f54a2c5b1f04" />

Developed by: Teajesh R
RegisterNumber: 25009069
*/



**RTL LOGIC DOWN COUNTER**

<img width="631" height="257" alt="image" src="https://github.com/user-attachments/assets/f862a1ee-2ad0-4e26-969a-371670f048f3" />



**TIMING DIAGRAM FOR DOWN COUNTER**

<img width="1919" height="604" alt="image" src="https://github.com/user-attachments/assets/cf149a44-499c-4f07-ac00-efbc5caa5370" />



**TRUTH TABLE**

<img width="707" height="710" alt="image" src="https://github.com/user-attachments/assets/e89fa104-0442-4d70-acf0-fdf28fad2d2f" />



**RESULTS**

Hence a 4 bit synchronous down counter is implemented correctly
