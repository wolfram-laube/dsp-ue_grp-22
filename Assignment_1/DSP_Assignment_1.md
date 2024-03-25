# Digital Signal Processing Tutorial (382.047/64/66/67/68/69/70), 2024S <br> Matthias Wagner, Bernhard Plaimer 

![](https://cdn.mathpix.com/cropped/2024_03_25_a7542b9dd769c78fe27fg-1.jpg?height=111&width=286&top_left_y=316&top_left_x=217)
UNIVERSITY LINZ
Assignment 1

Analogue Signals and Systems

Information about assignments and in particular on Moodle submission modalities can be found in DSP-Tutorial_2024S_Courselnfo.pdf.

Submission deadline is Tue 16. April 2024, 08:00.

## Exercise 1 Complex Numbers (20\%)

These complex numbers are given:

$$
\begin{aligned}
& c_{1}=-5+j 3 \\
& c_{2}=\frac{\sqrt{2}}{2} e^{-\frac{j 3 \pi}{4}} \\
& c_{3}=\frac{1}{\sqrt{2}}+\frac{j 1}{\sqrt{2}}
\end{aligned}
$$

Calculate the following numbers and show the calculations/derivations in the report.

- $c_{4}=c_{1}+c_{2}$
- $c_{5}=c_{1} \cdot c_{2}$
- $c_{6}=\left|c_{3}\right|^{2}$
- $c_{7}=\arg \left(c_{3}\right)$
- $c_{8}=\frac{c_{1}}{c_{2}}$
- $c_{9}=c_{1} \cdot c_{1}^{*}$

Subsequently check your results with Matlab. Useful functions in this context are abs and angle. You do not need to add those checks to your report, or show the corresponding code.

## Exercise 2 Fourier Transform (25\%)

The lecture notes show the following Fourier transform pair for the cosine wave (DSP_2.pdf, page 37):

$$
x(t)=\hat{X} \cos \left(2 \pi f_{0} t\right) \leftrightarrow X(f)=\frac{\hat{X}}{2} \delta\left(f-f_{0}\right)+\frac{\hat{X}}{2} \delta\left(f+f_{0}\right)
$$

Mathematically proof this relation. To do so, use Eulers formula to express the cosine in the time domain as a sum of complex exponentials and the Fourier transform of a complex exponential function from DSP_2.pdf, page 38.

Add a diagram of $X(f)$ in the report (draw the real and the imaginary part of $X(f)$ in the same diagram).

## Exercise 3 Time Shift and Phase (20\%)

Given are two sines according to the following formula

with $f_{1}=1 \mathrm{~Hz}$ and $f_{2}=3 \mathrm{~Hz}$.

$$
x_{i}(t)=\sin \left(2 \pi f_{i} t\right), \text { with } i \in\{1,2\}
$$

All two sines are time delayed by $\tau=0.1 \mathrm{~s}$ to yield

$$
y_{i}(t)=\sin \left(2 \pi f_{i}(t-0.1)\right) \text {. }
$$

This corresponds to a phase shift. Thus, the delayed sines may also be written as

$$
y_{i}(t)=\sin \left(2 \pi f_{i} t+\phi_{i}\right) .
$$

a) Calculate the phase shifts $\phi_{i}$ for each sine, and verify that this corresponds to the "Shift Theorem" of the Fourier Transform (DSP_2.pdf, page 41).

b) For both sines in separated plots: Plot the original signal, the time delayed signal and the phase shifted signal. Since the latter two are identical, show this by plotting the first with a solid line and the overlaid one in a different colour with a dashed line. Plot each signal from 0 to $1 \mathrm{~s}$. In Matlab use the following time-vector: $\mathrm{t}=0: 0.001: 1$.

## Exercise 4 Linearity and Time Invariance (35\%)

Examine the following systems (input $x(t)$ and output $y(t)$ ) for linearity and time invariance.

Clearly show the mathematical derivations and state if the systems are linear and/or time-invariant.

- $y(t)=(x(t))^{2}$
- $y(t)=x(t) \cdot \sin \left(\Omega_{0} t\right)$

