# NSCC Capstone Project : Cardiovascular Disease Risk Prediction Model
This repository was created to fulfill the requirements of NSCC's Capstone Project as part of the Business Intelligence Analytics Program. The objective of the Capstone Project is to acquire hands-on experience on a group project applying much of the material and skills learned throughout the program.

### Introduction and Motivation

This project aims to develop a robust predictive model for assessing the risk of cardiovascular disease (CVD) using the random forest algorithm. Cardiovascular diseases are among the leading causes of mortality globally. Early risk prediction can significantly improve outcomes through timely intervention and preventative measures. This project combines data exploration, visualization, and machine learning to provide insights into CVD risk factors and predict individual risk levels.

### Features

* Data Exploration and Visualization: Utilizing seaborn and Matplotlib for in-depth analysis and visualization of dataset attributes.
* Data Preprocessing: Employing Scikit-learn for data cleaning and preparation tasks.
* Predictive Modeling: Building and training a random forest classifier to accurately predict CVD risk.

### Technologies Used
- Python
- numpy
- pandas
- Scikit-learn
- Seaborn
- Matplotlib

### Dataset

The dataset used in this project is comprehensive, covering a wide range of variables associated with cardiovascular disease (CVD) risk factors. Each record in the dataset represents individual respondents with the following attributes:

- **General_Health**: Overall health rating of the individual (e.g., Excellent, Very Good, Good, Fair, Poor).
- **Checkup**: Frequency of medical checkups (e.g., Within last year, Within past two years, etc.).
- **Exercise**: Information on physical activity levels. (Yes/No)
- **Heart_Disease**: Presence of heart disease (Yes/No).
- **Skin_Cancer**: History of skin cancer (Yes/No).
- **Other_Cancer**: History of any cancer other than skin cancer (Yes/No).
- **Depression**: Indicator of depression (Yes/No).
- **Diabetes**: Indicates if the individual has diabetes (Yes/No).
- **Arthritis**: Indicates if the individual has arthritis (Yes/No).
- **Sex**: Biological sex of the respondent.
- **Age_Category**: Age range category of the respondent.
- **Height_(cm)**: Height of the individual in centimeters.
- **Weight_(kg)**: Weight of the individual in kilograms.
- **BMI**: Body Mass Index calculated from height and weight.
- **Smoking_History**: Smoking habits (Yes/No).
- **Alcohol_Consumption**: Quantity of alcohol consumption.
- **Fruit_Consumption**: Quantity of fruit consumption habits.
- **Green_Vegetables_Consumption**: Quantity of green vegetable consumption.
- **FriedPotato_Consumption**: Quantity of fried potato consumption.

This dataset provides a holistic view of factors that could influence the risk of developing cardiovascular diseases, allowing for detailed analysis and modeling to predict CVD risk.


### Model Building and Training

The predictive model for cardiovascular disease risk prediction was constructed using the RandomForestClassifier from sklearn, leveraging its capabilities for handling complex datasets with a mix of categorical and numerical data.

#### Model Configuration
- **Algorithm**: RandomForestClassifier
- **Key Parameter**: `n_estimators` was set to specify the number of trees in the forest, chosen based on preliminary validation to balance between overfitting and computational efficiency.

#### Training Process
- **Training Data**: The model was trained using `X_train` for the input features, encompassing a diverse range of variables such as age, gender, blood pressure, and cholesterol levels.
- **Target Variable**: `y_train` represented the presence or absence of cardiovascular disease, serving as the output parameter for the model.
- **Methodology**: Employed a robust training methodology to ensure the model accurately captures the underlying patterns without overfitting the training data.

