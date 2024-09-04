![Picture1](https://github.com/user-attachments/assets/fe14948d-b3c0-4f88-9b25-e7d94de24739)

## Introduction
The current research focuses on creating a Conditional Variational Autoencoder (CVAE) designed for encoding and reconstructing 5%-damped spectral acceleration. Unlike conventional approaches, this model integrates site-specificparameters related to the characteristics of the seismic source, propagation path, and site conditions, utilizing them as conditional inputs. The model is trained on an extensive dataset comprising 23,929 ground motion records from both horizontal and vertical directions, sourced from 325 shallow crustal events in the updated NGA-West2 database. The input parameters encompass moment magnitude, Joyner-Boore distance, focal mechanism, hypocentral depth, average shear-wave velocity up to 30 m depth. 

## Process for Validation
To validate the model's reliability, both inter-event and intra-event residual analyses are conducted, affirming its robustness and applicability. Furthermore, the model's performance is assessed through residual and SHAP analyses. Thus, this study contributes to advancing techniques in ground motion modelling, specifically enhancing seismic hazard assessment and the reconstruction of ground motion data.

## Library Used
* **Pandas**
* **Numpy**
* **Matplotlib**
* **Tensorflow**
* **Keras**

## Libraries Installation

```pip install numpy``` <br/>
```pip install matplotlib``` <br/>
```pip install tensorflow```<br/>
```pip install pandas``` <br/>
```pip install keras``` <br/>
```pip install sklearn```

## Importing the libraries
```import numpy as np```<br/>
```import matplotlib.pyplot as plt``` <br/>
```import pandas```<br/>
```import tensorflow as tf```<br/>
```import random```<br/>
```from sklearn.model_selection import train_test_split```<br/>
```from sklearn.preprocessing import MinMaxScaler,StandardScaler```<br/>
```from keras.layers import Input, Dense, Lambda```<br/>
```from keras.models import Model, load_model, Sequential```<br/>
```from keras import backend as K```<br/>
```from keras.losses import mse```<br/>
```from keras.optimizers import Adam```<br/>
```from keras.callbacks import ModelCheckpoint```<br/>
```from sklearn.model_selection import train_test_split```<br/>
```from sklearn.preprocessing import StandardScaler```<br/>

## Model Used
**CVAE** - A Conditional Variational Autoencoder (CVAE) is an extension of the Variational Autoencoder (VAE) that incorporates conditional information into the generative model. Unlike a standard VAE, which learns to encode and decode data without any additional context, a CVAE conditions the encoding and decoding processes on external information (e.g., labels or other features). This allows the model to generate outputs that are not only similar to the training data but also conform to specific conditions provided. CVAEs are particularly useful for tasks like controlled data generation, where specific attributes of the output need to be specified, such as generating images of a particular category or modifying specific features in data synthesis.

## Sections:
* Data Loading and Preprocessing.
* Test and Train set spiliting (0.2 and 0.8 respectively)
* Defing of the CVAE model with 4 dense layers
* Loss functions KL Divergence and Mean Squared.
* Training of CVAE model
* Generating encoded data
* Training ANN using the encoded data and the input parameters.
* Decoding the predicted data and ploting the same against original ones.
* Inter Intra and Site to Site residual analysis.
