# ThinkMatch-runtime

This repository is designed to automatically build docker runtime leveraging the Github Action feature.

We build both ``torch1.6.0-cuda10.1``, ``torch1.7.1-cuda11.0``, ``torch-1.10.0-cuda11.3`` to fit different requirements of most GPU devices. Please check the supported CUDA versions of your GPU device and the GPU driver. If you find your devices cannot fit, please raise an issue and provide details about your testbed, and your required CUDA versions, etc. 

Please see the available versions at [dockerhub](https://hub.docker.com/repository/registry-1.docker.io/runzhongwang/thinkmatch/general).


## Some Notes

* ``torch1.6.0-cuda10.1`` is the recommended image, suits GTX10 and RTX20 GPUs


* ``torch-1.10.0-cuda11.3`` is recommended for RTX30 GPUs
