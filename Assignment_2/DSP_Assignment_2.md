# Digital Signal Processing Tutorial (382.047/64/66/67/68/69/70), 2024S 

![](https://cdn.mathpix.com/cropped/2024_04_16_05aa650c2cf9d2378737g-1.jpg?height=111&width=285&top_left_y=316&top_left_x=220)

JOHANNES KEPLER UNIVERSITY LINZ

Matthias Wagner, Bernhard Plaimer

Assignment 2

Discrete Time Signals, Convolution, DTFT

Information about assignments and in particular on Moodle submission modalities can be found in DSP-Tutorial_2024S_Courselnfo.pdf.

Submission deadline is Tuesday, April 30th, 2024, 08:00.

Exercise 1 Discrete Time Signals (30\%)

(a) The following discrete time signals should be plotted in Matlab as indicated in Fig.1.

$$
\begin{array}{ll}
x_{1}[n]=-4 \delta[n+3]+4 \delta[n]-\delta[n-3]+2 \delta[n-7] & \text { for }-5 \leq n \leq 10 \\
x_{2}[n]=e^{-0.31 n} & \text { for }-5 \leq n \leq 10 \\
x_{3}[n]=3 \sin \left(2 \pi \frac{3.5}{64} n\right) & \text { for } 0 \leq n \leq 256 \\
x_{4}[n]=-\cos \left(\frac{9}{64} n\right) & \text { for } 0 \leq n \leq 256
\end{array}
$$

- To indicate the discrete time nature of the signals the stem command should be used, unless the signal length becomes too long in which case the plot command should be used instead. You should choose the ideal way to plot the signals.
- Extend the Matlab script dsp_A2_1.m. Useful commands are figure, stem, plot, subplot, xlabel, ylabel, title, legend, hold on, grid on, pi.
- You can use the provided function impseq.

![](https://cdn.mathpix.com/cropped/2024_04_16_05aa650c2cf9d2378737g-1.jpg?height=300&width=1063&top_left_y=1740&top_left_x=585)

Fig. 1: Required arrangement of plots.

(b) What is the normalized angular frequency $\Omega$ for $x_{3}[n]$ and $x_{4}[n]$.

(c) Are the signals $x_{3}[n]$ and $x_{4}[n]$ periodic? If yes, what is their fundamental period?

(d) Write the Matlab function custom_power which calculates the mean power of a discrete time periodic signal according to $P=\frac{1}{N} \sum_{n=0}^{N-1}|x[n]|^{2}$.

Pass exactly one signal period to this function to calculate the powers of all periodic (!) signals in (a).

(e) Now assume that all signals in (a) are zero outside the plot range (e.g. $x_{2}[11]=0$ ).

Write a function energy which calculates the signal energy according to $W=\sum_{n=-\infty}^{\infty}|x[n]|^{2}$.

Determine the energies for all these time-limited signals $x_{1}[n]$ to $x_{4}[n]$.

(f) Collect all the signal powers of (d) and signal energies of (e) in a single table in your protocol.

## Exercise 2 Convolution-1 (20\%)

The signal $x[n]=(3,-1,2,0,1)$ at sample times $n=(0,1,2,3,4)$ is the input to an LTI system with impulse response $h[n]=(2,3,4,1)$ at sample times $n=(0,1,2,3)$.

(a) How long is the output signal $y[n]$ ?

(b) Manually calculate the output signal $y[n]$.

## Exercise 3 Convolution-2 (25\%)

The impulse response of an LTI system is $h[n]=(0.25,0.5,0.25)$ at sample indices $n=(0,1,2)$.

The input signal is $x[n]=\cos \left(\frac{2 \pi}{20} n\right)$ for $0 \leq n<50$.

(a) What is the length $L y$ of the output signal $y[n]$ ?

(b) Implement the convolution operation $y[n]=\sum_{i=0}^{L_{h}-1} h[i] x[n-i]$ in Matlab as 2 nested forloops to calculate all $L_{y}$ output samples of $y[n]$. The outer for-loop increments the output index $n$, the inner for-loop increments the memory index $i$.

(c) Plot the signal $y[n]$.

(d) Verify the correct implementation of the convolution using the Matlab function conv. Plot both signals on top of each other, the lower one in solid line style the top in dashed style and provide a legend to your plot.

## Exercise 4 Discrete Time Fourier Transform (25\%)

The time discrete sequence $x[n]=(0.8)^{|n|}(u[n+10]-u[n-11])$ should be transformed to the frequency domain by using the discrete time Fourier transform (DTFT). As $x[n]$ has finite support (that means it is a sequence of finite length), $X\left(e^{j \Omega}\right)$ can be determined numerically via Matlab (or alternatively Octave, Python).

(a) Create a Matlab function, that is able to calculate the DTFT of a finite sequence. The function should provide the following interface:

![](https://cdn.mathpix.com/cropped/2024_04_16_05aa650c2cf9d2378737g-2.jpg?height=363&width=1619&top_left_y=1882&top_left_x=279)

Try to avoid for loops! You are still allowed to use for loops, however there will be a small deduction in points for the case you need to use for loops.

(b) Plot magnitude and phase response of $X\left(e^{j \Omega}\right)$ for the interval $-\pi \leq \Omega \leq \pi$ within single subplots. What do you observe for the phase response (hint: you should have a close look at the scaling of the $y$ axis)?

(c) Vary the parameter $\Omega$. What do you observe in the spectrum?

