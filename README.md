# HT-INV-NN

Author: Quan G

## About this notebook

This notebook combines dimensionality reduction techniques with a predictive deep learning (DL) model to estimate high-dimensional Gaussian and non-Gaussian channel fields. The HT-INV-NN model consists of a predictor that directly learns the inverse process from hydraulic head measurements to latent variables of random fields, and a decoder that generates high-dimensional parameter fields from predicted latent variables.

Please note this work:
* Assumes the reader is comfortable with Python, especially, jupyter notebook and tensorflow.
* Google Colab is recommended as the programming platform.

## Data
Data used for training DL models in paper experiments is stored at 
[Google Drive (under 'Data' directory)](https://drive.google.com/drive/folders/1UHO5VSUCmDCAoPgBvuqNUF2s8HM5ofG0?usp=share_link).

* dis/continuous_channel_reals: non-Gaussian channel realizations used to train DC-GAN
* Experiment 1: Gaussian_steady_state_512.mat 
* Experiment 2: Exponential_transient_256.mat
* Experiment 3: Gaussian_steady_state_3D.mat
* Experiment 4: Channel_Binary_steady_state_128.mat
* Experiment 5: Channel_Continuous_steady_state_128.mat 

## Train GAN model as Decoder
- **DC_GAN_train_for_Channel.ipynb**
    - set **fname = 'continuous' or 'discontinuous'** for corresponding realizations (at Load Data Section, 2nd code block, Line 4)

## Train Predictor model
- Experiment 1 & 2: Estimate 2D Gaussian field with PCA decoder
    - Use **2D_Gaussian_field.ipynb**
    - Set **experiment = 1 or 2** (at Load Data Section, 2nd code block, Line 9)

- Experiment 3: Estimate 3D Gaussian field with PCA decoder 
    - Use **3D_Gaussian_field.ipynb**

- Experiment 4 & 5: Estimate 2D non-Gaussian field with GAN decoder 
    - Use **2D_Channel_field.ipynb**
    - set **experiment = 4 or 5** (at Load Data Section, 2nd code block, Line 9)


## Citations
```
@article{GUO2023128828,
      title = {Predictive deep learning for high-dimensional inverse modeling of hydraulic tomography in Gaussian and non-Gaussian fields},
      doi = {DOI: 10.5281/zenodo.7992543},
      journal = {under review},
}
```
[comment]: <> (      volume = {616},
      pages = {128828},
      year = {2023},
      issn = {0022-1694},
      doi = {https://doi.org/10.1016/j.jhydrol.2022.128828},
      url = {https://www.sciencedirect.com/science/article/pii/S0022169422013981},
      author = {Quan Guo and Yue Zhao and Chunhui Lu and Jian Luo})

