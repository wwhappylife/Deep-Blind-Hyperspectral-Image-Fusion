# Deep-Blind-Hyperspectral-Image-Fusion

This repository is for DBIN introduced in the following paper：

[1] Wu Wang, Weihong Zeng, Yue Huang, Xinghao Ding and John Paisley, "Deep Blind Hyperspectral Image Fusion", ICCV 2019

The code is built on Tensorflow and tested on Ubuntu 14.04/16.04 environment (Python3.6, CUDA8.0, cuDNN5.1) with 1080Ti GPUs.

## Introduction

Hyperspectral image fusion (HIF) reconstructs high spatial
resolution hyperspectral images from low spatial resolution
hyperspectral images and high spatial resolution
multispectral images. Previous works usually assume that
the linear mapping between the point spread functions of
the hyperspectral camera and the spectral response functions
of the conventional camera is known. This is unrealistic
in many scenarios. We propose a method for blind
HIF problem based on deep learning, where the estimation
of the observation model and fusion process are optimized
iteratively and alternatingly during the super-resolution reconstruction.
In addition, the proposed framework enforces
simultaneous spatial and spectral accuracy. Using three
public datasets, the experimental results demonstrate that
the proposed algorithm outperforms existing blind and nonblind
methods.

## Train
For the CAVE dataset, we first convert the image to *.mat* format, and then generate the *tfrecord* file, which can improve the data reading speed. For the CAVE, Harvard, and NTR2018 data sets, we split the image into 64×64 image blocks without any data augmentation.
Unlike the normalization of natural images, we normalize each spectrum of each image to 0 to 1, because some spectral values are very close.
## Test
At the time of testing, we also first converted the image into a tfrecord file. When calculating PSNR, SSIM, SAM, and ERGAS, we used the same code as DHSIS（Deep Hyperspectral Image Sharpening）, here we thank the code provided by Renwei Dian.
## Results
 ![image](https://github.com/wwhapplife/Deep-Blind-Hyperspectral-Image-Fusion/raw/master/image_folder/CAVE.png)
## Citation

## Acknowledgements

