# Ingham Medical Physics Coding Challenge

This repository is the submission for the Ingham Medical Pysical Coding Challenge.

**Task**

Using the data from HN_Radiomics.csv and HN_ClinicalData.csv to predict an outcome for a patient. In this repository, **overall_survival_in_days** and **recurrence_metastatic_free_survival_in_days** are selected as the outcomes respectively. Other features in HN_ClinicalData.csv and GTV in HN_Radiomics.csv are merged as the input of the model. Regression models and classification predictions are both proposed in the repository.

**Classification Model**

See the **Classification_radiotheraphy_prediction.ipynb** Jupyter Notebook for the classification model code and results.

1. Good result (1) : **overall_survival_in_days** >5 years ; Bad result (0) : **overall_survival_in_days** <=5 years 

Top 10 important features as the input, overall_survival_in_days as the output, model accuracy comparison.

| Model | Test_accuracy_score|
| ------ | ------ |
| Random Forest | 80.000% |
| LGBMClassifier | 85.714% |
| DecisionTree | 80.000% |
| LogisticRegression | 91.429% |
| Neural Network | 88.571% |
| SVM | 88.571% |

2. Good result (1) : **recurrence_metastatic_free_survival_in_days** >5 years ; Bad result (0) : **recurrence_metastatic_free_survival_in_days** <=5 years 

Top 10 important features as the input, recurrence_metastatic_free_survival_in_days as the output, model accuracy comparison.

| Model | Test_accuracy_score|
| ------ | ------ |
| LogisticRegression | 88.571% |
| SVM | 85.714% |

**Regression Model**

See the **Regression_radiotheraphy_prediction.ipynb** Jupyter Notebook for the regression model code and results.

1. Regression predict overall_survival_in_days,  comparison on the mean difference between predictions and test_data.

| Model | Test_difference (days)|
| ------ | ------ |
| GradientBoostingRegressor | 27 | See the **Predictions.csv** CSV for the GBoot prediction results.
| RandomForestRegressor | 60 |
| ElasticNet | 185|


2. Regression predict recurrence_metastatic_free_survival_in_days,  comparison on the mean difference between predictions and test_data.

| Model | Test_difference (days)|
| ------ | ------ |
| GradientBoostingRegressor | 77 |

