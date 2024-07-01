# Computional Imaging Project 

This project ValidateS the use of self-supervised learning to accelerate MRI data reconstruction.

## Processed fastMRI dataset

In this project we used fastMRI axial T2 brain datasets. 
For the network training and testing, you can download the processed datasets from the following link.

**Download Link** : https://drive.google.com/file/d/18hGurziu8zMoyyN3MvhiljvfHZCaaOaz/view?usp=drive_link

##  Results and Contributes
![alt text](png/Result.png)

1.Self-supervised learning performances better image reconstruction quality at lower undersample folder.

2.SSDU can achieve better reconstruction perforamce with the increase of the number of trainable parameters, but the overfiting should also be considered.

3.For SSDU, Gaussian undersampled selection performances better image reconstruction quality than Uniform undersampled selection.

## Network structure

SSDU: Self-supervised learning of physics-guided reconstruction neural networks without fully sampled reference data

Official code: https://github.com/byaman14/SSDU

![alt text](png/Self_Suoervised_learning.PNG)

## Reference papers

SSDU: Self-supervised learning of physics-guided reconstruction neural networks without fully sampled reference data by Yaman, B., Hosseini, S. A. H., Moeller, S., Ellermann, J., Uğurbil, K., & Akçakaya, M on Magnetic Resonance in Medicine, 2020

Link: https://arxiv.org/abs/1912.07669

## Configuration file

The configuration files are in `config` folder. Every setting is the same as the paper.

Configuration files for K=1 and K=10 are provided. The authors trained the K=1 model first, and then trained the K=10 models using the weights of K=1 model.

## Train

You can change the configuration file for training by modifying the `train.sh` file.

```
scripts/train.sh
```

## Test

You can change the configuration file for testing by modifying the `test.sh` file.

```
scripts/test.sh
```

## Saved model

Saved model are provided.
For example:
`workspace/base_modl,k=2/checkpoints/final.epoch0039-score19.9291.pth` 

