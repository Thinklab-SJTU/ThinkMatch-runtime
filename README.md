# ThinkMatch-runtime

This repository is designed to automatically build docker runtime leveraging the Github Action feature.

We build both ``torch1.6.0-cuda10.1``, ``torch1.7.1-cuda11.0``, ``torch-1.10.0-cuda11.3`` to fit different requirements of most GPU devices. Please check the supported CUDA versions of your GPU device and the GPU driver. If you find your devices cannot fit, please raise an issue and provide details about your testbed, and your required CUDA versions, etc. 


## Get the image by docker

For ``torch1.6.0-cuda10.1``:

```
docker pull ghcr.io/thinklab-sjtu/thinkmatch:torch1.6.0-cuda10.1-cudnn7-pyg1.6.3-pygmtools0.2.0 # The recommended image, suit GTX10 and RTX20 GPUs
```

For ``torch1.7.1-cuda11.0``:

```
docker pull ghcr.io/thinklab-sjtu/thinkmatch:torch1.7.1-cuda11.0-cudnn8-pyg1.6.3-pygmtools0.2.0
```

For ``torch-1.10.0-cuda11.3``:

```
docker pull ghcr.io/thinklab-sjtu/thinkmatch:torch1.10.0-cuda11.3-cudnn8-pyg2.0.3-pygmtools0.2.0 # Recommended for RTX30 GPUs
```

## Get the image by Singularity:

If your HPC does not support docker due to privilege issues, our images also work for singularity:

For ``torch1.6.0-cuda10.1``:

```
singularity build --fakeroot name_of_your_runtime.sif docker://ghcr.io/thinklab-sjtu/thinkmatch:torch1.6.0-cuda10.1-cudnn7-pyg1.6.3-pygmtools0.2.0 # The recommended image, suit GTX10 and RTX20 GPUs
```

For ``torch1.7.1-cuda11.0``:

```
singularity build --fakeroot name_of_your_runtime.sif docker://ghcr.io/thinklab-sjtu/thinkmatch:torch1.7.1-cuda11.0-cudnn8-pyg1.6.3-pygmtools0.2.0
```

For ``torch-1.10.0-cuda11.3``:

```
singularity build --fakeroot name_of_your_runtime.sif docker://ghcr.io/thinklab-sjtu/thinkmatch:torch1.10.0-cuda11.3-cudnn8-pyg2.0.3-pygmtools0.2.0 # Recommended for RTX30 GPUs
```
