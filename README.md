# About

## Abstract

This repository generates realistic human faces by using deep convolutional generative adversarial network (DCGAN). It takes **32 numbers** and generates a **128x128x3** size image. The code is completly in Python with tensorflow. The model is in training phase, very soon it will be uploaded.

## Detailed

This is a repository to generate realistic human faces of size 128x128x3. It uses deep convolutional general adversarial network (DCGAN). It has two models, generator and discriminator, the generator generates fake faces from latent of size 32 and discriminator classifies the generated image and actual image into real or fake images. They both are trained in adversarial manner, they both try to minimize their loss like two players game.

The proposed model is trained on CelebA dataset. It has 2,02,599 images of 10,177 unique identities. 

Here the discriminator is the convolutional neural network (CNN) with 5 convolutional layers and one dense layer. The convolutional part of generator is divied into 5 blocks, each block contains convolutional layer and leaky relu activation in a sequence. The generator has 4 Con2dTranspose layer and 3 convolutional layer. The Conv2dTranspose layer performs upsampling and convolutional together. The generator generates image from latent size of 32.

The generator takes 32 numbers as input and reshape it to 16x16x128 tensor. Then it perfomes upsampling and covolution to generate 128x128x3 image. This generated image and actual image are passed to discrimiator. The labels for real and fake images are 0 and 1 respectively with some added noise. The discriminator identifies real and fake images. If discriminator makes mistake, it is penalised and if it makes correct prediction the generator is penalised. Hence both generator tries to fool the discriminator and discriminator tries to maximize its accuracy.

This repository contains 3 files. The `implementation.ipynb` is the implementation code of the model, the `requirments.txt` is the txt file containing requirments to run the model and the `instructions.txt` contains instructions to better understand this repository.

# Highlights

The generator

<img width="493" alt="Screenshot 2023-04-05 at 10 42 32 AM" src="https://user-images.githubusercontent.com/76246981/230336242-18ba08ac-1b56-4493-8813-3e024e1e5149.png">

The discriminator

<img width="483" alt="Screenshot 2023-04-05 at 10 42 50 AM" src="https://user-images.githubusercontent.com/76246981/230336384-78a25fda-4a68-4dfe-80f4-60e96a8763bd.png">

The GAN

<img width="487" alt="Screenshot 2023-04-05 at 10 43 12 AM" src="https://user-images.githubusercontent.com/76246981/230336445-64ef24ca-915e-499c-aec1-4908e3896cbc.png">

# Prerequisites

`Python>=3.6`

# Getting started

1. Download the repository and unzip it.
2. Install necessary packages using `pip install -r requirements.txt`.
3. Download the <a href="https://www.kaggle.com/datasets/jessicali9530/celeba-dataset">Celeba dataset</a> to train the model.
3. Read the `instructions.txt` for better understanding of repository.

# Future work

In future, i'm looking forward to generate more realistic human faces and upload it.

# Connect with me

Give your feedback at : karanhadiyal65@gmail.com
