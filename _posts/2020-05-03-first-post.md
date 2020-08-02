---
title: "MobileNet V1"
date: 2020-05-03 14:43:28
permalink: /posts/
author_profile: true
categories: DeepLearning
---
MobileNets: Efficient Convolutional Neural Networks for Mobile Vision Applications
=============
Andrew G. Howard, Menglong Zhu, Bo Chen, Dmitry Kalenichenko, Weijun Wang, Tobias Weyand, Marcj Andreetto, Hartwig Adam   
Google Inc.


# [Introduction]
* Propose  a streamlined architecture that uses depthwise separable convolutions to build light weight deep neural networks and two simple global hyperparameters that efficiently trade off between latency and accuracy
* A class of efficient models called MobileNets for mobile and embedded vision applications
* Focus on optimizing for latency but also yield small networks
  * Many papers on small networks focus only on size but do not consider

<center><img src="/assets/images/mobilenet_v1/mbn1.png" width="70%" height="70%"></img></center>

# [MobileNet Architecture]
1. Depthwise separable convolution
> The MobileNet model is based on depthwise separable convolutions which is a form of factorized convolutions which factorize a standard convolution into a depthwise convolution and a 1x1 convolution called a pointwise convolution
2. Network structure and training
3. Width multiplier: Thinner models
> Although the base MobileNet architecture is already small and low latency, many times a specific use case or application may require the model to be smaller and faster
4. Resolution multiplier: Reduced representation

## 1. Depthwise Separable Convolution
### * Standard convolution -> Depthwise convolution + Pointwise convolution
### * Depthwise convolution 
#### Apply a single filter to each input channel
### * Pointwise convolution
#### 1x1 convolution to combine the outputs the depthwise convolution
### * Computational cost
#### Standard convolution: D<sub>K</sub> x D<sub>K</sub>
#### Depthwise separable convolution:   

## 2. Network Structure and Training
### * The MobileNet structure is built on depthwise separable convolutions as mentioned in the previous section except for the first layer which is a full convolution
