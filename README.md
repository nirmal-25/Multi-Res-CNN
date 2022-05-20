# Multiresolution CNNs for Video Classification

Implemented Multiresolution CNN for video classification on the [Sports-1M](https://cs.stanford.edu/people/karpathy/deepvideo/) dataset based on the architecture given in [1]. The model uses two separate streams – ‘fovea’ and ‘context’ that are responsible for learning features from different scaled-down resolutions, and are concatenated later. This helps in avoiding losing important information while speeding up the training process.

*Model architecture from [1]*

<img src="https://user-images.githubusercontent.com/51696913/169607219-2fadc2ac-b8e7-4259-b06a-4cdf7854a39f.png" width="400">

- Images are resized to 200x200
- 170x170 crops are randomly sampled
- Horizontal flipping = 0.5
- Each pixel is mean subtracted
- Optimization - mini-batches = 32, momentum = 0.9, weight decay = 0.0005, learning rate = 0.001
- Local Response Normalization layers are replaced by Batch Normalization layers

The sports video dataset can be downloaded from [this](https://drive.google.com/file/d/1iVIpq_na_EXvX1gpC6Ys3diCPrjR470b/view?usp=sharing) link

Achieved the highest validation accuracy of 65 % using this implementation which is comparable to the results obtained in [1]

The sample video outputs can be seen [here](https://drive.google.com/file/d/1n2KZ_OYeLOjsug2Xxu1PU89S4t61TeWJ/view?usp=sharing)

### Reference
[1] A. Karpathy, G. Toderici, S. Shetty, T. Leung, R. Sukthankar and L. Fei-Fei, "Large-Scale Video Classification with Convolutional Neural Networks," 2014 IEEE Conference on Computer Vision and Pattern Recognition, Columbus, OH, USA, 2014, pp. 1725-1732, doi: 10.1109/CVPR.2014.223.
[Link](https://ieeexplore.ieee.org/document/6909619)
