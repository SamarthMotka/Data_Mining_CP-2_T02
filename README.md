# Team ID: 02 - Data Classification and Evaluation

## Team Members
- Nirmal Shah (202311043)
- Samarth Motka (202311023)
- Darshit Kalariya (202311035)
- Deepak Khatri (202311042)
- Viraj Prajapati (202311069)

## Dataset Overview
This dataset contains information about various aspects of individuals, including demographic information and health metrics. Here's an overview of the columns in the dataset:

- **Sex**: Gender of the individual (One-hot encoded: Male, Female).
- **Age**: Age of the individual rounded up to the nearest 5 years.
- **Height**: Height of the individual rounded up to the nearest 5 centimeters (cm).
- **Weight**: Weight of the individual in kilograms (kg).
- **Sight (Left and Right)**: Eyesight of the individual for the left and right eyes.
- **Hearing (Left and Right)**: Hearing status of the individual for the left and right ears (1: Normal, 2: Abnormal).
- **Systolic Blood Pressure (SBP)**: Systolic blood pressure in mmHg.
- **Diastolic Blood Pressure (DBP)**: Diastolic blood pressure in mmHg.
- **Fasting Blood Glucose (BLDS)**: Fasting blood glucose level in mg/dL.
- **Total Cholesterol (tot_chole)**: Total cholesterol level in mg/dL.
- **HDL Cholesterol (HDL_chole)**: High-density lipoprotein (HDL) cholesterol level in mg/dL.
- **LDL Cholesterol (LDL_chole)**: Low-density lipoprotein (LDL) cholesterol level in mg/dL.
- **Triglycerides**: Triglyceride level in mg/dL.
- **Hemoglobin**: Hemoglobin level in g/dL.
- **Urine Protein**: Presence of protein in urine (1: -, 2: +/-, 3: +1, 4: +2, 5: +3, 6: +4).
- **Serum Creatinine**: Serum (blood) creatinine level in mg/dL.
- **SGOT (AST)**: Aspartate transaminase (AST) level in IU/L.
- **SGOT (ALT)**: Alanine transaminase (ALT) level in IU/L.
- **Gamma-GTP (gamma_GTP)**: Gamma-glutamyl transpeptidase (γ-GTP) level in IU/L.
- **Smoking Status (Smk_stat_type_cd)**: Smoking status (1: Never, 2: Used to smoke but quit, 3: Still smoke).
- **Drinker or Not (DRK_YN)**: Whether the individual is a drinker or not.

## Data Preprocessing
- Categorical features are one-hot encoded.
- Features are divided into independent and dependent features.
- Feature scaling is applied using the RobustScaler class.

## Classification Models for Smoking Status
We classify individuals into three categories: never a smoker, used to be a smoker, or still a smoker. The following models are used for this classification:
1. **Logistic Regression Model**: A simple linear model to understand the relationship between input features and smoking status.
2. **Random Forest Model**: An ensemble model to capture complex relationships in the data.
3. **Grid Search CV on Random Forest**: Hyperparameter tuning for the Random Forest model.
4. **AdaBoost Classifier**: An ensemble model to improve the performance of weak classifiers.

## Classification Models for Drinker Status
We classify individuals into two categories: drinkers and non-drinkers. The following models are used for this classification:
1. **Logistic Regression Model**: A straightforward model to understand the relationship between input features and drinker status.
2. **Random Forest Model**: A versatile model to handle complex relationships in the data.
3. **K-Nearest Neighbor (K-NN)**: A non-parametric model that classifies individuals based on feature similarity to their nearest neighbors.

## Evaluation
- A classification report summarizes the performance of each model, including metrics like precision, recall, and F1-score for each class.
- A confusion matrix helps evaluate the model's performance in terms of true positives, true negatives, false positives, and false negatives.

These tools and models assist in predicting an individual's smoking and drinking status based on the provided features. Model performance metrics guide the selection of the best model for each classification task.
