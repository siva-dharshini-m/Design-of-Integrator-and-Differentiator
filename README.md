# Design-of-Integrator-and-Differentiator
### AIM:
To design and test the performance of integrator and differentiator circuits using Op-amp.
### APPARATUS REQUIRED:

| S.No | Name of the Apparatus        | Range/Specification     | Quantity     |
|------|------------------------------|---------------------------|--------------|
| 1    | Signal Generator             | 3 MHz                     | 1            |
| 2    | DSO                          | 30 MHz                    | 1            |
| 3    | Dual RPS                     | (0 – 30) V                | 1            |
| 4    | Op-Amp                       | µA741                     | 1            |
| 5    | Bread Board                  | —                         | 1            |
| 6    | Resistors                    | 1K, 10K, 100K             | 2            |
| 7    | Capacitors                   | 0.1 µF, 0.01 µF           | 1            |
| 8    | Connecting wires and probes  | As required               | As required  |

### THEORY:
### INTEGRATOR
A circuit in which the output voltage waveform is the integral of the input voltage waveform is the integrator. Such a circuit is obtained by using a basic inverting amplifier configuration if the feedback resistor Rf is replaced by a capacitor Cf . The expression for the output voltage is given as,
Vo = - (1/Rf C1 ) ∫ Vi dt
Here the negative sign indicates that the output voltage is 180 0 out of phase with the input signal. Normally between fa and fb the circuit acts as an integrator. Generally, the value of fa < fb . The input signal will be integrated properly if the Time period T of the signal is larger than or equal to Rf Cf . That is,
T ≥ Rf Cf
The integrator is most commonly used in analog computers and ADC and signal-wave shaping circuits.
### DIFFEERENTIATOR:
The differentiator circuit performs the mathematical operation of differentiation; that is, the output waveform is the derivative of the input waveform. The differentiator may be constructed from a basic inverting amplifier if an input resistor R1 is replaced by a capacitor C1 . The expression for the output voltage is given as,
Vo = - Rf C1 ( dVi /dt )
Here the negative sign indicates that the output voltage is 180 0 out of phase with the input signal. A resistor Rcomp = Rf is normally connected to the non-inverting input terminal of the op-amp to compensate for the input bias current. A workable differentiator can be designed by implementing the following steps:
1.	Select fa equal to the highest frequency of the input signal to be differentiated. Then, assuming a value of C1 < 1 µF, calculate the value of Rf.
2.	Choose fb = 20 fa and calculate the values of R1 and Cf so that R1C1 = Rf Cf.
The differentiator is most commonly used in wave shaping circuits to detect high frequency components in an input signal and also as a rate–of–change detector in FM modulators.
### DESIGN:
### INTEGRATOR
To obtain the output of an Integrator circuit with component values R1Cf = 0.1ms , Rf = 10 R1 and Cf = 0.01 µF and also if 1 V peak square wave at 1000Hz is applied as input.
We know the frequency at which the gain is 0 dB, fb = 1 / (2π R1 Cf) Therefore fb = 	 Since fb = 10 fa , and also the gain limiting frequency fa = 1 / (2π Rf Cf)
We get , R1 =	and hence Rf = 	.
### DIFFERENTIATOR
Design an op-amp differentiator that will differentiate an input signal with fmax = 100HZ Select fa = fmax = 100 HZ = 1 / 2πRFC1
Let C1 = 0.1μF
Then RF = 1 / 2π(102)(10-7)
= 15.9KΩ
Now choose fb = 10fa = 1 / 2πR1C1 Therefore, R1 = 1 / 2π(103)(10-7)
= 1.59KΩ Since RFCF = R1C1
We get, CF = (1.59*103*10-7) / 15.9*103
= 0.01μF


### INTEGRATOR CIRCUIT DIAGRAM

<img width="940" height="478" alt="image" src="https://github.com/user-attachments/assets/9b266103-e1da-4f93-b7a5-916e523fd14b" />

### TABULATION:

| Wave Type   | Input Amplitude (V) | Input Time Period (ms) | Input Frequency (Hz) | Output Amplitude (V) | Output Time Period (ms) | Output Frequency (Hz) |
|-------------|---------------------|-------------------------|----------------------|----------------------|--------------------------|-----------------------|
| Sine Wave   |    500m             |      64                 |       1.5k           |         3.36         |    64                    |         1.55k         |
| Square Wave |      280            |       64                |         1.5k         |        2.80          |    64                    |         1.55k         |


### MODEL GRAPH

<img width="644" height="330" alt="image" src="https://github.com/user-attachments/assets/bff30b0a-c276-4bd8-8798-230a3bebd0b4" />

<img width="940" height="558" alt="image" src="https://github.com/user-attachments/assets/c061b815-c3f3-4d69-874d-a539c1bdf779" />

OUTPUT:

<img width="600" height="770" alt="image" src="https://github.com/user-attachments/assets/a76e8aeb-f194-4675-8dbe-198e89a38e96" />


### DIFFERENTIATOR CIRCUIT DIAGRAM

<img width="673" height="356" alt="image" src="https://github.com/user-attachments/assets/677abdb4-c856-4d60-a6cf-d48b23a6e4a3" />

### TABULATION:

| Wave Type   | Input Amplitude (V) | Input Time Period (ms) | Input Frequency (Hz) | Output Amplitude (V) | Output Time Period (ms) | Output Frequency (Hz) |
|-------------|---------------------|-------------------------|----------------------|----------------------|--------------------------|-----------------------|
| Sine Wave   |   784m              |             50          |      2k              |          1.04        |          50              |        2k               |
| Square Wave     848m              |            50           |      2k              |           1.68       |           50             |        2k              

### MODEL GRAPH
<img width="940" height="1080" alt="image" src="https://github.com/user-attachments/assets/079984a9-bc54-4b2a-b4ee-e15aaf81e312" />


GRAPH:

<img width="586" height="751" alt="image" src="https://github.com/user-attachments/assets/a832bc53-33a2-471f-b662-d1e316434563" />


### PROCEDURE
1.	Connections are given as per the circuit diagram
2. + Vcc and - Vcc supply is given to the power supply terminal of the Op-Amp IC.
3.	By adjusting the amplitude and frequency knobs of the function generator, appropriate input voltage is applied to the inverting input terminal of the Op- Amp.
4.	The output voltage is obtained in the CRO and the input and output voltage waveforms are plotted in a graph sheet.

### RESULT:
Thus an Integrator and Differentiator using op-amp are designed and their performance was successfully tested using op-amp IC 741.
