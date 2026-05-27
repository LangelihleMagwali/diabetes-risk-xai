# Diabetes Risk Prediction with Explainable AI

## Project Overview

This project uses machine learning and Explainable AI to predict diabetes risk using health, lifestyle, and demographic indicators. The goal is to build a classification model that can identify whether an individual may be at risk of diabetes and then explain the model’s predictions using Explainable AI methods such as SHAP and LIME.

The project focuses not only on prediction accuracy, but also on model interpretability. This is important because healthcare-related models should be understandable, transparent, and useful for decision-making. By applying Explainable AI, the project aims to show which health indicators influence the model’s predictions and how these insights can support early diabetes screening and prevention strategies.

---

## Research Question

Can machine learning models predict diabetes risk from health indicators, and can Explainable AI methods explain which factors contribute most to the prediction?

---

## Dataset

The dataset used in this project is the **Diabetes Health Indicators Dataset**, based on health survey data.

The dataset contains health, lifestyle, and demographic features such as:

- High blood pressure
- High cholesterol
- Cholesterol check
- BMI
- Smoking status
- Stroke history
- Heart disease or heart attack
- Physical activity
- Fruit consumption
- Vegetable consumption
- Heavy alcohol consumption
- Healthcare access
- Doctor visit cost barrier
- General health
- Mental health
- Physical health
- Difficulty walking
- Sex
- Age
- Education
- Income

The original target variable is:

```text
Diabetes_012
```

Where:

```text
0 = No diabetes
1 = Prediabetes
2 = Diabetes
```

For this project, the target variable was converted into a binary classification problem:

```text
0 = No diabetes
1 = Prediabetes or diabetes risk
```

This makes the project easier to interpret and more useful for identifying individuals who may need early screening or health intervention.

---

## Project Type

This is a **binary classification project**.

The model predicts whether a person belongs to one of two groups:

```text
No diabetes
At risk of diabetes
```

This is not a regression project because the target variable is a category, not a continuous numerical value.

---

## Repository Structure

```text
diabetes-risk-xai/
│
├── data/
│   └── diabetes_012_health_indicators_BRFSS2015.csv
│
├── notebooks/
│   └── diabetes_xai_full_pipeline.ipynb
│
├── presentation/
│   └── diabetes_xai_presentation.pptx
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Project Workflow

The project follows these main steps:

1. Data loading and understanding
2. Data cleaning and preprocessing
3. Exploratory Data Analysis
4. Feature and target preparation
5. Model training
6. Model evaluation
7. Explainable AI analysis
8. Business and healthcare recommendations
9. Final presentation and documentation

---

## Exploratory Data Analysis

The Exploratory Data Analysis section investigates patterns between diabetes risk and different health indicators.

The main visualisations include:

- Diabetes risk class distribution
- Percentage distribution of diabetes risk classes
- BMI distribution by diabetes risk
- Average BMI by diabetes risk
- Diabetes risk by high blood pressure
- Diabetes risk by high cholesterol
- Diabetes risk by physical activity
- Diabetes risk by general health
- Diabetes risk by age group
- Diabetes risk by income level
- Diabetes risk by education level
- Correlation of features with diabetes risk

A consistent blue, orange, and yellow colour palette is used throughout the visualisations to make the analysis clear and presentation-friendly.

---

## Data Preparation

The original dataset contains the target variable `Diabetes_012`, which has three classes. Since the prediabetes class is much smaller than the other classes, the target variable was transformed into a binary variable called `Diabetes_binary`.

The transformation was done as follows:

```text
0 = No diabetes
1 = Prediabetes or diabetes
```

This binary target allows the model to focus on identifying individuals who may be at risk of diabetes.

The dataset was also checked for:

- Missing values
- Duplicate rows
- Data types
- Summary statistics
- Target variable imbalance

---

## Machine Learning Models

The project compares interpretable and black-box machine learning models.

Planned models include:

| Model | Purpose |
|---|---|
| Logistic Regression | Baseline interpretable model |
| Decision Tree | Simple explainable model |
| Random Forest | Main black-box model |
| XGBoost | Stronger black-box model |

The final model will be selected based on performance and explainability.

---

## Model Evaluation

Because the dataset is imbalanced, accuracy alone is not enough to evaluate the model.

The following evaluation metrics are used:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion matrix
- Classification report

Recall is especially important because, in a healthcare setting, failing to identify someone at risk of diabetes could be harmful.

---

## Explainable AI Methods

The project uses Explainable AI to understand how the model makes predictions.

### Feature Importance

Feature importance is used to identify which variables contribute most to the model’s predictions. This helps show which health indicators the model relies on most when predicting diabetes risk.

### SHAP

SHAP is used to explain both global and local model behaviour.

SHAP helps answer questions such as:

- Which features are most important overall?
- Which features increase diabetes risk?
- Which features reduce diabetes risk?
- Why did the model predict a specific person as high risk?

Planned SHAP outputs include:

- SHAP summary plot
- SHAP bar plot
- SHAP waterfall plot for an individual prediction

### LIME

LIME is used to explain individual predictions in a simple and understandable way.

It helps show which features influenced one specific prediction. This is useful for explaining the model’s decision to a non-technical audience.

---

## Expected Insights

The project is expected to identify important diabetes risk factors such as:

- BMI
- High blood pressure
- High cholesterol
- General health
- Age
- Physical activity
- Difficulty walking
- Income
- Education

These insights can help make the model useful for healthcare decision-making.

---

## Business and Healthcare Value

The model can support public health and healthcare decision-making by helping identify individuals who may be at risk of diabetes.

Possible uses include:

- Early diabetes risk screening
- Targeted health awareness campaigns
- Preventive healthcare planning
- Supporting lifestyle intervention programmes
- Helping healthcare providers understand key risk factors
- Improving communication of model results through Explainable AI

Explainable AI makes the model more transparent by showing why certain individuals are predicted to be at risk.

---

## GitHub Workflow

This project uses Git and GitHub for version control and teamwork.

The main branch structure is:

```text
main
eda-data-cleaning
model-training
xai-explanations
presentation-readme
```

### Branch Purpose

| Branch | Purpose |
|---|---|
| main | Final clean version of the project |
| eda-data-cleaning | Data understanding, cleaning, and EDA |
| model-training | Model training and evaluation |
| xai-explanations | SHAP, LIME, and model interpretation |
| presentation-readme | README, final report, and presentation |

Each team member works on their own branch and creates pull requests before merging into `main`.

---

## GitHub Project Board

The team also uses a GitHub Project board to track tasks and monitor progress.

Main issues include:

1. Complete data understanding and cleaning
2. Create exploratory data analysis visualisations
3. Train and evaluate machine learning models
4. Apply Explainable AI methods
5. Prepare final README and presentation

This helps organise teamwork and track progress throughout the project.

---

## Team Work Distribution

| Team Member | Main Responsibilities |
|---|---|
| Langelihle Magwali | Data understanding, data cleaning, EDA visualisations, EDA interpretation, GitHub setup |
| Chiedza Chimedza | Model training, model evaluation, XAI explanations, model interpretation |
| Both members | README, presentation, final review, business and healthcare recommendations |

---

## How to Run the Project

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/diabetes-risk-xai.git
```

