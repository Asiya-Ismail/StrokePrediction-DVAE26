# Stroke Prediction with Random Forest

## Introduction
A Random Forest and Decision Tree model trained to predict the likelihood of a stroke based on various patient features like age, BMI, and medical history. They were then both compared to find the best model for predictions. The random forest model was the better model for predictions. The accuracy in predictions for the decision tree model was 97 and for random forest model 99.

## Data Quality Report

### Data Source
- The dataset is used in this project is sourced from the Stroke Prediction Kaggle dataset.

### Challenges Faced and Measures Taken for Data Integrity
- There were 201 missing values in BMI.
- Outliers in BMI and Average Glucose Levels were identified but retained to preserve the model's predictive performance. I fixed this by using scaling and robust models like Random Forest, which are less affected by outliers, were used..
- The dataset contained more people with no stroke than with stroke, I solved this using SMOTE to make the two categories balanced.
- BMI also was found to have 972 null values, this was corrected using KNNImputer which fills missing values by using the K-Nearest Neighbors algorithm.
- Random Forest Model performance was improved by fine-tuning hyperparameters.



## Model Development and Workflow Pipeline

### Workflow Overview
1. Data loading and preprocessing (handling missing values, scaling, encoding).
2. Feature Engineering by creating new features(age_group)
2. Decision Tree model selection and training.
3. Random Forest model selection and training.
4. Showcasing Random Forest model Interpretability using feature importance.
5. Unit Tests
6. Evaluations of models using accuracy and F1-score.
7. Deployment to Hugging Face


### Model Development Steps
- **Step 1**: Loaded data using pandas.
- **Step 2**: Cleaned and preprocessed features
- **Step 2**: Performed feature engineering by creating a new feature (age_group).
- **Step 3**: Trained Random Forest model using grid search for hyperparameter tuning. Also trained a decision tree model.
- **Step 4**: Evaluated models with accuracy and confusion matrix.
- **Step 5**: Saved the Random Forest model using joblib.
- **Step 6**: Deployed to hugging face

## Key Findings
- A higher proportion of married individuals experienced strokes compared to unmarried individuals.
- Also found that having hypertension and heart disease has a correlation to getting strokes.
- The average age of patients is 43, with the majority of the population being female.
- Visualizations of feature distributions and correlations are available in the Data Exploration and Quality Analysis section of the jupyter notebook.
- Random Forest outperformed Decision Tree
- For interpretability of Random Forest model we see that the features that play the biggest role in determining the target variable(stroke, no stroke) are age, bmi and average glucose levels.


## Software Engineering Best Practices
- **Git Version Control**: All changes were tracked using Git.
- **Testing**: I created unit tests for certain steps in the workflow like Label Encoding and Standard Scaling.
- **Documentation**: The code is fully documented with comments, prints and a README.

## Model Deployment to Hugging Face

### Deployment Overview
Since the trained Random Forest model was the better of the two models I used that model to deploy to Hugging Face. This deployment process ensures that the model can be accessed easily by others to use for stroke predictions.

### Steps for Deployment
- **Model Repository**: A new repository was created on Hugging Face.
- **Model Upload**: The trained model was uploaded to Hugging Face using the `huggingface_hub` library.
- **Readme Upload**: A readme was also uploaded to Hugging Face using the `huggingface_hub` library that showcases the applications of the model.
