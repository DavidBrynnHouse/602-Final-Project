# 602-Final-Project

The data for this project was retrieved from: https://opendata.dc.gov/datasets/crashes-in-dc/explore

# Introduction
The data that I am using for my final project was taken from the open data D.C web page. The data was taken from crashes in the district and recorded the time location, those involved, injuries and fatalities. The goal of my project is to create a classifier which can determine if a crash is fatal for anyone involved. This could be useful in finding locations that are particularly dangerous and re-working road signs or traffic patterns to make them safer.

# Data exploration and cleaning
Many of the features of my data set were id's police codes or duplicate values so I had to throw many of them away. I found that the data set was very complete with very few nan's. There was one feature which was categorical so I used one hot encoding to make it useful. Since most crashes do not result in a fatality I used under sampling to create a blanced dataset.

# Modeling
The first technique I tried was to create a deep learning model with keras. Unfortunatly this did not yield a high accuracy and the losses failed to converge on the training and validation sets. I then tested several ML models including random forests, svc, and logistic regression. I determined the best hyperparameters using grid search and found the accuracy from random forests to be the highest.

# Results

```
              precision    recall  f1-score   support

           0       0.60      0.73      0.66        78
           1       0.69      0.55      0.61        85
    accuracy                           0.64       163
   macro avg       0.65      0.64      0.64       163
weighted avg       0.65      0.64      0.64       163
```

The most important conclusion we can draw from our analysis is that the location of the crash plays the largest role in whether an accident will be fatal or not. This is striking because location is more imprtant even than whether or not the driver was impaired.

# Next Steps

Because we can see that the most relevant features to whether or not some one died in an accident was where that accident took place the first thing I would do is try to find out where the fatal accidents are taking place. Then a survey can be done to try and determine why these areas are so lethal.