Move into the project folder:

```bash
cd diabetes-risk-xai
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Open the notebook:

```bash
jupyter notebook notebooks/diabetes_xai_full_pipeline.ipynb
```

Run the notebook cells from top to bottom.

---

## Requirements

The main Python libraries used are:

```text
pandas
numpy
matplotlib
seaborn
scikit-learn
shap
lime
xgboost
jupyter
```

These packages are also listed in the `requirements.txt` file.

---

## Limitations

This project has some limitations:

- The dataset is based on survey responses, so some variables may be self-reported.
- The dataset is imbalanced, with more individuals in the no-diabetes group.
- The model identifies patterns and associations, but it does not prove medical causation.
- The model should support healthcare decision-making, not replace professional medical diagnosis.
- SHAP and LIME explain model behaviour, not direct medical causes.
- The dataset comes from a specific survey context, so results may not generalise perfectly to every population.

---

## Ethical Considerations

Since this project involves health-related prediction, ethical use of the model is important.

The model should not be used as a replacement for professional medical advice or diagnosis. Instead, it should be seen as a decision-support tool that can help identify possible risk factors and support early screening strategies.

Explainability is important because users and stakeholders need to understand why the model makes certain predictions, especially in a healthcare context.

---

## Authors

This project was completed as part of an Explainable Artificial Intelligence capstone project.

Team members:

- Langelihle Magwali
- Chiedza Chimedza

---

## Project Status

Current progress:

- [x] Repository created
- [x] Dataset added
- [x] Notebook created
- [x] Binary target variable created
- [x] Data understanding started
- [x] EDA visualisations started
- [ ] Model training
- [ ] Model evaluation
- [ ] SHAP explanations
- [ ] LIME explanations
- [ ] Final presentation

---

## Final Goal

The final goal of this project is to build a machine learning model that can predict diabetes risk and explain the prediction results in a way that is understandable to non-technical stakeholders.

The project aims to show how Explainable AI can make machine learning models more transparent, useful, and trustworthy in healthcare-related decision-making.

---

## AI Declaration

During the development of this project, AI tools were used as a support tool to assist with planning, structuring, writing, and improving the clarity of the project documentation and code explanations.

