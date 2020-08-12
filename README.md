![PyPI - Python Version](https://img.shields.io/badge/Python-3.7-brightgreen)
![PyPI - Python Version](https://img.shields.io/badge/requirements.txt-updated-yellow)
# GeoStatEISTI
## Purpose of Plan
The Geographical statistics of engineering internships Plan will provide a definition of the project, including the
project’s goals and objectives. Additionally, the Plan will serve as an agreement between the following parties: Project
Sponsor, Steering Committee, Project Team, and other personnel associated with and/or affected by the project.

## Preview
![Project Preview](https://github.com/mopidevimu/GeoStatEisti/blob/master/ReadMe_pics/project.gif)

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