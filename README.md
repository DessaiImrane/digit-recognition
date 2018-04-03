## Digit Recognition using Keras/TensorFlow and OpenCV in Python


### Requirements

I tested the code on python 3.6.5 x86_64

```
pip install opencv-python
pip install tensorflow 
pip install matplotlib
pip install keras
pip install h5py
pip install imutils
```

### Description

I wanted to use my knowledge on DeepLearning to make a real-world project. It was fun and i've learned many things.

<img src="https://github.com/DessaiImrane/digit-recognition/blob/master/Digit-Recognition-Thumb.gif">

For long version, [see]()


### Python  Implementation

1) Dataset- MNIST dataset
2) Images of size 28 X 28
3) Classify digits from 0 to 9
4) CNN

### Train Acuracy 99,45%
### Test Acuracy 99,32%

### Execution for showing images through webcam
To run the code, 
```
python cam.py
```

### Execution to see trained CNN on some samples

To run the code,

```
python test-keras-training-reload.py
```



### Execution to train CNN

To run the code,

```
python keras-training.py
```

This took 1 hour on my laptop.

Model Sumary
```
Using TensorFlow backend.
_________________________________________________________________
Layer (type)                 Output Shape              Param #
=================================================================
conv2d_1 (Conv2D)            (None, 26, 26, 32)        320
_________________________________________________________________
conv2d_2 (Conv2D)            (None, 24, 24, 64)        18496
_________________________________________________________________
max_pooling2d_1 (MaxPooling2 (None, 12, 12, 64)        0
_________________________________________________________________
dropout_1 (Dropout)          (None, 12, 12, 64)        0
_________________________________________________________________
flatten_1 (Flatten)          (None, 9216)              0
_________________________________________________________________
dense_1 (Dense)              (None, 128)               1179776
_________________________________________________________________
dropout_2 (Dropout)          (None, 128)               0
_________________________________________________________________
dense_2 (Dense)              (None, 10)                1290
=================================================================
Total params: 1,199,882
Trainable params: 1,199,882
Non-trainable params: 0
_________________________________________________________________
```

Model Fit
```
Train on 60000 samples, validate on 10000 samples
Epoch 1/15
 - 263s - loss: 0.1884 - acc: 0.9441 - val_loss: 0.0451 - val_acc: 0.9854
Epoch 2/15
 - 262s - loss: 0.0790 - acc: 0.9769 - val_loss: 0.0360 - val_acc: 0.9884
Epoch 3/15
 - 262s - loss: 0.0635 - acc: 0.9810 - val_loss: 0.0334 - val_acc: 0.9891
Epoch 4/15
 - 269s - loss: 0.0484 - acc: 0.9854 - val_loss: 0.0285 - val_acc: 0.9905
Epoch 5/15
 - 268s - loss: 0.0414 - acc: 0.9876 - val_loss: 0.0274 - val_acc: 0.9921
Epoch 6/15
 - 250s - loss: 0.0374 - acc: 0.9885 - val_loss: 0.0333 - val_acc: 0.9896
Epoch 7/15
 - 240s - loss: 0.0321 - acc: 0.9900 - val_loss: 0.0273 - val_acc: 0.9926
Epoch 8/15
 - 240s - loss: 0.0290 - acc: 0.9907 - val_loss: 0.0268 - val_acc: 0.9918
Epoch 9/15
 - 239s - loss: 0.0276 - acc: 0.9913 - val_loss: 0.0281 - val_acc: 0.9924
Epoch 10/15
 - 240s - loss: 0.0240 - acc: 0.9924 - val_loss: 0.0341 - val_acc: 0.9914
Epoch 11/15
 - 239s - loss: 0.0233 - acc: 0.9925 - val_loss: 0.0234 - val_acc: 0.9938
Epoch 12/15
 - 239s - loss: 0.0219 - acc: 0.9933 - val_loss: 0.0286 - val_acc: 0.9925
Epoch 13/15
 - 238s - loss: 0.0204 - acc: 0.9934 - val_loss: 0.0309 - val_acc: 0.9918
Epoch 14/15
 - 237s - loss: 0.0191 - acc: 0.9935 - val_loss: 0.0288 - val_acc: 0.9929
Epoch 15/15
 - 241s - loss: 0.0174 - acc: 0.9944 - val_loss: 0.0310 - val_acc: 0.9932
```

