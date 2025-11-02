# :ship: Titanic: Data Analysis, Hypothesis Testing, and Predictions

## :pushpin: Overview
This [notebook](notebook.ipynb) showcases my skills in data analysis including hypothesis testing and building prediction models using the following python libraries: `pandas`, `matplotlib`, `seaborn`, `scikit-learn`, and `scipy.stats`.

## :eyes: What Is Analyzed?
The [Titanic data set](data/titanic.csv) encourages to discover the relation between the survival rate and passenger characteristics such as `Sex`,  `Class`, `Age`, etc. The data allows to test a bunch of hypothesis and verify what certain types of passengers were more likely to survive. I encourage you to explore [the notebook](notebook.ipynb) and find out the answers. 

## :bar_chart: Data Analysis Topics Covered
1. **Data Cleaning**
    - There were a lot of instances with blank `Age`. I replaced those values with the median `Age` regarding the `Passenger Class` and `Sex` of the specific instance.
2. **Data Exploration**
    - *"a picture is worth a thousand words"* - jump to [the notebook](notebook.ipynb) and verify yourself how helpful visualizations can be in understanding the data and suggesting the hypothesis to test.
    - I would also like to emphasize the influence of `outliers` on the data exploration process, but for further details refer the corresponding section in [the notebook](notebook.ipynb).
3. **Hypothesis Testing**
    - The tests listed below helped a lot in verifying the influence of different variables on the survival rate:
        - Two-Proportion z-Test
        - Chi-Square Test of Independence
        - Welch's t-Test
4. **Building Prediction Model**
    - Tree Models
    - *K*-Nearest Neighbors
    - Logistic Regression
    - Random Forest Classifiers
5. **Cross-Validation**
    - I used cross-validation to evaluate models' performance. I've used the following metrics instead of accuracy:
        - F1 Score
        - Precision
        - Recall
        - AUC Score
6. **Bootstrap Confidence Interval**
    - I built confidence intervals for models' prediction performance using bootstrap resampling on the test set.  

:syringe: However, the so-called *machine learning* part of this tutorial is not complete and it makes sense to go further as the performance can be improved using **ensemble models**, **stacking**, and **feature engineering**.

## :game_die: Who Survived?
In short, I would highlight the next factors that influenced survival the most. It may be tempting to say that being a `Female` or being a `Child` was a gamechanger. However, the `Fare` that a passenger paid for the ticket *(which is the marker of the passenger's social class)* has made a huge difference. For example, a *3-class female* had almost the same chances to survive as a *1-class male*. The `RandomForestClassifier` *(which is one of the most powerful classifiers)* suggests the following rank of survival-influence features *(top 5)*:
1. `Fare` *(consider this as a more sophisticated marker of the passenger's social class)*
2. `Age` *(being a child might help a lot the passenger to survive)*
3. `Female`
4. `Male`
5. `3-Class Passengers` *(e.g., 3-class females had pretty fair chances (50%) to survive, while higher-class females were **likely** (~90%) to survive)*

## :hammer_and_wrench: Libraries Used
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `sklearn`
- `scipy.stats`

## :toolbox: Setup Instructions
0. I believe that you have [python](https://www.python.org/downloads/) already installed on your machine.  
1. I am using [miniconda](https://www.anaconda.com/docs/getting-started/miniconda/install) and [Visual Studio Code](https://code.visualstudio.com/download) with [Jupyter extension](https://www.google.com/search?q=jupyter+extension+in+vs+code).
2. In case, you would really want to play around with the notebook, I include [the environment](/env/environment.yaml) file which you can use to install all the dependencies. 
3. If you reached this step, you do need to add the environment as a Jupyter kernell.  

:santa: CHRISTMAS GIFT FROM THE SANTA :santa:  
Once you have installed `miniconda` and downloaded the `environment.yaml`, run this code in the Anaconda Prompt console ->
```bash
conda env create -f environment.yaml
conda activate ds
python -m ipykernel install --user --name ds --display-name "Python DS"
```

The data is located right [here](/data/titanic.csv). 

## :raising_hand_man: Author
Volodymyr Karpenko  
[LinkedIn](https://www.linkedin.com/in/volod-karpenko/) • <a href=mailto:volod1701@gmail.com>Email </a>(volod1701@gmail.com)
