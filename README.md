# P1_MoneyBall_FIFA


## Objective and hypothesis

### Objective
Learn how to clean the data, apply the statistical techniques and visulization to answer the three objectives defined below. 
In addition, apply machine learning techniques to find the best model for predicting the market value of the players.

Objectives:

1) Which position in football has the highest market value?
2) Which age group has the highest market value?
3) What is the correlation between the player's overall rate and their composure(mental strength under pressure)?

#### Hypothesis
1) The vairous position in football will lead to different market values (e.g. value differences in goal keeper and striker).
2) The age group between 25 - 30 of the players are in the best market value position from their potential of growth.
3) Composure is an important elements as a sports player and the higher the composure is 
a) the overall rate is lead high.
b) high composure players are placed in offence positions (goal_keeping. striker)


## Data Source
Data was obtained from Kaggle - fifa-21-complete-player-dataset (link: https://www.kaggle.com/ekrembayar/fifa-21-complete-player-dataset).
The dataset represents player's name, age, position, belonging club, overall rating, market values, and detailed columns with individual scores for their skills (e.g. ball skills, passing, defencing, shooting, goal keeping, mentality, and more). The dataset consists of 17125 rows and 107 columns.

After the data cleaning process (removing redundant datas and handling null values),
the dataset rows and columns decrease to 17092 rows and 84 columns.

## Data processing
Below is the summary of how the data was processed:

1. Import libraries

2. Import data

3. Data cleaning and wranggling:
    - Understand the content of the features
    - Deal with duplicates, NaN values
    - Deal with categorical and numerical features and convert if necesssary
    
4. Data exploration and visualization:
    - Create a copy of dataframe and vizualized to analyzed the objectives (see above).
    
5. Fit into a model to predict market value of the players:
    - Apply boxcox transformation to bring the data closer to normal distribution
    - Define the outliers and remove them
    - Onehot encoding (change the categorical to numerical columns)
    - X, Y Train and Test slip
    - Create linear regression model and apply
    
6. Analyzing results

## Objective results
1) Which position in football has the highest market value?
   - After removing the outliers we see that the top 5 positions with highest market values are 
     RW, CM, RWB, CF, CDM
   
2) Which age group has the highest market value?
   - The age group between 26 to 30 years old can be assumed that has the most highest market values.        - The high correlation betwee Age and the market value ('value_k') was not found.
     
3) What is the correlation between the player's overall rate and their composure(mental strength under pressure)?
   - A relatively high correlation between composure and overall_rating.
   - A high correlation to player's the performance score (e.g. 'attacking', 'short_passing') 



## Libraries
Below are the list of libraries applied to the project:
- import pandas as pd
- import numpy as np
- import matplotlib.pyplot as plt
- import seaborn as sns
- import scipy.stats as stats
- import os
- from sklearn.preprocessing import StandardScaler
- from sklearn.model_selection import train_test_split
- from sklearn.linear_model import LinearRegression
- from sklearn.metrics import r2_score, mean_squared_error, mean_absolute_error




