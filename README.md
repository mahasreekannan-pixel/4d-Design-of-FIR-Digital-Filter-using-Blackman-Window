# FIR-FILTER-DESIGN
# EXP 4 d: Design-of-FIR-Digital-Filter-using-Blackman-Window

# AIM 1:  To perform Design-of-LOWPASS FIR-Digital-Filter-using-Blackman-Window using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
<br>clc ; 
<br>close ; 
<br>M=input('Enter the Odd Filter Length ='); 
<br>Wc=input('Enter the Digital Cut off frequency ='); 
<br>alpha= (M -1)/2 // Center Value 
<br>for n = 1:M 
<br>if (n ==alpha+1) 
<br>hd(n) = Wc/ %pi ; 
<br>else 
<br>hd(n) = sin(Wc *((n -1)-alpha)) /(((n -1)-alpha)*%pi); 
<br>end 
<br>end 
<br>// Blackman Window 
<br>for n = 1:M 
<br>W(n) = 0.42-(0.5*cos((2*%pi*(n-1))/(M-1)))+(0.08*cos((4*%pi*(n-1))/(M-1))); 
<br>end 
<br>//Windowing filter coefficients 
<br>h = hd.*W; 
<br>disp(h,'Filter Coefficients are') 
<br>[hzm,fr]= frmag (h,256) ; 
<br>subplot(2 ,1 ,1) 
<br>plot(2*fr, hzm) 
<br>xlabel( ' Normalized Digital Frequency w'); 
<br>ylabel( 'Magnitude '); 
<br>title( ' Frequency Response of FIR LPF using Blackman Window ') 
<br>hzm_dB = 20* log10 (hzm); 
<br>subplot (2 ,1 ,2); 
<br>plot(2*fr , hzm_dB); 
<br>xlabel( ' Normalized Digital Frequency W' ); 
<br>ylabel( 'Magnitude in dB'); 
<br>title('Frequency Response of FIR LPF using Blackman Window');

# OUTPUT: 
<img width="486" height="350" alt="image" src="https://github.com/user-attachments/assets/e63fbd87-316b-454e-bad7-98bb0084d16f" />

<img width="456" height="375" alt="image" src="https://github.com/user-attachments/assets/19a936ce-9839-4e5e-9aa0-c10c1a677266" />


# RESULT: 

Thus design of low pass FIR digital filter using-Blackman-Window waveforms were plotted and output was verified.

# AIM 2: To perform DESIGN OF HIGH PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 


# OUTPUT: 


# RESULT: 
Thus design of HIGH pass FIR digital filter using-Blackman-Window waveforms were plotted and output was verified.

# AIM 3: To perform DESIGN OF BAND PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 


# OUTPUT: 


# RESULT: 
Thus design of BAND pass FIR digital filter using-Blackman-Window waveforms were plotted and output was verified.

# AIM 4: To perform DESIGN OF BAND STOP FIR DIGITAL FILTER using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 


# OUTPUT: 


# RESULT: 
Thus design of BAND STOP FIR digital filter using-Blackman-Window waveforms were plotted and output was verified.
