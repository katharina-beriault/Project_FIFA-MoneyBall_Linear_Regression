# Project FIFA MoneyBall

## Objective

The objective of this project is to build a linear regression model which can predict the _market value_ of a FIFA 21 player. I want to find out which indicators are most important to predict the market value of a player.

After data cleaning and before modeling, I will perform analysis on the dataset based on different questions (see section 'Questions and visualization'). 


## Data set

I am using the **FIFA 21 COMPLETE PLAYER DATASET** dataset from Kaggle: [**fifa21_male2.csv**](https://www.kaggle.com/ekrembayar/fifa-21-complete-player-dataset?select=fifa21_male2.csv)

This dataset contains 107 columns with 17125 rows. Each row shows the information for one FIFA 21 player. There is information on different topics:

- general information

   |   |   |
    |---|---|
    |  Player Name | Club of the Player   |
    | Nationaliy  | Height  |
    | Weight  |  Contract |
    |  Foot | Best Position  |
    |||
    
- monetary values

  |   |   |
    |---|---|
    |  **Market value** | Wage   | Release clause |
    |||

- player statistics

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

I performed analysis on four different topics:

- comparison value/wage/release clause for the different field positions
- comparison of wage for left/right foot (general VS split for different positions)
- relationship of age and wage
- comparison of club and market value



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


## Libraries

[import pandas as pd](https://pandas.pydata.org/)
[import numpy as np](https://numpy.org/doc/)
[import matplotlib.pyplot as plt](https://matplotlib.org/3.1.1/contents.html)
[import seaborn as sns](https://seaborn.pydata.org/)


