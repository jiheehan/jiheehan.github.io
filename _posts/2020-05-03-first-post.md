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

1. Depthwise Separable Convolution
* Standard convolution -> Depthwise convolution + Pointwise convolution
* Depthwise convolution    
    Apply a single filter to each input channel
* Pointwise convolution   
    1x1 convolution to combine the outputs the depthwise convolution
* Computational cost   
    Standard convolution: D<sub>K</sub> x D<sub>K</sub> x M x N x D<sub>F</sub> x D<sub>F</sub>
    > depends multicatively on the number of input channels, the number of output channels, the kernel size and the feature map size    
    
    Depthwise separable convolution: D<sub>K</sub> x D<sub>K</sub> x M x D<sub>F</sub> x D<sub>F</sub> + M x N x D<sub>F</sub> x D<sub>F</sub>       
     * D<sub>K</sub>: spatial width, height of a kernel
     * D<sub>F</sub>: spatial width, height of a square input feature map
     * M: number of input channels
     * N: number of output channels
     
        <center><img src="/assets/images/mobilenet_v1/mbn2.PNG" width="100%" height="100%"></img></center>

2. Network Structure and Training
 * The MobileNet structure is built on depthwise separable convolutions as mentioned in the previous section except for the first layer which is a full convolution   
 * All layers are followed by a batchnorm and ReLU nonlinearity with the exception of the final fully connected layer which has no nonlinearity and feeds into a softmax layer for classification
 * A final average pooling reduces the spatial resolution to 1 before the finally connected layer
 * Counting depthwise and pointwise convolutions as separable layers, MobileNet has 28 layers
 
    <center><img src="/assets/images/mobilenet_v1/mbn3_4.PNG" width="100%" height="100%"></img></center>
    
    
3. Width Multiplier: Thinner Models
 * In order to construct smaller and less computationally expensive models, introduce a parameter &alpha   
 * The role of the width multiplier &alpha is to thin a network uniformly at each layer
 * For a given layer and width multiplier &alpha, the number of input channels M becomes &alpha M and the numver of output channels N becomes &alpha N
 * Computational Cost of a depthwise separable convolution with width multiplier &alpha    
     : D<sub>K</sub> x D<sub>K</sub> x &alpha M x D<sub>F</sub> x D<sub>F</sub> + &alpha M x &alpha N x D<sub>F</sub> x D<sub>F</sub>    
 * Width multiplier has the effect of reducing computational cost and the number of parameters quadratically by roughly &alpha<sup>2</sup>

