---
layout: post
title:  "Image Filters"
date:   Tue May  2 08:50:14 PDT 2017
categories:
---


## Notebooks
- [Reverb]({{site.url | append:site.baseurl}}/nb/Reverb.html)
- [Audio Filters (loose ends)]({{site.url | append:site.baseurl}}/nb/Audio Filters (loose ends).html)
- [Image Filters]({{site.url | append:site.baseurl}}/nb/Image Filters.html)


## Reading

[The Scientist and Engineer's Guide to Digital Signal Processing: Chapter 6 - Convolution](http://www.dspguide.com/ch6.htm)


## Homework 4

> Due Tuesday, May 9 by 0600


### Problem 1 (40%)

Download the three HW4 audio files below. For each clip, compute the DFT of the entire file and then identify the index of the most prominent peaks in its magnitude spectrum. The audio files are encoded with a sampling rate of 44100 Hz -- what frequencies (in Hz) correspond to the bins with the most prominent peaks?

Hint: use the fft.rfft and argmax functions. Compute one real FFT with frame size equal to the number of samples for each file.


#### Audio Files:
- [glockenspiel.wav](http://w2.mat.ucsb.edu/201A/2016/res/glockenspiel.wav)
- [piano.wav](http://w2.mat.ucsb.edu/201A/2016/res/piano.wav)
- [tom.wav](http://w2.mat.ucsb.edu/201A/2016/res/tom.wav)


### Problem 2 (40%)

Using the same audio files, compute each clip's autocorrelation function and use it to identify the most salient frequency components (in Hz) in the signal. How do these results compare to your findings in HW4?

Hint: use the acorr() function and use the lags associated with the most prominent peaks in the autocorrelation output to calculate the corresponding frequency (recall that these files are sampled at 44100 Hz).


### Problem 3 (20%)

Briefly discuss the pros and cons of these two approaches. Under what circumstances would autocorrelation yeild "better" results than the DFT and vice versa?

- - -

## Homework 5

> Due Thursday, May 11 0600

Submit in writing your final project proposal. Provide details on your goals and deliverables. Discuss the technologies and tools you will use to achieve them.


- - -

## Homework 6

> Due Tuesday, May 16 0600

Refresh your memory on [Audio Filters](http://w2.mat.ucsb.edu/201A/nb/Audio%20Filters.html).


### Problem 1 (50%)

Implement and test a [DC Blocker](https://ccrma.stanford.edu/~jos/fp/DC_Blocker.html) filter. Make a semi-complex signal with some DC offset. For instance, mix 3 sine waves of different frequencies with some constant, non-periodic signal with amplitude between -1 and 1. Then design a filter that, when applied to your signal, removes the DC but leaves the sine waves (mostly) untouched. Use `scipy.signal.freqz` to plot the frequency and phase response of your filter. Use `scipy.signal.lfilter` to apply your filter and `numpy.fft.rfft` to show the resulting signal.


### Problem 2 (50%)

Audio signals commonly suffer from ["mains hum"](https://en.wikipedia.org/wiki/Mains_hum). Given [this example of mains hum](http://www.mat.ucsb.edu/201A/nb/Mains_hum_60_Hz_01.wav), design a filter to clean up [this noisy recording](http://www.mat.ucsb.edu/201A/nb/AlanWattsWithMainsHum.wav). Start by plotting the magitude spectrum of the mains hum. Use both autocorrelation and the DFT to characterize this signal: Where are the peaks of its spectrum? What, if any, pattern do you see in the spectral peaks? How broad/narrow are the peaks? Design a filter to combat the scourge of mains hum. This filter should "flatten the spectrum" of a clip of mains hum noise. It should reduce the energy of any signal at the spectral peaks of mains hum. Apply this filter to the given noisy signal. Plot the magnitude spectrum of the resulting signal. Discuss how well/badly your filter worked.

