This is quick evaluation of different architectures functions performance on ImageNet-2012. 

The architecture is similar to common ones for ImageNet, but has differences:

1. Images are resized to small side = 128 for speed reasons.
2. Networks are initialized with [LSUV-init](http://arxiv.org/abs/1511.06422)


![CaffeNet128 test accuracy](/logs/architectures/img/0.png)
![CaffeNet128 test accuracy](/logs/architectures/img/2.png)
![CaffeNet128 test accuracy](/logs/architectures/img/6.png)

Architectures tested:

1. CaffeNet (pool5 size = 3x3)
2. HeNet [Convolutional Neural Networks at Constrained Time Cost](http://arxiv.org/abs/1412.1710). The difference with paper is VLReLU (converges faster at start) and no SPP pooling, instead used "classical" pool5
3. CaffeNetSPP, single scale training (SPP pool5 = 3x3 + 2x2 + 1x1) [Spatial Pyramid Pooling in Deep Convolutional Networks for Visual Recognition](http://arxiv.org/abs/1406.4729)]
4. ThinResNet-101 [Deep Residual Learning for Image Recognition](http://arxiv.org/abs/1512.03385) with BN, 1st attempt
5. TBD

P.S. Logs are merged from lots of "save-resume", because were trained at nights, so plot "Accuracy vs. seconds" will give weird results. 

