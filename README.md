# Digital-Signal-Processing--FIR-LOW-PASS-FILTER-DESIGN
## AIM:
To generate design of low pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Low Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM:
<pre>
clc; % clear screen
clear all; % clear screen
close all; % close all figure windows
wc=input('enter the value of cut off frequency');
N=input('enter the value of filter');
alpha=(N-1)/2;
eps=0.001;
%Low Pass Filter Coefficient
n=0:1:N-1;
hd=sin(wc*(n-alpha+eps))./(pi*(n-alpha+eps))
%Hanning Window Sequence
n=0:1:N-1;
wh=0.5-0.5*cos((2*pi*n)/(N-1))
hn=hd.*wh
% Plot the Low Pass Filter with Hanning Window Technique
w=0:0.01:pi;
h=freqz(hn,1,w);
plot(w/pi,abs(h),'ms');
</pre>
## OUTPUT:
<img width="701" height="622" alt="image" src="https://github.com/user-attachments/assets/d302fbe9-2540-4ba1-bc5d-87ac3d6a6753" />

## RESULT:
<img width="641" height="380" alt="Screenshot 2026-03-25 212531" src="https://github.com/user-attachments/assets/ffb06b91-c5a4-4899-a8c6-c236d42c7ea2" />
