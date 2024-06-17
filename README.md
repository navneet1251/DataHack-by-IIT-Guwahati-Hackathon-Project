# DataHack-by-IIT-Guwahati-Hackathon-Project
I solved the problem statement given to us by using the Random Forest Classifier from scratch and predicted how likely individuals are to receive their XYZ and seasonal flu vaccines. Specifically, I predicted two probabilities: one for the XYZ vaccine and one for the seasonal flu vaccine.

---

## Project Description: Predicting Vaccination Probabilities Using Machine Learning

### Objective
The primary objective of this project is to predict the probabilities that individuals will choose to take two types of vaccines: the xyz_vaccine and the seasonal_vaccine. This is accomplished through data preprocessing, feature engineering, and applying a Random Forest Classifier.

### Dataset
The dataset used for this project consists of survey responses that include demographic information, health-related behaviors, and attitudes towards vaccination. Key columns in the dataset include:
-> respondent_id: Unique identifier for each respondent.
-> xyz_vaccine: Target variable indicating whether the respondent would take the xyz_vaccine.
-> seasonal_vaccine: Target variable indicating whether the respondent would take the seasonal_vaccine.
-> Various categorical and numerical features representing respondent characteristics and responses.

### Data Preprocessing
To ensure robust model performance, several preprocessing steps were undertaken:
1. Handling Missing Values: Missing values in the dataset were imputed using the most frequent value for each feature.
2. Categorical Encoding: Categorical features 'race', 'sex', 'marital_status', 'rent_or_own', 'employment_status', 'hhs_geo_region','census_msa', 'employment_industry', and 'employment_occupation' were encoded using count or frequency encoding technique and the remaining categorical features like 'income_poverty', 'age_group' ,and 'education' were encoded using ordinal number encoding. This technique replaces each category with mapping each unique category value to a different integer.
3. Feature Scaling: Numerical features were scaled using StandardScaler to normalize the data, which helps improve model accuracy and performance.

### Model Training
Two separate Random Forest Classifier models were trained to predict the likelihood of respondents taking the xyz_vaccine and the seasonal_vaccine respectively:
1. Training and Test Split: The dataset was split into training and testing sets to evaluate the model performance.
2. Model Training: The Random Forest Classifier was chosen due to its robustness and ability to handle a mixture of feature types.
3. Model Evaluation: The models were evaluated using the ROC AUC score to measure their performance in distinguishing between the classes.

### Results
The trained models provided the following results on the test set:
ROC AUC for xyz_vaccine: 0.8318755305112238
ROC AUC for seasonal_vaccine: 0.8519783325648995
Mean ROC AUC: 0.8419269315380616

### Predictions
After evaluating the models, predictions were made for the entire dataset. The predicted probabilities indicate the likelihood of each respondent taking the xyz_vaccine and the seasonal_vaccine.

#### Submission File
A submission file named submission.csv for the evaluation that have features:
-> respondent_id: Unique identifier for each respondent.
-> xyz_vaccine: Predicted probability of the respondent taking the xyz_vaccine.
-> seasonal_vaccine: Predicted probability of the respondent taking the seasonal_vaccine.

---

### Conclusion
This project successfully demonstrated the use of machine learning techniques to predict vaccination probabilities. The Random Forest Classifier models, combined with appropriate data preprocessing, provided robust predictions that can be used for further analysis or decision-making processes.

