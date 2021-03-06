# Inception Keras

#### Image Recognition using Keras and Inception-v3

Keras allows ['easy and fast'](https://keras.io) use of models: [example](https://keras.io/applications/#usage-examples-for-image-classification-models).  
[Inception-v3](https://www.tensorflow.org/tutorials/image_recognition) is a trained image recognition model for tensorflow.  

![Inception arch](https://github.com/EN10/inception-keras/raw/master/images/Inception-v3.png)

It was trained on 1.2 million images from [ImageNet](http://image-net.org/challenges/LSVRC/2012/index#introduction) to detect [1000 classes](http://image-net.org/challenges/LSVRC/2012/browse-synsets) (or labels for the images).  

![ImageNet](https://github.com/EN10/inception-keras/raw/master/images/ImageNet.png)

It took [8 NVIDIA Tesla K40s, 2 weeks](https://research.googleblog.com/2016/03/train-your-own-image-classifier-with.html) to train.

![K40](https://github.com/EN10/inception-keras/raw/master/images/K40.jpg)

This example was built and tested on c9.io or cs50.io as they provide a free Ubuntu VM (docker container) with 512MB RAM and 2GB Disk.

## Install

    sudo pip install -U pip 
    sudo pip install tensorflow 
    sudo pip install h5py pillow 

`sudo pip install -U pip` update pip with tensorflow  
`... h5py` to load weights  
`... pillow` to load image  
as `from tensorflow ... keras ... import` is used, `keras` is not installed separately  

disable "cpu_feature_guard":  
`export TF_CPP_MIN_LOG_LEVEL=2`

### Tensorflow Imports
[image](https://github.com/tensorflow/tensorflow/blob/master/tensorflow/contrib/keras/python/keras/preprocessing/image.py)  
[inception_v3](https://github.com/tensorflow/tensorflow/blob/master/tensorflow/contrib/keras/python/keras/applications/inception_v3.py)