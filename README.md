# Denoising_SR
* Hongik University graduaion project


## Overview
![image](https://user-images.githubusercontent.com/36150943/91537587-8028c600-e951-11ea-817d-eee18bee4481.png)
![image](https://user-images.githubusercontent.com/36150943/91537537-68e9d880-e951-11ea-9a12-6b6ec8c4e214.png)
> __Abstract__: _this model based on [DnResnet](https://ieeexplore.ieee.org/document/8575286), [EDSR](https://arxiv.org/abs/1707.02921), [DBPN](https://arxiv.org/abs/1803.02735)
to solve noised super resolution problem. first of all, we trained EDSR model with not noised low resolution images, and then its pretrained model used for solving denoising 
problem by transfering trained parameters. in denoising phase, we used several data preprocessing method like unsharp filter to solve blurry outputs. the DnResnet independently trained to eliminate noises. then the outputs that were low resolution images with no noise
inputed to EDSR module. we used shuffle method not deconvolution for upsampling in EDSR and BackProjection module._


## Dataset 
* DIV2K(bicubic, wild)

## Result

![image](https://user-images.githubusercontent.com/36150943/91540392-b2d4bd80-e955-11ea-8751-c807dd09ca11.png)



## Dependencies
* python 3.6
* tensorflow
* numpy
* matplot
* opencv

## Reference
1. B Lim et al. [Enhanced Deep Residual Networks for Single Image Super-Resolution.](https://arxiv.org/abs/1707.02921) CVPR 2018
2. D Park et al. [Efficient Module Based Single Image Super Resolution for Multiple Problems](https://ieeexplore.ieee.org/document/8575286) 2018 IEEE
3. M Haris et al. [Deep Back-Projection Networks For Super-Resolution](https://arxiv.org/abs/1803.02735) arXiv:1803.02735
2. DIV 2K image set from : [DIV_2K](https://data.vision.ee.ethz.ch/cvl/DIV2K/)
