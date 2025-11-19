# DSBSC-using-python


## AIM:

To implement and analyze DSBSC using Python's NumPy and Matplotlib libraries. 

## EQUIPMENTS REQUIRED

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer


## Algorithm:


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate DSBSC Signal: Apply the DSBSC formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.


## Program

```
import numpy as np
import matplotlib.pyplot as plt
Am = 4.6;
fm = 384;
Ac = 9.2;
fc = 3840;
fs = 38400;
t=np.arange(0,2/fm,1/fs)
m = np.cos(2 * np.pi * fm * t)
c=np.cos(2*np.pi*fc*t)
s1 = (Ac + m) * np.cos(2 * np.pi * fc * t)
s2 = (Ac - m) * np.cos(2 * np.pi * fc * t)
s = s1 - s2
s = m * c
plt.subplot(3,1,1)
plt.plot(t, m)

plt.subplot(3,1,2)
plt.plot(t,c)

plt.subplot(3,1,3)
plt.plot(t,s)
```

## Output Graph

<img width="684" height="513" alt="image" src="https://github.com/user-attachments/assets/5845ced7-8393-4262-9a18-d4130bc381b9" />





## Tablular Column





## Result

Thus the DSB-SC-AM Modulation is generated using python.
