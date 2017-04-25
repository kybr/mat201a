---
layout: post
title:  "Convolution and Audio Filters"
date:   Tue Apr 25 12:13:34 PDT 2017
categories:
---

[Notes](http://w2.mat.ucsb.edu/201A/2016/notes/Frequency_domain.html)

[Impulse response database](http://www.openairlib.net/auralizationdb)


## Homework 3

> Due Tuesday May 2nd 0600

Use cross-correlation (or auto-correlation) to find features or similarities/differences in/between images. Generate the cross-correlation matrix and extract the highest/lowest values in a way that makes sense with your particular material.

Treat this as an exploratory/creative exercise; Try various images and discover your goals. Analyze and discuss your process and results.

For instance, find an image that contains a smaller version of itself (See the [Droste effect](https://en.wikipedia.org/wiki/Droste_effect)). Make a scaled copy of this image such that it is about same size as the image within the image. Now use the cross-correlation techniques from the notebook [_Variance and Correlation_]({{ site.url | append:site.baseurl}}/nb/Variance%20and%20Correlation.html) to determine the coordinates of the internal image.

Or consider Danny Bazo's [_Escher Animator_](https://www.youtube.com/watch?v=Mp-MPIUWw9w) which allows a user to choose a square subsection of an image with slowly morphing patterns. Given the users square, how would you use cross correlation to find the nearest most similar square beyond some distance?

These are just examples. Try to come up with your own idea.

Ideally, your chosen material, goal, and/or technique are related to you research in some way. Explain how.

Show your work, explaining what you had to do and why. The notebook you turn in should present your idea and process well so that other people in the class can understand.


