# PoP Projekt 14 - Elektrontommogram Denoising Demo

This repositroy contains a demonstration of four different methods used to denoise electron tommogram images, three filter based methods and one machine-learning based method.

## Filter-based denoising

![filter comp][def]
explanation filter

## Machine Learning based denoising

image n2v
explanation n2v

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