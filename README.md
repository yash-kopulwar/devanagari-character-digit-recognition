# devanagari-character-digit-recognition
Character recognition of Hindi handwritten single characters and digits using CNN.

## Contents
* [Overview](#overview)
* [Motivation](#motivation)
* [Dataset](#dataset)
* [Setup](#setup)
* [Repository files](#repository-files)
* [Model](#model)
* [What did I learn](#what-did-i-learn)

## Overview
A simple image recognition model to recognize Hindi handwritten character and digits from an image of size (32, 32).

<p align="center">
  <img src="https://www.researchgate.net/profile/Kiran-Ravulakollu/publication/261876337/figure/fig1/AS:340899369373704@1458288151610/Samples-of-CPAR-2012-numeral-datasets.png" width="400">
</p>

## Motivation
The image classification problem with MNIST image dataset is considered a very standard problem to learn and practice how to develop, evaluate and use the deep neural networks. So, after completing that project, I worked on classifying devanagari characters using convolutional layers to understand the effects of changing the hyperparameters on the accuracy and the performance of a CNN model.

## Dataset
The dataset was downloaded from Kaggle<br>
Website: [devanagari-character-set](https://www.kaggle.com/rishianand/devanagari-character-set)

## Setup
Windows 10<br>
python 3.7<br>
tensorflow-gpu==2.1.0

## Repository files
devanagari_character_digit_recognition.ipny - jupyter notebook<br>
devanagari_character_digit_recognition_model.h5 - saved model after 30 epochs<br>
model_layers.png - layers used in my model

## Model
<p align="center">
  <img src="model_layers.png" width="400">
</p>

## What did I learn?
#### Problem: Loss function was decreasing but oscillating
Solution:<br>
Reducing the learning rate, use momentum on SGD (or better, use momentum based optimizers like Adam)
#### Problem: Difference in final values of valdaition and training accuracy
Solution:<br>
Underfitting - val and train accuracy low<br>
Overfitting - high train accuracy, low val accuracy<br>
Good fit - val accuracy close to train accuracy and both are high<br>
Unknown fit - high val accuracy, low train accuracy<br>

My model was facing overfitting, so I increased the batch size and added dropout layers.
