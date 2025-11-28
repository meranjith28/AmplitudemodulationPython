# Amplitude modulation python

Aim

To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries. 


Apparatus Required:

Software: Python with NumPy and Matplotlib libraries

Hardware: Personal Computer

Theory

Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting information via a radio carrier wave. In AM, the amplitude of the carrier wave is varied in proportion to that of the message signal. The general form of an AM signal is:


Algorithm

1.	Initialize Parameters: Set the values for carrier frequency, message frequency, and sampling frequency.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Generate Carrier Signal: Define the carrier signal as a cosine wave.
5.	Modulate Signal: Apply the AM formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Code:
```
import numpy as np
import matplotlib.pyplot as plt

# Parameters
am = 4.6      # Message amplitude
fm = 366      # Message frequency
ac = 9.2      # Carrier amplitude
fc = 3660     # Carrier frequency
fs = 36600    # Sampling frequency
t = np.arange(0, 2/fm, 1/fs)  # Time vector

# Message signal
m = am * np.cos(2 * np.pi * fm * t)
plt.subplot(3,1,1)
plt.plot(t, m)
plt.title("Message Signal")

# Carrier signal
c = ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3,1,2)
plt.plot(t, c)
plt.title("Carrier Signal")

# AM signal: s(t) = [1 + m(t)/Ac] * carrier
am_signal = (1 + m / ac) * c
plt.subplot(3,1,3)
plt.plot(t, am_signal)
plt.title("AM")

plt.tight_layout()
plt.show()
```

Output Graph:

<img width="630" height="470" alt="image" src="https://github.com/user-attachments/assets/0def0014-4631-4c93-a7e8-a9a6fd84e17e" />

Tabulation:

![20251128_200044](https://github.com/user-attachments/assets/569d3399-ea79-4b9f-8fcc-a23e2dfcf058)


Result

The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. Thus AM is implemented using numPy and Matplotlib.
 
