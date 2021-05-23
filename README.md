# devanagari-digit-classification

## Contents
* [Overview](#overview)
* [Motivation](#motivation)
* [Dataset](#dataset)

## Overview
A simple image classification model to recognize Hindi handwritten digits and alphabets

<p align="center">
  <img src="https://www.researchgate.net/profile/Kiran-Ravulakollu/publication/261876337/figure/fig1/AS:340899369373704@1458288151610/Samples-of-CPAR-2012-numeral-datasets.png" width="400">
</p>

## Motivation

## Dataset
Installing CPAR

    $ pip install cpar

Importing the datset

    from cpar.char import load_data
    train_x, test_y, train_y, test_y = load_data()
    
