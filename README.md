# Project FIFA MoneyBall

## Objective

The objective of this project is to build a linear regression model which can predict the *market value* of a FIFA 21 player. I want to find out which indicators are most important to predict the market value of a player.

After data cleaning and before modeling, I will perform analysis on the dataset based on different questions (see section 'Questions and visualization'). 


## Dataset

I am using the **FIFA 21 COMPLETE PLAYER DATASET** dataset from Kaggle: [**fifa21_male2.csv**](https://www.kaggle.com/ekrembayar/fifa-21-complete-player-dataset?select=fifa21_male2.csv)

This dataset contains 107 columns with 17125 rows. Each row shows the information for one FIFA 21 player. There is information on different topics:

- General information

   |   |   |
    |---|---|
    |  Player Name | Club of the Player   |
    | Nationaliy  | Height  |
    | Weight  |  Contract |
    |  Foot | Best Position  |
    |||
    
- Monetary values

  |   |   ||
    |---|---|---|
    |  **Market value** | Wage   | Release clause |
    ||||

- Player's statistics

   |   |   |
    |---|---|
    |  Overal Rating | Potential   |
    | Growth  | Attacking  |
    | Skill  |  Movement |
    |  Hits | Dribbling  |
    | Defending|Physical|
    |||

After data cleaning and dropping unnecessary columns for the model the dataframe contains 70 columns, the amount of rows remained the same.

## Data cleaning and wrangling

In this section I performed the following steps for data cleaning:

- Changing the column header names (lower letter and no spaces)
- Removing duplicate rows in dataframe
- Changing column types
    - Extracting only year from column 'joined'
    - Changing column types to numerical
    - Changing monetary columns (€)
- Dealing with NaN-values
    - Overview of present NaN-values
    - Overview of how to proceed with columns containing NaN-values
    - Replacing NaN-values
- Dropping unnecessary columns


## Questions and visualization

I performed an analysis on four different topics to gain more insight about the relationship of monetary values and specific indicators. The idea is to find out which factors make it most likely for a player to have a high wage, market value and release clause:

- Comparison value/wage/release clause for the different field positions
- Comparison of wage for left/right foot (general VS split for different positions)
- Relationship of age and wage
- Comparison of club and market value


## Linear regression model

To create a linear regression model the following steps were performed:

- Pre-processing data for the linear regression model
    - Correlation of numerical columns
    - Insights after first exploration
    - Boxcox transformation
    - Dealing with outliers
- Normalization of the data
- Dealing with categorical columns
- Comparison of data sets by checking R-score
    - Overview of different R2-scores
- Modeling and model validation
- Reporting

## Main results

|||
|:---:| :---:|
|R2-score| 0.930|
|||

## Libraries

[import pandas as pd](https://pandas.pydata.org/)<br>
[import numpy as np](https://numpy.org/doc/)<br>
[import matplotlib.pyplot as plt](https://matplotlib.org/3.1.1/contents.html)<br>
[import seaborn as sns](https://seaborn.pydata.org/)<br>
[import sklearn](https://scikit-learn.org/stable/index.html)<br>
[import statsmodels](https://www.statsmodels.org/stable/index.html)


