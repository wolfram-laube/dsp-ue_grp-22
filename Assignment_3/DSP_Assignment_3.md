Digital Signal Processing Tutorial

$(382.047 / 64 / 66 / 67 / 68 / 69 / 70), 20245$

Matthias Wagner, Bernhard Plaimer

Assignment 3

Sampling and Reconstruction

Information about assignments and in particular on Moodle submission modalities can be found in DSP-Tutorial_2024S_Courselnfo.pdf.

Submission deadline is Tue May 14 2024, 08:00.

# Exercise 1 Sampling $1(40 \%)$ 

The analogue signal

$$
x(t)=x_{1}(t)+x_{2}(t)=\sin \left(2 \pi f_{1} t\right)+\sin \left(2 \pi f_{2} t\right)
$$

with $f_{1}=4 \mathrm{kHz}$ and $f_{2}=6 \mathrm{kHz}$ is sampled with a sampling rate of $f_{s}=10 \mathrm{kHz}$ to yield the discrete time signal $x[n]$.

a) Draw the spectrum of $x(t)$.

b) Due to sampling frequency shifted versions of the analogue spectrum are generated.

Draw the spectra shifted by $-f_{s}, 0$ and $+f_{s}$ and then the spectrum for $x[n]$ as a result of spectral addition in one diagram. The diagram should show the spectra in the range from $-f_{s}$ to $+f_{s}$.

Hint: Draw real and imaginary parts of the spectrum rather than magnitude and phase to ease addition.

c) In Matlab plot the section 0 to $2 \mathrm{~ms}$ of the signal $x(t)$ with a sampling rate of $100 \mathrm{kHz}$ to emulate an analogue signal.

Then also add the sampled signal $x[n]=x\left(n T_{s}\right)$ to the same plot. Show that $x[n]$ corresponds to the spectrum derived in b).

Exercise 2 Sampling 2 (25\%)

The spectrum $X(f)$ of an analogue signal $x(t)$ is given with:
![](https://cdn.mathpix.com/cropped/2024_05_02_cce32ce20ed068e88e62g-1.jpg?height=388&width=580&top_left_y=2076&top_left_x=656)

a) Draw the real and imaginary parts of the spectrum $X(f)$.
b) $x(t)$ is sampled with $8 \mathrm{kHz}$ to yield the discrete time signal $x[n]$. Draw the spectrum of $x[n]$ from $-f_{s}$ to $f_{s}$ and indicate the baseband.

## Exercise 3 Reconstruction (35\%)

The discrete time signal $x[n]=\sqrt{2} \cdot \sin \left(2 \pi \cdot \frac{1}{8} \cdot n\right)$ is converted to the analogue signal $x(t)$ with an DAC which uses a clock frequency of $8 \mathrm{kHz}$ and which converts a numerical value of 1 to $1 \mathrm{~V}$.

a) Up to $20 \mathrm{kHz}$, list all positive frequencies which occur (in general) in $x(t)$.

b) The DAC implements a zero-order hold reconstruction.

1. What is the power (in $\mathrm{dB}$ ) of the baseband sinewave (the sine at the lowest frequency).
2. What is the power (in $\mathrm{dB}$ ) of the first out-of-band sinewave (the sine with the second lowest frequency).

c) Qualitatively draw the spectrum of $x(t)$ up to $20 \mathrm{kHz}$. Delta pulses should be drawn with an arrow, the height of the arrow should indicate the weight of the delta-pulse.

Hints:

- The power of a sinewave with amplitude $A$ is $P=\frac{A^{2}}{2}$ (also see Parseval's theorem for periodic signals DSP_02/27).
- The impulse response of a 0 -order reconstruction filter is a rectangular pulse, its frequency response is thus given in $D S P_{-} 02 / 43$.
- When calculating the attenuation for the respective frequencies it should be noted that e.g. Matlab uses the normalized sinc function.


## Exercise 4 Signal Processing Onramp - BONUS (15\%)

This task is optional (additional 15\%) and should help you to learn the basics of practical signal processing techniques in MATLAB. You will find out how to use spectral analysis and filtering for preprocessing, analyzing and extracting information from signal data.

For that you need to carry out the full 'Signal Processing Onramp course' [1]. For getting the bonus points you need to add the certificate to your protocol (you can download a pdf - see 'Share Certificate and Progress'). Also, you need to share your progress with my account (matthias.wagner@jku.at), what can be done in the same tab.

[1] https://matlabacademy.mathworks.com/details/signal-processing-onramp/signalprocessing

