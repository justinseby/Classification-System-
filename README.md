# Multi-label Classification model for a Hotel booking app
This model helped the client in identifying whether the review was positive or negative and also for which category the review was given.


## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Code Examples](#codeexamples)
* [Contact](#contact)

## General info
This project is a flight ticket booking system in which users can book or cancel tickets. They can view fligt and airline details and choose from the collection and also they are able to update their account information. The admin will be able to add, delete and update various components of the services. A combination of Text mining and supervised classification algorithm was used in a pipeline method.

## Description: Multi-label Classification model for a Hotel booking app.
### Goal:
To classify the reviews as Positive or Negative and further identifying them as reviews on 4
important categories (Room, Staff and Service, Amenities, Food).

### Synopsis:
+ This model helped the client in identifying whether the review was positive or negative and also for
which category the review was given. For example if it was a positive review, the model would
identify whether it is on food, staff and service, amenities or room.
+ A combination of Text mining and supervised classification algorithm was used in a pipeline
method.
+ NuSVC was the highest performing algorithm after “K-fold” cross validation for binary classification.
+ Conv 1D was the highest performing algorithm for multi label classification.
+ “F1 micro” score, along with “Hamming loss” was considered as the evaluation metrics.


## Technologies
Tools/Technique: Python, Feature Engineering, Text mining, t-SNE,LSTM, Conv 1D


## Code Examples

rom keras.preprocessing.sequence import pad_sequences
encoded_docs_train = vect.texts_to_sequences(train['preprocess'])
max_length = vocab_size
padded_docs_train = pad_sequences(encoded_docs_train, maxlen=1200, padding='post')
print(padded_docs_train)
[[ 144    1  862 ...    0    0    0]
 [ 211 3117    3 ...    0    0    0]
 [  10    2    4 ...    0    0    0]
 ...
 [  19  240   46 ...    0    0    0]
 [  27   23   51 ...    0    0    0]
 [5817 5818  140 ...    0    0    0]]
In [ ]:
encoded_docs_test = vect.texts_to_sequences(test['preprocess'])
max_length = vocab_size
padded_docs_test = pad_sequences(encoded_docs_test, maxlen=1200, padding='post')
In [ ]:
from keras.layers import Dense, Flatten, LSTM, Conv1D, Conv2D, MaxPooling1D, Dropout, Activation,GlobalMaxPool1D
from keras.preprocessing.text import Tokenizer
from keras.preprocessing.sequence import pad_sequences
from keras.models import Sequential
from keras.optimizers import Adam
from time import time
from keras.callbacks import TensorBoard
from keras.layers import Dense, Activation, Embedding, Flatten, GlobalMaxPool1D, Dropout, Conv1D
from keras.callbacks import ReduceLROnPlateau, EarlyStopping, ModelCheckpoint
from keras.losses import binary_crossentropy
from keras.optimizers import Adam

from keras.layers.embeddings import Embedding
from keras.callbacks import ReduceLROnPlateau
  

## Contact
created by [@justinseby] - feel free to contact me
