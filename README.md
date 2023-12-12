# DSP-image-process

I put my code in file “problem.m”.

The following is the image of Barbara :

![image](https://github.com/wayne540500/DSP-image-process/assets/69573286/4b95aec9-c562-4209-81b5-3081ad641259)

FIR linear phase minimax filter: 
This filter type is designed to have linear phase characteristics and minimize the maximum ripple in the passband.
FIR minimum phase filter: 
Derived from the linear phase filter by reflecting zeros outside the unit circle. This filter type satisfies the same specifications but may exhibit different characteristics.
Like the hint for step 2 says, I follow the same code method to show our pole zero diagram.
% Step 2: Design FIR Linear Phase Minimax Filter
Wp = 0.15 * pi;
Ws = 0.2 * pi;
[nfir, f0, m0, w] = firpmord([Wp, Ws], [1, 0], [0.05, 0.05]);
b_fir = firpm(nfir, f0, m0, w);
figure
zplane(b_fir); % Show z-plane of the filter

And this is the pole zero plot, we can see that there are 13 poles&zeros:

![image](https://github.com/wayne540500/DSP-image-process/assets/69573286/e53a01a9-22d7-423b-9e60-fd020f288509)

![image](https://github.com/wayne540500/DSP-image-process/assets/69573286/aee04d65-0ab5-40f9-b614-c31346303d4c)

I design my code to match the criteria of the hint.


And the following are the plot of magnitude response and phase response:

![image](https://github.com/wayne540500/DSP-image-process/assets/69573286/5ca5900d-4d8d-4860-9251-b69955396727)

Finally, we can see the result under 2 different FIR , the FIR Linear Phase one seems more brighter to me and the FIR Minimum Phase one looks darker:

![image](https://github.com/wayne540500/DSP-image-process/assets/69573286/c1d1007c-867a-459e-aff6-53b6ef9fe076)

The filter is applied horizontally, we can observe them from the code and the result image.
