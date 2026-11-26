# FIR-FILTER-DESIGN
# EXP 4 b: Design-of-FIR-Digital-Filter-using-Hamming-Window

# AIM 1:  To perform Design-of-LOWPASS FIR-Digital-Filter-using-Hamming-Window using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
clc; clear; close;

N = 21;
wc = %pi / 2;
alpha = (N - 1) / 2;

hd = zeros(1, N); for n = 0 : N-1 if n == alpha then hd(n+1) = wc / %pi; else hd(n+1) = sin(wc * (n - alpha)) / (%pi * (n - alpha)); end end

w = zeros(1, N); for n = 0 : N-1 w(n+1) = 0.54 - 0.46 * cos((2 * %pi * n) / (N - 1)); end

h = hd .* w;

[H, w_freq] = frmag(h, 256);

figure; subplot(2, 1, 1); plot2d3(0:N-1, h);
plot(0:N-1, h, 'ro');
xtitle('Impulse Response', 'n', 'h(n)'); xgrid(1);

subplot(2, 1, 2); H_dB = 20 * log10(H);
plot(w_freq, H_dB); xtitle('Magnitude Response', 'Normalized Frequency', 'Magnitude (dB)'); xgrid(1);

# OUTPUT: 
<img width="1917" height="893" alt="image" src="https://github.com/user-attachments/assets/ea8c9e6a-da3a-46a3-96f2-79ec6d320713" />


# RESULT: 

Thus design of low pass FIR digital filter using-Hamming-Window waveforms were plotted and output was verified.

# AIM 2: To perform DESIGN OF HIGH PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
clear; close;

N = 21;
wc = %pi / 2;
alpha = (N - 1) / 2;

hd = zeros(1, N); for n = 0 : N-1 if n == alpha then hd(n+1) = 1 - (wc / %pi); else hd(n+1) = -sin(wc * (n - alpha)) / (%pi * (n - alpha)); end end

w = zeros(1, N); for n = 0 : N-1 w(n+1) = 0.54 - 0.46 * cos((2 * %pi * n) / (N - 1)); end

h = hd .* w;

[H, w_freq] = frmag(h, 256);

figure; subplot(2, 1, 1); plot2d3(0:N-1, h);
plot(0:N-1, h, 'ro');
xtitle('Impulse Response', 'n', 'h(n)'); xgrid(1);

subplot(2, 1, 2); H_dB = 20 * log10(H);
plot(w_freq, H_dB); xtitle('Magnitude Response', 'Normalized Frequency', 'Magnitude (dB)'); xgrid(1);

# OUTPUT: 
<img width="1917" height="897" alt="image" src="https://github.com/user-attachments/assets/68658a53-3ed3-4f3d-b683-ed25f07c1dc4" />


# RESULT: 
Thus design of HIGH pass FIR digital filter using-Hamming-Window waveforms were plotted and output was verified.

# AIM 3: To perform DESIGN OF BAND PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
clc; clear; close;

N = 21;
wc1 = %pi / 4;
wc2 = 3 * %pi / 4;
alpha = (N - 1) / 2;

hd = zeros(1, N); for n = 0 : N-1 if n == alpha then hd(n+1) = (wc2 - wc1) / %pi; else hd(n+1) = (sin(wc2 * (n - alpha)) - sin(wc1 * (n - alpha))) / (%pi * (n - alpha)); end end

w = zeros(1, N); for n = 0 : N-1 w(n+1) = 0.54 - 0.46 * cos((2 * %pi * n) / (N - 1)); end

h = hd .* w;

[H, w_freq] = frmag(h, 256);

figure; subplot(2, 1, 1); plot2d3(0:N-1, h);
plot(0:N-1, h, 'ro');
xtitle('Impulse Response', 'n', 'h(n)'); xgrid(1);

subplot(2, 1, 2); H_dB = 20 * log10(H);
plot(w_freq, H_dB); xtitle('Magnitude Response', 'Normalized Frequency', 'Magnitude (dB)'); xgrid(1);

# OUTPUT: 
<img width="1917" height="893" alt="image" src="https://github.com/user-attachments/assets/ccc38a08-f1d8-4011-b9ae-70a0af5f19e1" />


# RESULT: 
Thus design of BAND pass FIR digital filter using-Hamming-Window waveforms were plotted and output was verified.

# AIM 4: To perform DESIGN OF BAND STOP FIR DIGITAL FILTER using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
clc; clear; close;

N = 21;
wc1 = %pi / 4;
wc2 = 3 * %pi / 4;
alpha = (N - 1) / 2;

hd = zeros(1, N); for n = 0 : N-1 if n == alpha then hd(n+1) = 1 - ((wc2 - wc1) / %pi); else hd(n+1) = (sin(wc1 * (n - alpha)) - sin(wc2 * (n - alpha))) / (%pi * (n - alpha)); end end

w = zeros(1, N); for n = 0 : N-1 w(n+1) = 0.54 - 0.46 * cos((2 * %pi * n) / (N - 1)); end

h = hd .* w;

[H, w_freq] = frmag(h, 256);

figure; subplot(2, 1, 1); plot2d3(0:N-1, h);
plot(0:N-1, h, 'ro');
xtitle('Impulse Response', 'n', 'h(n)'); xgrid(1);

subplot(2, 1, 2); H_dB = 20 * log10(H);
plot(w_freq, H_dB); xtitle('Magnitude Response', 'Normalized Frequency', 'Magnitude (dB)'); xgrid(1);

# OUTPUT: 
<img width="1917" height="891" alt="720033715-0b04911d-5881-43e1-b640-39e216b4a39b" src="https://github.com/user-attachments/assets/1b18351e-2ec0-4efe-b897-3710a56a796f" />


# RESULT: 
Thus design of BAND STOP FIR digital filter using-Hamming-Window waveforms were plotted and output was verified.
