# Description

A classical ML project for classifying digits from 0-9 based on a vector image with size 28x28. Dataset is the famous MNIST dataset.

# ML model

Different ML models shown in this notebook work a little different. In general, ML models accept `N*784` array with N elements (digits to predict); models outputs either an array `N*1` specifying which number it predicts (Sklearn), or `N*10`.

# Pipeline

- **Load data** for MNIST;
- **Pre-processing**: 
  - Convert `N*28*28` 3D array of N images to `N*784` 2D array of N images;
  - Normalize: / 256
  - (depending on the model) Process labels: from 5, 4, etc. to [0,0,0,1,0,0,0,0,0,0]
- **Train models**:
  - Sklearn models: SGDClassifier, Random Forest, NN
  - Keras (Tensorflow): NN
  - Accuracy assessed on train set by cross-validation method
- **Test models**:
  - On the test holdout set
  - On the custom local images

