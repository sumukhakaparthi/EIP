# Assignment 2
###### 15th May, 2018
###### B.V.S.G. Suraj, Batch 7 

## Dilated Convolutions
These convolutions are used to get increase the receptive field of a filter. This method doesn't comprimise on the resolution. Also, the computation is same as of a normal convolution.

The filter takes alternate pixels from the input and applies convolution. This way, the patterns which are situated far away from each other but belong to the same family are considered into the same feature map.

![](https://i.stack.imgur.com/tOg0g.png)

## Deconvolution

Deconvolution is is an upsampling method. In a loose manner, it is same as that of what convolutions do. The feature map or input to the deconvolution NN is padded and filters are applied. This way, bigger images are obtained. They try to generate an image of resolution same as of input images. The image need not be the same.

![](https://i.stack.imgur.com/f2RiP.gif)

## Max pooling
This is a downsampling method. The image is divided into sub-parts. Then, the max of each sub-part is taken. This way, the image is down-sampled.

Max pooling is used in convolution networks after convolution layers on the feature maps. The main reason we use maxpooling is to increase the receptive field. So, that the next convolution layers will learn 

![Maxpooling](http://amitkushwaha.co.in/images/cropped_max_pooling.gif)