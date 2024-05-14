# PoP Projekt 14 - Electron Tomography Denoising Demo

This repository contains a demonstration notebook of four different methods used to denoise electron tomography images, three filter based methods and one machine-learning based method.

## Filter-based denoising

### Median Filter

The median filter removes intensity outliers in an image by replacing the value of every pixel with the median of the pixels in its sourrounding. This simple and computationally efficient method, while working well with pixel independant (unstructured) noise, introduces a not insignificant amount of blurring in high contrast areas.

### Anisotropic Diffusion

Anisotropic diffusion smooths out noise in an image while preserving important features like edges by varying the amount of diffusion based on the local gradients. It achieves this through an iterative process that selectively reduces noise more in uniform areas and less near edges. Like the median filter this algorithms effectivenes is limited when dealing with structured noise.

### Non-local Means

Non-local means filtering reduces noise by averaging each pixel in an image with other pixels that have similar intensity patterns, regardless of their location in the image. This method preserves details and textures better than local averaging because it uses information from the entire image. While this make this method adaptive to varying noise levels in a single image and able to preserve edges well, it also is computationally intensive when compared to other filter based methods.

<p align="center">
  <img src="./sources/pop_denoise_demo_filter_comp.jpg" width="500" title="Comparrison of filter based denoising results">
</p>


## Machine Learning based denoising

<p align="center">
  <img src="./sources/pop_denoise_demo_structN2V_comp.jpg" width="620" title="Comparrison of ML based denoising results">
</p>

# How to use this notebook

This notebook is intended to be run in Google Colab but can also be used locally.

To open this notebook in Colab just click on <a href="https://colab.research.google.com/github/lucasfortune/PoP_Denoise_demo/blob/main/PoP_Denoise_demo.ipynb">this</a> link. 


If you prefer to run the notebook locally all necessary dependencies must be installed. It is recommended to install everything in a anaconda virtual environment. After installing <a href="https://docs.anaconda.com/free/anaconda/install/index.html">anaconda</a> run the folowwing commands:

```bash
conda create -n denoise_demo python=3.9
conda activate denoise_demo
conda install matplotlib tifffile scikit-image pandas
```

If you are planning on also running the Noise2Void Demo it is necessary to install n2v and Tensorflow. Please follow the installation instructions <a href="https://pypi.org/project/n2v/"> here </a>.



[def]: /Users/lucasfortune/Documents/arbeit/phd/code/denoise_demo/PoP_Denoise_demo/sources/pop_denoise_demo_filter_comp.jpg