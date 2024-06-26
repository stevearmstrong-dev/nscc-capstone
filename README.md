# NSCC Capstone Project: Cardiovascular Disease Risk Prediction Model
This repository was created to fulfill the requirements of NSCC's Capstone Project as part of Team Prediction in the Business Intelligence Analytics Program. The objective of the Capstone Project is to acquire hands-on experience on a group project applying much of the material and skills learned throughout the program.

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

![Model Training Visualization](assets/classifier.png)

The RandomForestClassifier was chosen for its efficacy in classification tasks, its intrinsic ability to manage overfitting, and its feature importance capabilities, which are instrumental for understanding the predictive power of the various risk factors involved in cardiovascular disease.

### Model Validation and Testing
- **Prediction**: Applied the trained model to the testing dataset to predict cardiovascular disease risk.
- **Probability Assessment**: Computed prediction probabilities, offering insights into model confidence levels for each prediction.

### Model Evaluation
- **Classification Report**: Generated a detailed classification report using sklearn, providing precision, recall, and f1-score metrics for a comprehensive performance assessment.
- **ROC Score**: Calculated the receiver operating characteristic (ROC) score, measuring the model's ability to distinguish between classes.

## Visualizations
### PairGrid - Histogram and ScatterPlot

![PairGrid Histogram and ScatterPlot](assets/pairgrid.png)

### Distribution of the Categorical Features of the Dataset

![Distribution of Categorical Features](assets/categorical.png)

### Distribution of the Numerical Features of the Dataset

![Distribution of Numerical Features](assets/numerical.png)

### Visualization of Factors Causing Heart Disease

![Factors Causing Heart Disease](assets/bar_chart.png)

## Key Findings
- The RandomForestClassifier demonstrated promising accuracy in predicting cardiovascular disease risk, as evidenced by the classification report and ROC score.

![Classification Report](assets/classification_report.png)

## Report Breakdown:

### Class 0 (Negative Class)
- **Precision**: 92% precision means that when the model predicts an instance as Class 0 (no cardiovascular disease risk), it is correct 92% of the time.
- **Recall**: 100% recall for Class 0 means the model successfully identifies all actual instances of Class 0 in the dataset. This is an ideal scenario for recall, indicating no Class 0 instances were mistakenly labeled as Class 1 by the model.
- **F1-Score**: The F1-score is a harmonic mean of precision and recall, sitting at 96% for Class 0. This high score suggests a very balanced and effective model performance for this class, as it skillfully balances both precision and recall.
- **Support**: Indicates the total number of actual instances of Class 0 in the dataset, which is 85,134. This is the number the model was tested against for its predictions.
### Class 1 (Positive Class):
- **Precision**: 48% precision for Class 1 means that less than half of the instances predicted as Class 1 (indicating a risk of cardiovascular disease) are correctly identified. This low precision indicates a significant number of false positives, where the model incorrectly flags risk where there is none.
- **Recall**: At 2% recall, the model only correctly identifies 2% of all actual Class 1 instances. This extremely low recall indicates the model is missing almost all true Class 1 instances, failing to flag them as at risk.
- **F1-Score**: The F1-score for Class 1 is at 5%, reflecting the poor balance between precision and recall for this class. It suggests the model is ineffective at predicting cardiovascular disease risk accurately for those who have it.
- **Support**: This is the total number of actual instances of Class 1 in the dataset, amounting to 7,523. It's the benchmark for evaluating how well the model predicts cardiovascular disease risk.

### Accuracy:
- Overall, the model correctly predicted 92% of all cases. However, this metric can be misleading for imbalanced classes.

## Interpretation:

While the model performs exceptionally well in class 0 (likely the majority class), it struggles significantly with class 1, as indicated by the low recall and F1-score for class 1. This suggests the model is biased towards the majority class and has difficulties identifying the minority class (class 1), which is a common issue in imbalanced datasets.

## Impact
- **Predictive Power**: This model significantly enhances my ability to predict cardiovascular disease risk, potentially informing more targeted preventative measures.
- **Model Confidence**: Probability assessments provide valuable insights into the model's confidence in its predictions, guiding clinical decision-making processes.

### Understanding the Results
The notebook includes detailed comments and visualizations to help you understand each step of the process, from data exploration to model evaluation. Here's what to look for:

* Data Exploration and Visualization: Initial sections of the notebook provide insights into the dataset's structure and distribution of variables.
* Model Training: Look for the section where the RandomForestClassifier is trained with the cvd_cleaned.csv dataset.
* Model Evaluation: The final sections will show the model's performance on the test set, including accuracy, precision, recall, and the ROC score. Interpret these metrics to gauge the model's effectiveness in predicting cardiovascular disease risk.

## Contact
For any questions or discussions, feel free to contact me at [steve@stevearmstrong.org](mailto:steve@stevearmstrong.org).

### License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE) file for details.
