# UNet-implementation
UNet :  Convolutional Networks for Biomedical Image Segmentation

The u-net is convolutional network architecture for fast and precise segmentation of images. 

Architecture (example for 32x32 pixels in the lowest resolution). Each blue box corresponds to a multi-channel feature map. 
The number of channels is denoted on top of the box. The x-y-size is provided at the lower left edge of the box. 
White boxes represent copied feature maps. The arrows denote the different operations.

![UNet architecture](https://lmb.informatik.uni-freiburg.de/people/ronneber/u-net/u-net-architecture.png)


```
#random image tensor
>>> image = torch.rand((1,1,572,572))
torch.Size([1, 2, 388, 388])
#output of UNet
tensor([[[[-0.1104, -0.1083, -0.1082,  ..., -0.1108, -0.1088, -0.1078],
          [-0.1099, -0.1078, -0.1075,  ..., -0.1069, -0.1108, -0.1088],
          [-0.1073, -0.1083, -0.1108,  ..., -0.1117, -0.1080, -0.1087],
          ...,
          [-0.1085, -0.1091, -0.1049,  ..., -0.1089, -0.1054, -0.1109],
          [-0.1139, -0.1094, -0.1111,  ..., -0.1101, -0.1081, -0.1094],
          [-0.1058, -0.1086, -0.1119,  ..., -0.1075, -0.1078, -0.1067]],

         [[ 0.0757,  0.0736,  0.0695,  ...,  0.0746,  0.0725,  0.0754],
          [ 0.0761,  0.0760,  0.0723,  ...,  0.0738,  0.0730,  0.0728],
          [ 0.0737,  0.0740,  0.0715,  ...,  0.0728,  0.0714,  0.0746],
          ...,
          [ 0.0793,  0.0739,  0.0711,  ...,  0.0731,  0.0759,  0.0706],
          [ 0.0739,  0.0737,  0.0725,  ...,  0.0697,  0.0762,  0.0760],
          [ 0.0736,  0.0739,  0.0733,  ...,  0.0705,  0.0748,  0.0747]]]],
       grad_fn=<MkldnnConvolutionBackward>)

```

https://arxiv.org/abs/1505.04597


