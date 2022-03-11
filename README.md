# Aalto Micro and nano robotics

````diff
- Deadline for pre-assignments 11. March 2022
````

## Exercise 1
1. Answer the following questions:
    - What is the working principle of piezoelectric stick-slip actuator? 
        - Stick: piezoelectric-actuator is extended slowly (static friction).
        - Slip: the actuator returns suddenly to its initial position making the system slide (dynamic friction).
    - What is Step mode?
        - Step: Sawtooth signal, resolution equal to one step.
    - What is Scan mode?
        - Scan: Extend the piezoelectric-actuator in Stick-mode only. Resolution lower than a step.
    - How does the control signal look like and why? What are the key parameters?
        - Control signal is sawtooth signal, because improves the performance including step size, speed, positioning accuracy, and repeatability. Two types - conventional sawtooth waveform (CSW) and modified sawtooth waveform (MSW).
Slow ramp followed by a rapid retraction.
    - What is back-step movement during the control signal’s peak-to-peak sudden change?
    - What is the purpose of the pre-load force?

2. Explain the advantages and disadvantages of this type of actuator
    - Regarding to: resolution, range, control, step size, linearity, force and speed.
        - Good resolution (~ 1 nm).
        - Good range (> 10 mm).
        - Good force (> 1 N).
        - Good speed (> 20 mm/s).

3. Familiarize yourself with the provided functions of the control system in the AB8_help_2022.html file. Explain the parameters of the following functions: 
    - Nanomanipulator.StepMove (cha, steps, stepSize, stepFreq)
        - cha:		(int) Channel (0 .. )
        - steps:	(int) Number of steps to move (-30 000 .. 30 000)
        - stepSize:	(int) Step size (0 .. 4 095), 0 = 0V and 4 095 = 100V
        - stepFreq:	(int) Step frequency in Hz (1 .. 18 500)
    - Nanomanipulator.ScanMoveRelative (cha, disp, speed)
        - cha:		(int) Channel (0 .. )
        - disp:		(int) Displacement (-4 095 .. 4 095)
        - speed:	(int) Scanning Speed (1 .. 4 095 000 000)

4. Read and understand Tasks 1 and 2 before coming to the Hands-on session.

## Exercise 2
1. Home assignment: Your group develops a control algorithm using a simulator (deadline for submission: 11.03.2022 – for all groups).

2. Pre-assignment questions: You can find the pre-assignment questions in the exercise document (Acoustic_Manipulation_2022.pdf). You are supposed to prepare for answering the questions individually before the lab. If the answers are not satisfactory, you do not get to operate the lab setup:
    - What are standing waves?
    - How can standing waves appear in a vibrating plate?
    - Where do particles tend to move to on a vibrating plate?
    - How can you control the movement direction of a particle on a vibrating plate?
    - What properties of the driving signal affect the movement speed of the particles?
    - What properties of the particles affect their movement speed?
    - When a plate is vibrated with a piezo stack actuator attached directly to it, what can limit the vibration and how?
    - How would you determine the resonance modes of a plate?