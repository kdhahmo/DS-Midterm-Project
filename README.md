# Data Science Midterm Project

## Project/Goals
1. Prepare the data for Modelling by cleaning and preprocessing it.
2. Select the type of model to use after trying different models on the data.
3. Tune the hyperparameters of the model.

## Process
### Step 1: EDA

1. Load the data from the provides files in the [data folder](/data/). I chose to load parse the json files and then load them into a DataFrame after. During this step I familiarized myself with the data.
2. Clean and preprocess the data. The data has duplicates of the exact same values which are easy to remove. I also imputed nulls using averages or mode according to state.
3. The visual aspect of EDA helps identify any relationships or lack of between variables.
4. Prepare any columns with string values by making dummies.
5. Save the prepared training and testing data in the [data/processed/ folder](/data/processed/)

The complete details of the data preparation process can be found in the [1 - EDA](/notebooks/1%20-%20EDA.ipynb) notebook in the [notebooks folder](/notebooks/).

### Step 2: Model Selection

1. Try multiple supervised learning models on the preprocessed data.
2. Decide on the criteria for model selection. I used RMSE and adjusted R2 to judge the usefulness of the models.

The complete details of the model selection process can be found in the [2 - model_selection](/notebooks/2%20-%20model_selection.ipynb) notebook in the [notebooks folder](/notebooks/).

### Step 3: Tuning

1. Perform hyperparameter tuning on the best performing model from Part 2.
2. Save the tuned model.

The complete details of the hyperparameter tuning process can be found in the [3 - tuning_pipeline](/notebooks/3 - tuning_pipeline) notebook in the [notebooks folder](/notebooks/).

## Results
The best model score indicates the model can explain 44.98% of the data. The model doesn't use bootstrap, which to me indicates the data is varied enough that the model can get a better idea of the data by seeing it all.

## Challenges 
- Knowing when to stop cleaning the data.
- Using the right setup for hyperparameter tuning. I used the wrong random state and had to re run.

## Future Goals
- Get the city values that were null by using the latitude and longitude values.
- Use the information in tags
- Adjust the features I choose with more consideration for covariance and relation.
- Use adjusted R2 as the scoring metric for hyperparameter tuning.