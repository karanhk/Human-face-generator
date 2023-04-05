# About

## Abstract

This repository generates realistic human faces by using deep convolutional general adversarial network (DCGAN). It takes **32 numbers** and generates a **128x128x3** size image. It creates spectrogram from audio file by using `librosa` library and classifies that spectrogram by using CNN.

## Detailed

This is a repository to generate realistic human faces of size 128x128x3. It uses deep convolutional general adversarial network (DCGAN). It has two models, generator and discriminator, the generator generates fake faces from latent of size 32 and discriminator classifies the generated image and actual image into real or fake images. They both are trained together, they both try to minimize their loss like two players game.
The proposed model is trained on CelebA dataset.

The discriminator is the convolutional neural network (CNN) with 5 convolutional layers and one dense layer. The convolutional part of generator is divied into 5 blocks, each block contains convolutional layer and leaky relu activation in a sequence. The generator has 4 Con2dTranspose layer and 3 convolutional layer. The Conv2dTranspose layer performs upsampling and convolutional together. The generator generates image from latent size of 32.

The generator takes 32 numbers as input and reshape it to 16x16x128 tensor. Then it perfomes upsampling and covolution to generate 128x128x3 image. This generated image and actual image are passed to discrimiator. The labels for real and fake images are 0 and 1 respectively with some added noise. The discriminator identifies real and fake images. If discriminator makes mistake, it is penalised and if it makes correct prediction the generator is penalised. Hence both generator tries to fool the discriminator and discriminator tries to maximize its accuracy.

This repository contains 3 files. The `implementation.ipynb` is the implementation code of the model, the `requirments.txt` is the txt file containing requirments to run the model and the `instructions.txt` contains instructions to better understand this repository.

# Highlights

The generator
<img align="center" src="https://drive.google.com/file/d/1bNUVuSwKVnGePwTHIo8emPMrB46zgqeW/view?usp=sharing", alt="GAN"/>

The discriminator
<img align="center" src="https://drive.google.com/file/d/1bNUVuSwKVnGePwTHIo8emPMrB46zgqeW/view?usp=sharing", alt="GAN"/>

The GAN
<img align="center" src="https://drive.google.com/file/d/1bNUVuSwKVnGePwTHIo8emPMrB46zgqeW/view?usp=sharing", alt="GAN"/>

# Prerequisites

`Python>=3.6`

# Getting started

1. Download the repository and unzip it.
2. Install necessary packages using `pip install -r requirements.txt`.
3. Read the `instructions.txt` for better understanding of repository.

# Future work

In future, i'm looking forward to generate more realistic human faces and upload it.

# Connect with me

Give your feedback at : karanhadiyal65@gmail.com
