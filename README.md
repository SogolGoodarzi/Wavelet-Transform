# Wavelet-Transform
* <p align="justify"> First, save the audio file "sonata.mp3" in an array and specify its sampling frequency. As you can see, this audio has two channels. Store the two channels in two new arrays and plot them in a graph in the time domain (in seconds). </p>

![image](https://github.com/SogolGoodarzi/Wavelet-Transform/assets/125180530/b7dd9d8e-e508-4432-9020-bfdb3d49476d)

<p align="justify"> As mentioned, this sound has two channels. We store each channel in separate arrays named ch1 and ch2 and draw the signal shape of these two channels as below. </p>

![image](https://github.com/SogolGoodarzi/Wavelet-Transform/assets/125180530/95f3b1ea-e030-469d-835d-625ad701addd)

##### Similarities:
<p align="justify"> The similarity that is evident in the two plotted signals is that the overall shape of both of them is almost the same. Carefully in the time domain, we can see that the time span of the two channels is similar, and the domains related to each time in the two channels are located correspondingly and are placed on top of each other. </p>

##### Differences:
<p align="justify"> The difference that can be mentioned for these two channels is that at some times the range of one of the channels (channel 1) was larger than the other, but the important point is that this difference in range is small and with a good approximation. It can be said that the signal of both channels is similar and the same. </p>

* We draw the Fourier transform of the previous two channels as follows:

![image](https://github.com/SogolGoodarzi/Wavelet-Transform/assets/125180530/ee95219e-11c3-4d42-91de-1efa37651d99)

<p align="justify"> According to the diagram, it can be said that the frequency band of the two channels is approximately between $1.5×10^{4}$ Hz and $2×10^{4}$ Hz, which if we want to express more precisely, the frequency band of the channels is equal to $1.75×10^{4}$ Hz. </p>

<p align="justify"> In order to draw the power spectrum of the signal, we must actually draw the density of the signal spectrum, which is related to the Fourier transform of the signal as follows. </p>

![image](https://github.com/SogolGoodarzi/Wavelet-Transform/assets/125180530/4c2ea83c-1feb-4b81-9603-14995ea73164)

So, using the above relationship, we draw the power spectrum of channel 1 as below:

![image](https://github.com/SogolGoodarzi/Wavelet-Transform/assets/125180530/9d61b914-0ce5-4a90-a45e-d4790de8e8ff)

**Main frequencies:** <p align="justify">According to the power spectrum drawn in the diagram above, we can see that the main frequencies or stronger frequencies, i.e. the range where the power range is higher, are in the frequency range of zero to 5 kHz. If we want to be more precise and consider only very large peaks, this range becomes smaller and includes from zero to 2.5 kHz. </p>

* <p align="justify"> In this step, we want to identify what frequencies the signal has in different time intervals. Select one of the channels and draw its spectrogram using the command spectrogram(x, window, size, noverlap, nfft, fs). The result for channel 1 is as follows: </p>

![image](https://github.com/SogolGoodarzi/Wavelet-Transform/assets/125180530/135e3f0c-7b58-48d8-aa44-900af6d08635)

**Comparison of the spectrogram and the original signal:** <p align="justify"> If you pay close attention to the graph drawn above, we can see that the frequency power is high in the time zone between 0.8 minutes and 1 minute. In the chart plotted for the channels in the time domain, if we pay close attention, we can see that in the time area between approximately 48 seconds and 60 seconds (that is, the same time area that was detected in the spectrogram), we also have the highest amplitude for the signal. Similarly, in the two graphs that are plotted side by side in the figure below, if we pay close attention, we can see that in a small time period before the previous time period that was mentioned, we have a blue area in the spectrogram diagram, which corresponds to it in the channel 1 signal diagram. We also see that the amplitude of the signal is very low and at zero, which indicates a break or silence in the sound. </p>

![image](https://github.com/SogolGoodarzi/Wavelet-Transform/assets/125180530/49bba81a-750a-4959-aebc-4e3b25816edf)

#### Overall Evaluation:
**First interval:** <p align="justify"> Now we listen to the sound according to the question. For the first part, that is, from the beginning of the sound to the 48th second, we can see that at the beginning, other instruments are played except the violin, and from the 10th second onwards, this instrument is also played along with the others, and also the speed of playing these instruments in comparison It is less with the next section. If you pay attention to the spectrogram diagram, in this time zone for low frequencies (between 0 and 5 kHz), we see a yellow color that expresses the frequency power between 60 and 50 dB/Hz, so it can be said that low frequencies, in this time zone, They have more power or power, which is due to the fact that the violin is played (it is violin making, the frequency of which is lower than other instruments.) which is related to the playing of other instruments that have a higher frequency than the violin. </p>

![image](https://github.com/SogolGoodarzi/Wavelet-Transform/assets/125180530/fb0aabd6-09eb-4a99-a50d-287dd891fbe1)

**Second interval:** <p align="justify"> In this area, which is between 0.8 minute and 1 minute, we see the blue color, which corresponds to the frequency power between 110 and 130 dB/Hz. Since we see this blue band in all frequency ranges, from 0 to 25 kHz, it can be assumed that no musical instrument is played in this area. </p>

![image](https://github.com/SogolGoodarzi/Wavelet-Transform/assets/125180530/8ea61495-54c2-47fd-bdc8-39b8be0ae328)

**Third interval:** <p align="justify"> In this range, for frequencies between zero and 5 kilohertz, i.e. low frequencies, we see yellow color, which has the highest frequency power. If we pay attention to the sound of this area, we can see that the only instrument played at this time was the violin, and its sound can be distinguished from other instruments, and the speed of playing this instrument is also higher in this area than other times, which is the same. This has caused yellow color to appear with more power in this area. For higher frequencies, similar to the analysis of the previous parts, because it is related to other instruments, we see the blue color, which has a lower frequency power. </p>

![image](https://github.com/SogolGoodarzi/Wavelet-Transform/assets/125180530/73dd7869-0318-404d-bdb6-a811967acb0d)

**Fourth interval:** <p align="justify"> In this area, we first see the blue color, the reason is that the violin is played with a lower intensity and speed than the previous area, which is almost similar to hearing a pause or approximate silence, so the frequency power is lower in this area. In the seconds after that, we see the yellow area again, which is due to the violin being played with more intensity than before. </p>

![image](https://github.com/SogolGoodarzi/Wavelet-Transform/assets/125180530/57794f27-4431-43a2-b0d6-19158f4f7b78)

* <p align="justify"> The reason why two channels are used to store some audio files is that some audio players have two outputs for playing audio. For example, hands-free or headset are two examples of these devices. </p>

* <p align="justify"> Now we want to evaluate the effect of changing different arguments of the function on frequency and time transparency. So, look at the following figures. </p>

![image](https://github.com/SogolGoodarzi/Wavelet-Transform/assets/125180530/87afbfdb-1f86-48a5-938c-3164c3f101d6)

![image](https://github.com/SogolGoodarzi/Wavelet-Transform/assets/125180530/d3fbff0e-4caf-49ed-8d5b-2aec03f92c85)

#### Conclusion:
<p align="justify"> The smaller the size of the window, the more accurately and accurately we can comment on the occurrence time of each frequency. On the contrary, we can say that the smaller the size of the windows, the more accurately we can comment on the characteristics of the frequency and the information related to it, but it is not possible to accurately inform about the occurrence time of each frequency. In other words, it can be said that increasing the size of the window will increase the resolution of the frequency domain, and decreasing it will increase the resolution of the time domain, which can be seen in the graphs above. Another point is that the more we increase the value of the noverlap parameter, the better the resolution is, because we have increased the number of overlapped samples in the windows, so the number of new samples in each window is less, and this means with smaller steps of the window. We have shifted it, which causes better accuracy. Regarding the nfft parameter, we can say that the more we increase it, the better the accuracy and resolution will be. </p>  

<p align="justify"> In this section, we learned about the short-time Fourier transform. The main disadvantage of STFT transformation is that the smaller the window size, the more accurately we can determine when a frequency occurred in the original signal, but on the other hand, we get less information about the frequency value of the original signal. Similarly, the larger the window size we choose, the more information we will get about the frequency value and the less information we will get about the frequency occurrence time. A better way to analyze a signal with a dynamic frequency spectrum is to use Wavelet Transform. In this transformation, the original signal can be multiplied by the wavelet at different moments of time. In the first step, we start with the initial points of the signal and gradually move the wavelet towards the end of the signal. This operation is called convolution. After we have done the convolution with the original wavelet signal, we can scale it to make it bigger and repeat the process again. Therefore, the wavelet transformation of a one-dimensional signal gives us information of two dimensions, time and scale (in other words, frequency).  </p>

![image](https://github.com/SogolGoodarzi/Wavelet-Transform/assets/125180530/3b13598e-ebcb-4a6b-b412-460347c8694f)

* <p align="justify"> In the wavelet transform, the two dimensions of the spectrogram are time and scale (the scale here is equivalent to the frequency in the Fourier transform). According to the above definition, the scale can be converted to pseudo-frequency from the following relationship: </p>

![image](https://github.com/SogolGoodarzi/Wavelet-Transform/assets/125180530/c3a4b30d-8a27-4953-bd94-f2eb2c795274)

<p align="justify"> In this relation, $f_{a}$ is equal to the pseudo-frequency, $f_{c}$ is equal to the central frequency of the mother wavelet signal, and a is the scale factor. A larger comparison coefficient is equivalent to lower frequencies, so by scaling the wavelet signal in the time domain, smaller frequencies can be analyzed, and as a result, we reach a higher resolution in the frequency domain and a lower resolution in the time domain. In a similar way, a lower resolution in the frequency domain and a higher resolution in the time domain can be achieved with a smaller scale. So it can be understood that the scale is the inverse of the frequency in the Fourier transform. </p>
