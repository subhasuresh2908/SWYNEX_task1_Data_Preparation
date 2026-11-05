# SWYNEX Internship – Task 4
## End-to-End Data Science Case Study

### 1. Project Overview
This project demonstrates a complete data science workflow using the Palmer Penguins dataset. It includes problem definition, data preparation, exploratory data analysis, machine learning, model evaluation, and conclusions.

### 2. Problem Statement
The objective is to predict penguin species using physical measurements such as bill length, bill depth, flipper length, and body mass.

### 3. Dataset Information
- Dataset: Palmer Penguins
- Total Records: 344
- Total Features: 7
- Target Variable: Species
- Missing Values: 0 after data preparation

### 4. Data Preparation
- Loaded the cleaned dataset.
- Checked missing values.
- Verified data types.
- Prepared numerical features for machine learning.
- Selected species as the prediction target.

### 5. Exploratory Data Analysis
Performed:
- Species distribution analysis.
- Body mass comparison using boxplots.
- Correlation analysis using a heatmap.

### 6. Key Insights
1. Adelie is the most common penguin species.
2. Gentoo penguins have higher body mass than the other species.
3. Flipper length and body mass have a strong positive correlation (0.87).
4. Bill length and flipper length have a positive correlation (0.66).
5. Bill depth and flipper length have a negative correlation (-0.58).

### 7. Machine Learning Models
Implemented two classification algorithms:
- Logistic Regression
- Random Forest Classifier

Dataset split:
- 80% Training
- 20% Testing

### 8. Model Evaluation

| Model | Accuracy |
|---|---:|
| Logistic Regression | 100% |
| Random Forest | 98.55% |

Logistic Regression achieved the highest accuracy on the selected test dataset.

### 9. Conclusion
The project successfully demonstrates an end-to-end data science workflow. Exploratory analysis revealed useful relationships between penguin measurements, and machine learning models were developed to predict penguin species.

Logistic Regression achieved 100% accuracy on the test split, while Random Forest achieved 98.55%.

Further validation using cross-validation and unseen datasets would help assess model generalization.

### 10. Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- GitHub

### 11. Project Outcome
Successfully completed an end-to-end data science case study covering data preparation, EDA, model building, evaluation, and conclusions.