![PyPI - Python Version](https://img.shields.io/badge/Python-3.7-brightgreen)
![PyPI - Python Version](https://img.shields.io/badge/requirements.txt-updated-yellow)
# Convolutional Neural Networks

## Purpose of Plan
Cats vs Dogs classification is a fundamental Deep Learning project for beginners. If you want to start your
Deep Learning Journey with Python Keras, you must work on this elementary project.

## Preview
![Project Preview](https://github.com/mopidevimu/Convolutional_Neural_Networks/blob/master/git_img/cat_dog.gif)
![Project Preview](https://github.com/mopidevimu/Convolutional_Neural_Networks/blob/master/git_img/cat-vs-dog.jpg)

## QickView

```python
from keras.preprocessing.image import ImageDataGenerator

train_datagen = ImageDataGenerator(rescale = 1./255,
                                   shear_range = 0.2,
                                   zoom_range = 0.2,
                                   horizontal_flip = True)

test_datagen = ImageDataGenerator(rescale = 1./255)

training_set = train_datagen.flow_from_directory('dataset/training_set',
                                                 target_size = (64, 64),
                                                 batch_size = 32,
                                                 class_mode = 'binary')

test_set = test_datagen.flow_from_directory('dataset/test_set',
                                            target_size = (64, 64),
                                            batch_size = 32,
                                            class_mode = 'binary')

classifier.fit_generator(training_set,
                         steps_per_epoch = 8000,
                         epochs = 25,
                         validation_data = test_set,
                         validation_steps = 2000)
```