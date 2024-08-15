# AIDI1010-Emerging-AI

## 1. Data Overview
   
The dataset used in this project is StudentsPerformance.csv, which includes various features related to student performance. Key features are:

Gender: Gender of the student
Race/Ethnicity: Categorical variable representing the student's race/ethnicity
Parental Level of Education: Categorical variable representing the highest level of education attained by the student's parents
Lunch: Type of lunch the student receives (standard or free/reduced)
Test Preparation Course: Whether the student completed a test preparation course
Math Score: Student's score in mathematics
Reading Score: Student's score in reading
Writing Score: Student's score in writing

### Contents

Data Cleaning and Preparation: Standardization of features, encoding categorical variables, and feature engineering.
Model Training and Evaluation: Training and evaluating different regression models.
AutoML Implementation: Use of AutoML to optimize the model-building process.
Quantum Computing: Conceptual exploration of quantum-enhanced features.
Visualization: Summary of model performance and data visualization.

### Requirements

Python 3.6+

Pandas

NumPy

scikit-learn

Pennylane

Matplotlib 

## 2. Data Cleaning and Preparation
Data Standardization
Numerical features (Math Score, Reading Score, Writing Score) are standardized using StandardScaler to ensure they have a mean of 0 and a standard deviation of 1.

### Handling Missing Values

The dataset is checked for missing values, and none are found, indicating that no additional handling is required.

### Encoding Categorical Variables

Categorical features are encoded using LabelEncoder to convert them into numeric formats suitable for machine learning models.

### Feature Engineering

Two new features are created:

Total Score: Sum of Math, Reading, and Writing Scores
Average Score: The average of the Total Score

## 3. Model Training and Evaluation

The dataset is split into training and test sets with an 80-20 ratio. Various machine learning models are trained and evaluated based on:

Root Mean Squared Error (RMSE)
Mean Absolute Error (MAE)
R-squared (R2) Score
Models Used
Decision Tree Regressor
Artificial Neural Network (ANN)
J48 (Decision Tree)
NNge (kNN)
Multi-Layer Perceptron (MLP)
Random Forest Regressor
k-Nearest Neighbour (kNN)

## 4. Results and Visualization

### Model Performance

The performance of each model is evaluated, including training and test metrics. Results are summarized and sorted based on R2 scores in a DataFrame.

### Visualization

Correlation Matrix: Displays relationships between features.
Total Score Distribution: Visualized with a histogram.
Pair Plot: Shows relationships among Math, Reading, and Writing Scores with regression lines.

## 5. AutoML Implementation

An AutoML pipeline is implemented using the mljar-supervised library, automating the machine learning process from preprocessing to model selection. The AutoML model is trained, predictions are made, and a performance report is generated.

### Prediction and Outcomes

The AutoML ensemble model significantly outperformed manually selected models, with an RMSE of 16.0563. This aligns with expectations, as ensemble methods often provide better accuracy by combining multiple models' strengths. The results are consistent with existing research, which highlights the effectiveness of ensemble methods and AutoML in educational predictions.

## 6. Conceptual Enhancement: Quantum Computing
   
A basic quantum feature is added to the dataset using a 2-qubit quantum circuit. This conceptual addition explores the potential benefits of quantum-enhanced features for model performance.

### Why Quantum Computing?

Quantum Computing may offer efficient solutions for certain problems. By integrating quantum features, we can investigate their impact on prediction accuracy.

## 7. Visualization and User-Friendliness
   
Results are visualized through various graphs and tables to facilitate understanding. The code is structured with comments to make it accessible to users with a basic knowledge of data science.

Installation and Setup
Install Required Libraries:

```bash
pip install PennyLane mljar-supervised
```

Run the Code:

Ensure StudentsPerformance.csv is in the working directory, then execute the script to perform data analysis, model training, and evaluation.

### Conclusion

This project demonstrates the application of data preprocessing, machine learning, AutoML, and quantum computing to predict student performance. The results emphasize the value of automated methods and advanced computational techniques in improving prediction accuracy and understanding data relationships.
