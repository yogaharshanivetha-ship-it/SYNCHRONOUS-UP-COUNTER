### NAME : HARSHA NIVETHA .A.K
### REG NO :25016557
# EXPERIMENT 7:  IMPLEMENTATION OF SYNCHRONOUS UP COUNTER

# #AIM:

To implement 4 bit synchronous up counter and validate functionality.

# SOFTWARE REQUIRED:

Quartus prime

# 4 BIT SYNCHRONOUS UP COUNTER

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

# PROCEDURE :
 1.Initialize the shift register to a known state (e.g., all zeros).
 
 2.Input a bit serially into the shift register.
 
 3.Shift the contents of the register one position to the right (or left).
 
 4.Output the shifted bit from the last stage of the register.
 
 5.Repeat steps 2-4 for each bit you want to input and shift.
 


# PROGRAM :
![EXP UP PROGRAM](https://github.com/user-attachments/assets/9cfd4a57-816c-40a7-a1ff-ee00c6d940ea)


# RTL LOGIC UP COUNTER :
![UP LOGIC DE](https://github.com/user-attachments/assets/1a17d74b-1ce6-471d-b962-e950d5c8ff4e)


# TIMING DIAGRAM FOR IP COUNTER :
![UP WAVE FORM](https://github.com/user-attachments/assets/d17a043b-aabe-44fc-8a65-a08cba89f986)

# TRUTH TABLE
![TRUTHTABLE UP](https://github.com/user-attachments/assets/db284906-f159-43a8-8dc0-c85b1a234658)

# RESULT :
 Hence a 4 bit synchronous up counter is implemented successfully.
