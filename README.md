# Phase-modulation

# AIM
To implement and analyze phase modulation (PM) using Python's NumPy and Matplotlib libraries.

# APPARATUS REQUIRED 

Software: Scilab
Hardware: Personal Computer

# THEORY

Phase Modulation (PM) is a technique where the phase of the carrier wave is varied in proportion to the instantaneous amplitude of the input signal (message signal). Unlike frequency modulation, where the frequency is varied, in phase modulation, the phase angle of the carrier wave changes with the amplitude of the message signal.

The general form of a PM signal can be represented as:

<img width="816" height="464" alt="image" src="https://github.com/user-attachments/assets/e6b6c5fe-abf4-4048-a8f3-49da2a4b598f" />

# ALGORITHM 

1. Initialize Parameters:
   Set the values of carrier amplitude, carrier frequency, message frequency, sampling frequency and phase deviation sensitivity.

2. Generate Time Axis:
   Create a time vector for the required signal duration using the sampling frequency.

3. Generate Message Signal:
   Generate the message signal as a cosine wave.

4. Generate Carrier Signal:
   Generate the carrier signal using the carrier amplitude and carrier frequency.

5. Generate PM Signal:
   Apply the phase modulation equation using the message and carrier signals to obtain the phase-modulated signal.

6. Plot the Signals:
   Plot the message signal, carrier signal and phase-modulated signal using Scilab plotting commands.

7. Display the Result:
   Observe the phase variation of the carrier signal according to the message signal.

# PROGRAM

Am=1.85;
fm=403;
Ac=3.237;
fc=4030;
fs=403000;
B=2.68;
Kp=B;
t=0:1/fs:2/fm;
em=Am*cos(2*3.14*fm*t);
subplot(4,1,1);
plot(t,em);
ec=Ac*cos(2*3.14*fc*t);
subplot(4,1,2);
plot(t,ec);
eFM=Ac.*cos((2*3.14*fc*t)+(B*sin(2*3.14*fm*t)));
subplot(4,1,3);
plot(t,eFM);
ePM=Ac.*cos((2*3.14*fc*t)+(Kp*cos(2*3.14*fm*t)));
subplot(4,1,4);
plot(t,ePM);

# OUTPUT WAVEFORM
<img width="1600" height="853" alt="WhatsApp Image 2026-09-24 at 11 20 05 AM" src="https://github.com/user-attachments/assets/3de09ab4-5530-4a9c-ac8b-91bb5f5c9ed0" />



# TABULATION
<img width="1030" height="1600" alt="WhatsApp Image 2026-09-07 at 1 44 37 PM" src="https://github.com/user-attachments/assets/2279e52f-2327-409e-9ee4-bbb067fd467c" />

# RESULT

The message signal, carrier signal, and phase-modulated (PM) signal will be displayed in separate plots. The modulated signal will show phase variations corresponding to the amplitude of the message signal.


