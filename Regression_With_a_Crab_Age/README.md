# 🦀 Regression With a Crab Age 
## (IN PROGRESS)

## :pushpin: Overview
This [notebook](notebook.ipynb) showcases the steps that I have done while participating *(the solution is not submitted yet)* in the [Kaggle Playground Series, S3E16](https://www.kaggle.com/competitions/playground-series-s3e16).

## :eyes: The Goal
The task is to use regression to predict the age of crabs given physical attributes. 

## :books: Data
The [data](data/train.csv) contains next attributes:
- `Sex`
- `Length`
- `Diameter`
- `Height`
- `Weight`
- `Shucked Weight`
- `Viscera Weight`
- `Shell Weight`
- `Age`  

## :eyes: Results
At the moment of this writing, I have not submitted the solution yet. However, I have reached the **MAE** *(Mean Absolute Error)* of $1.408$, while the best **MAE** in the [Leaderboard](https://www.kaggle.com/competitions/playground-series-s3e16/leaderboard?) is about $1.33$.  

I have tried different models, using `GridSearchCV` and `RandomizedSearchCV` to tune hyperparameters:
- `DecisionTreeRegressor`
- `Ridge`
- `GradientBoostingRegressor`
- `RandomForestRegressor` 

On top of those models, I've used `StackingRegressor`, however it has not improved the **MAE** much: it minimized it from about $1.41$ *(best individual model score)* to $1.40$.

As for the data transformations, I've done standard scaling and one-hot encoding. I have skipped **feature engineering**, but I guess it may help, e.g. calculating **body mass index** or some other (?).

**UPDATES ARE IN PROGRESS**...I encourage you to explore the current version of the [notebook](notebook.ipynb) in case you are interested in what I have and have not done ☺️.

## :hammer_and_wrench: Libraries Used
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `sklearn`

## :raising_hand_man: Author
Volodymyr Karpenko  
[LinkedIn](https://www.linkedin.com/in/volod-karpenko/) • <a href=mailto:volod1701@gmail.com>Email </a>(volod1701@gmail.com)
