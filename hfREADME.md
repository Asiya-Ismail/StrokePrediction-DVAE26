---
library_name: sklearn
tags:
- random-forest
- stroke-prediction
- sklearn
pipeline_tag: tabular-classification
license: mit
---


# Stroke Prediction Random Forest Model

This project uses a Random Forest model to predict the risk of strokes based on user input features. The model has been deployed on Hugging Face for seamless integration.

## Features
- Predicts the likelihood of a stroke based on various health parameters.
- Fast and efficient model, hosted on Hugging Face.

## Input Features
The model expects the following inputs:
- `age`: Patient's age (numeric)
- `age_group`: Patients age group child(Less than 18 ),Young Adult (18-34 ), Adult (35-59 ), Senior (60 and over )
- `hypertension`: 1 if the patient has hypertension, else 0
- `heart_disease`: 1 if the patient has heart disease, else 0
- `avg_glucose_level`: Average glucose level in the blood
- `bmi`: Body Mass Index
- `gender`: Male/Female/Other
- `ever_married`: Yes/No
- `work_type`: Type of work (e.g., Private, Self-employed, never_worked)
- `Residence_type`: Urban/Rural
- `smoking_status`: Smoking habits (e.g., never smoked, formerly smoked)

## Model Deployment
The model has been deployed on the [Hugging Face Hub](https://huggingface.co). You can access it via my repo [Random Forest Model for Stroke Prediction](https://huggingface.co/Asiya-Mohammed/random-forest-model).

