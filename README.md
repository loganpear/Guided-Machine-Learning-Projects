# Rock vs Mine Prediction

This project is a guided project by Siddhardhan, sourced from [YouTube](https://youtu.be/fiz1ORTBGpY?si=TxoxWqYd7VVxM-BG).

## Overview

This project uses Logistic Regression to predict whether an object detected by sonar is a rock or a mine based on sonar data.

## Dependencies

- numpy
- pandas
- sklearn

## Dataset

The dataset used (`sonar_data_MLproj1.csv`) contains sonar data with features and labels ('R' for rock and 'M' for mine). Here's a brief overview of the dataset:

- Total instances: 208
- Features: 60
- Labels: 'R' (Rock), 'M' (Mine)

## Data Processing

The data is loaded into a pandas DataFrame and preprocessed for training and testing.

## Model Training

A Logistic Regression model is trained using the processed data.

## Evaluation

The model is evaluated for accuracy on both training and testing datasets.

- Training accuracy: 83.42%
- Testing accuracy: 76.19%

## Predictive System

A system is implemented to predict whether new sonar data represents a rock or a mine.

### Example Usage

```python
# Example input data
input_data = (0.0200, 0.0371, 0.0428, ...)

# Predicting
prediction = model.predict(np.asarray(input_data).reshape(1, -1))

# Output
if prediction[0] == 'R':
    print('The object is a Rock')
else:
    print('The object is a Mine')
