# BASICS-OF-ELECTRONICS
Explanation of Series RLC Band-Pass Filter Project  
Introduction  
The Series RLC Band-Pass Filter project aims to demonstrate how a series RLC circuit can 
selectively allow a narrow band of frequencies to pass while attenuating others. This filter 
exhibits a peak response at its resonant frequency, where the inductive and capacitive 
reactances cancel each other, leaving the circuit impedance dominated by the resistor. The 
project involves designing the circuit, simulating its behavior using LTspice, and analyzing 
the frequency response and transient characteristics.  
Circuit Design  
The circuit consists of the following components connected in series:  
• V1: AC voltage source with an amplitude of 1 V, configured as SINE(0 1 0) AC 1 for AC 
analysis.  
• L1: Inductor with a value of 10 mH.  
• C1: Capacitor with a value of 100 nF.  
• R1: Resistor with a value of 100 Ω. The components are connected in a series loop 
from the voltage source to ground, with the output voltage measured across R1 
(between the junction of C1 and R1 and ground).  
Simulation Setup  
The simulation was conducted using LTspice with the following directives:  
• AC Analysis: .ac dec 100 10 10k – A logarithmic frequency sweep from 10 Hz to 10 
kHz with 100 points per decade to observe the band-pass response.  
• Transient Analysis (Optional): .tran 0 10m 0 1u – A 10 ms transient simulation with a 
1 µs timestep, using V1 set to SINE(0 1 1591.55) to test the response at the resonant 
frequency.  
The output voltage (across R1) was plotted to analyze the filter’s behavior.  
Results and Observations  
1. AC Analysis:   
o The magnitude plot of the output voltage (Vout) shows a peak at 
approximately 1.59 kHz, confirming the resonant frequency.  
o At this frequency, the output voltage reaches close to 1 V, indicating 
maximum signal transmission.  
o Frequencies below and above the resonant frequency are attenuated, 
demonstrating the band-pass characteristic.  
o The phase plot transitions from +90° at low frequencies 
(capacitordominated) to -90° at high frequencies (inductor-dominated), 
crossing 0° at the resonant frequency.  
2. Transient Analysis (Optional):   
o When V1 is set to SINE(0 1 1591.55) and the transient simulation is run, the 
output waveform across R1 shows a sine wave with an amplitude of 
approximately 1 V, verifying the circuit’s response at resonance. o  
At 
frequencies far from 1.59 kHz (e.g., 500 Hz or 5 kHz), the output amplitude is 
significantly reduced, consistent with the band-pass filter behavior.  
Conclusion  
The simulation successfully demonstrates the band-pass behavior of the series RLC circuit, 
with a clear peak at the resonant frequency of approximately 1.59 kHz. The AC analysis 
confirms the filter’s ability to pass signals near this frequency while attenuating others, 
aligning with the project’s objectives. The transient analysis further validates the circuit’s 
response at the resonant frequency. This project provides a practical understanding of how 
RLC circuits can be used to filter specific frequency bands. 
