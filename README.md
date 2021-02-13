# Radio-Astronomy-Winter-School

(Radio Astronomy Winter School is a two week program organised by IUCAA and NCRA,Pune.Participants are selected on the basis of their merit and previous contribution in Astronomy.Each individual is provided with some data and asked to analyse and compare the behaviour of the data provided by different telescopic arrays at the same given time.)

GMRT Data Analysis

When we observe the sky using a telescope, although we aim to receive the signals only from celestial sources, what we actually get is a mix of terrestrial and celestial signals. Man-made signals that get mixed with the celestial signals received by radio telescopes are termed as Radio Frequency Interference (RFI).

This EDA is based towards learning about the signals and the corruption due to RFI. The origin of RFI and the effect on the data also hold surprises - like the microwave emission being mistaken as a new kind of burst or finding RFI from flights ! Two ascii data files at are used and rest are for comparison(C11_1024_Packets_B3.out and C12_1024_Packets_B3.out). Each contains a list of 4194304 (1024*4096)points.These are voltages recorded from the dipoles on the antennas C11 and C12 of the GMRT. Each value was recorded every 2.5e-9 s which is the Nyquist sampling for the signal recorded with a bandwidth of 200 MHz. The antennas were tracking the source 3C286 in the sky when the data were recorded.The data used are:
uGMRT Band-3 (300 - 500 MHz ) data files:
I) C11_1024_Packets_B3.out and C12_1024_Packets_B3.out
II) C11_1024_Packets_B3_4.out and C12_1024_Packets_B3_4.out
uGMRT Band-5 (1050 - 1450 MHz) data files:
III) C11_1024_Packets_B5.out and C12_1024_Packets_B5.out
IV) C11_1024_Packets_B5_4.out and C12_1024_Packets_B5_4.out

1. Examination of the data:
   Voltages is plotted as a function of time.Voltage range,mean and rms is calculated.
   Histogram of voltages is plotted which is then made to Gaussian fit.Further, Mean and Sigma is calculated.
   Histogram of Voltage Square is plotted(Power spectrum).Mean and Standard deviation is calculated.
   
2. Obtaining a dynamic spectrum:
   From first dataset(C11_1024_Packets_B3.out) 512 points are taken at a time and Fourier Transformation is performed.The amplitude versus channel number (or frequency) is      plotted.
   The auto-correlation spectrum is calculated and plotted as an image with frequency and time on X and Y axes and the amplitude on the Z axis shown in colour scale.
   The cross-correlation spectrum is calculated and plotted in a similar way.
   
3. Statistics of the data in each channel:
   The mean/rms of each is calculated and plotted against the channel number.The expected rms is calculated(calculated as mean divided by the square root of the product          2*time*bandwidth) and then compared with the observed rms in order to find the location with significant RFI.

4. Relative importance of the phase and magnitude of the recorded data:
   Voltages are made to retain only the sign (one bit the data) and then all the spectra (as above) is observed.(To know the fluctuation and stability of array which is          observing the data.)
   Now the modulus of voltages are taken and the spectra is obtained as given before.(In order to study the behaviour of data)
   
   Acknowledgement: The data files were recorded and made available for RAWS2020 by Kaushal Buch and his team at the GMRT.
