# Caffe

[![Build Status](https://travis-ci.org/BVLC/caffe.svg?branch=master)](https://travis-ci.org/BVLC/caffe)
[![License](https://img.shields.io/badge/license-BSD-blue.svg)](LICENSE)

Caffe is a deep learning framework made with expression, speed, and modularity in mind.
It is developed by the Berkeley Vision and Learning Center ([BVLC](http://bvlc.eecs.berkeley.edu)) and community contributors.


## Installation
### dependence 
opencv 2.4.13 built with cuda 8.0 support 
most of the machines can bypass following steps to reinstall opencv
1. download opencv-2.4.13 source code
2. `cd opencv-2.4.13 &&  mkdir release && cd release`
3. `cmake -D CMAKE_BUILD_TYPE=RELEASE -D CUDA_TOOLKIT_ROOT_DIR="/usr/local/cuda-8.0" -D CMAKE_INSTALL_PREFIX=/usr/local/opencv-2.4.13 ..`
4. `make -j6`
5. `make install`

### caffe 
1. clone this repo 
2. `cd caffe && mkdir build && cd build`
3. `cmake -D CMAKE_PREFIX_PATH="/usr/local/opencv-2.4.13;/usr/local/cudnn-v5" -D CUDA_TOOLKIT_ROOT_DIR="/usr/local/cuda-8.0"  -D BLAS=open ..`
4. `make -j6`

### pycaffe
add 
`export PYTHONPATH=$PYTHONPATH:/usr/local/opencv-2.4.13/lib/python2.7/site-packages`
`export PYTHONPATH=$PYTHONPATH:$HOME/caffe/python`
to  .bashrc or .zshrc



Check out the [project site](http://caffe.berkeleyvision.org) for all the details like

- [DIY Deep Learning for Vision with Caffe](https://docs.google.com/presentation/d/1UeKXVgRvvxg9OUdh_UiC5G71UMscNPlvArsWER41PsU/edit#slide=id.p)
- [Tutorial Documentation](http://caffe.berkeleyvision.org/tutorial/)
- [BVLC reference models](http://caffe.berkeleyvision.org/model_zoo.html) and the [community model zoo](https://github.com/BVLC/caffe/wiki/Model-Zoo)
- [Installation instructions](http://caffe.berkeleyvision.org/installation.html)

and step-by-step examples.

[![Join the chat at https://gitter.im/BVLC/caffe](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/BVLC/caffe?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Please join the [caffe-users group](https://groups.google.com/forum/#!forum/caffe-users) or [gitter chat](https://gitter.im/BVLC/caffe) to ask questions and talk about methods and models.
Framework development discussions and thorough bug reports are collected on [Issues](https://github.com/BVLC/caffe/issues).

Happy brewing!

## License and Citation

Caffe is released under the [BSD 2-Clause license](https://github.com/BVLC/caffe/blob/master/LICENSE).
The BVLC reference models are released for unrestricted use.

Please cite Caffe in your publications if it helps your research:

    @article{jia2014caffe,
      Author = {Jia, Yangqing and Shelhamer, Evan and Donahue, Jeff and Karayev, Sergey and Long, Jonathan and Girshick, Ross and Guadarrama, Sergio and Darrell, Trevor},
      Journal = {arXiv preprint arXiv:1408.5093},
      Title = {Caffe: Convolutional Architecture for Fast Feature Embedding},
      Year = {2014}
    }
