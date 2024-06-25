# z-Transform, Digital Filters 

Information about assignments and in particular on Moodle submission modalities can be found in DSP-Tutorial_2024S_CourseInfo.pdf. Submission deadline is Fr., July 5, 2024, 08:00.

## Exercise 1 Signal Distortion and Group Delay (20\%)

Generate three periods of the signal

$$
x[n]=\sum_{i=1}^{4} \frac{1}{2 i-1} \sin (2 \pi 0.005(2 i-1) n)
$$

and load (MATLAB command load) the provided mat file Filter_coefficients.mat. This file contains the filter coefficients of an FIR filter (b1 and a1) and the filter coefficients of an IIR filter (b2 and a2). Both filters are designed to fulfil the same design criteria (filter specification). Filter with both the FIR and the IIR filter the signal $x[n]$ and observe the signal distortion. Show and discuss the results in your report.

## Exercise 2 z-Transform (25\%)

Consider the difference equation of a recursive LTI system

$$
y[n]=x[n]-\frac{1}{15} y[n-1]+\frac{2}{5} y[n-2]
$$

(a) Sketch the block diagram of the LTI system corresponding to the given difference equation.

(b) Determine the filter type (FIR or IIR) and explain your choice in the report.

(c) Compute the transfer function $H(z)=\frac{Y(z)}{X(z)}$.

(d) Calculate the poles and zeros of $H(z)$ and include a sketch of the pole-zero map in your report. Also include the region of convergence (ROC) in the pole-zero map.

(e) Is the system stable? Explain your answer.

## Exercise 3 Recursive Filter (25\%)

Let the poles and zeros of a recursive filter be given:

- Zeros: $N_{1}=-1, N_{2}=j, N_{3}=-j$
- Poles: $P_{1}=0, P_{2}=0.75+j 0.25, P_{3}=0.75-j 0.25$

(a) Does this filter have real coefficients? Justify your answer.

(b) Draw a sketch of the pole-zero map.
(c) State the transfer function, first with polynomials of $z^{-i}, i=0,1,2,3, \ldots$, and afterwards with polynomials of $z^{+i}$.

(d) Draw the block diagram of a direct-form-l implementation of the filter and specify the coefficient values in the block diagram.

(e) Plot the magnitude and phase response of the filter in MATLAB.

(f) Plot the impulse response of the filter for $0 \leq n \leq 50$ in MATLAB.

## Exercise 4 Lowpass Filter Design (30\%)

An analogue signal is sampled with a sampling frequency $f_{\mathrm{s}}=20 \mathrm{kHz}$ and filtered subsequently. The digital lowpass filter should exhibit the following specification:

- Passband cutoff frequency: $f_{\text {pass }}=3.4 \mathrm{kHz}$
- Stopband cutoff frequency: $f_{\text {stop }}=4 \mathrm{kHz}$
- Allowed ripple in the passband: $\pm 5 \%$
- Minimum stopband attenuation: $45 \mathrm{~dB}$

(a) Specify the normalized radian frequencies for the passband $\Omega_{\text {pass }}$ and the stopband $\Omega_{\text {stop }}$, the passband tolerance $\delta_{1}$ and the stopband tolerance $\delta_{2}$. Hint: Be sure to use the decadic logarithm $\log 10$ ( ) for conversion to decibels.

(b) What is the ideal impulse response $h_{\text {ideal }}[n]$ for the ideal frequency response

$$
H_{\text {ideal }}(\Omega)= \begin{cases}1 & \text { for } 0 \leq|\Omega| \leq \Omega_{0} \\ 0 & \text { for } \Omega_{0} \leq|\Omega| \leq \pi\end{cases}
$$

with $\Omega_{0}=\frac{\Omega_{\text {pass }}+\Omega_{\text {stop }}}{2}$ ?

(c) Which two measures are necessary to deduce a realizable FIR system of order $N$ from the ideal impulse response $h_{\text {ideal }}[n]$ ?

(d) How can the decrease to the specified filter order $N$ be interpreted, and which effect on the frequency response of the realizable filter does that have?

(e) Design an FIR filter of order $N=20$ with a rectangular window with a corner radian frequency $\Omega_{0}$. Plot its frequency response and the tolerance scheme in one plot. To this end, complete the provided file dsp_5_4.m.

(f) Is the tolerance scheme being violated? Can the tolerance scheme be fulfilled by increasing the filter order to $N=90$ ?

(g) Now, use a hamming window instead of the rectangular window (for $N=90$ ) and assess the result.

(h) Use the MATLAB filterDesigner to design an elliptic IIR filter fulfilling the above described requirements. What is the order of this filter? What is the disadvantage of this filter?

