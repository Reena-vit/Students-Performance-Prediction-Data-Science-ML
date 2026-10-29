# Students-Performance-Prediction-Data-Science-ML

Students Performance Prediction and Analysis Using Machine Learning

📌 Project Overview

This project focuses on analyzing student-related factors and predicting examination scores using Machine Learning regression algorithms.

The project explores student performance through data inspection, data cleaning, exploratory data analysis (EDA), correlation analysis, model training, evaluation, and performance prediction.

Six machine learning models are trained and compared using multiple evaluation metrics. The best-performing model is selected based on the highest R² score on the test dataset. The selected model and preprocessing pipeline are saved for future predictions.

The project also supports interactive predictions by accepting student details from the user and estimating their examination scores.

🎯 Objectives

- Analyze factors associated with student examination performance.
- Inspect, clean, and preprocess the dataset.
- Perform exploratory data analysis and visualize important patterns.
- Train and compare multiple machine learning regression models.
- Evaluate model performance using standard regression metrics.
- Identify important features using Random Forest feature importance.
- Select the best-performing model based on test-set R².
- Save the trained model and preprocessing pipeline using Joblib.
- Predict examination scores for new student inputs.
- Categorize predicted performance into understandable groups.

📊 Dataset Description

The project uses the Student Performance Factors dataset.

The dataset is loaded from a ZIP file containing a CSV file. The notebook includes data inspection, data-quality auditing, duplicate removal, missing-value handling, and final cleaning verification.

Dataset preparation

The notebook performs the following operations:

- Inspects dataset dimensions, column names, data types, and statistical summaries.
- Checks for missing values and duplicate records.
- Audits numerical ranges and categorical consistency.
- Examines potential numerical outliers.
- Removes duplicate rows.
- Handles missing numerical values using the median.
- Handles missing categorical values using the mode.
- Verifies data quality after cleaning.

Target Variable

"Exam_Score"

The target variable represents the examination score that the machine learning models aim to predict.

Features Used for Prediction

The notebook uses the following five features:

Feature| Description
"Hours_Studied"| Hours spent studying
"Attendance"| Student attendance
"Previous_Scores"| Previous examination scores
"Sleep_Hours"| Hours of sleep
"Tutoring_Sessions"| Number of tutoring sessions

These features are separated from the target variable before the data is split into training and testing sets.

🔍 Exploratory Data Analysis (EDA)

The project explores the dataset using statistical analysis and visualizations.

The notebook includes:

- Distribution of examination scores.
- Relationship between hours studied and examination scores.
- Relationship between attendance and examination scores.
- Average examination scores across selected categorical groups.
- Correlation analysis among numerical variables.
- Correlation of numerical features with "Exam_Score".

These analyses help explore patterns and relationships within the dataset.

⚙️ Data Preprocessing

The project uses Scikit-learn preprocessing tools.

The preprocessing pipeline includes:

- StandardScaler: Standardizes numerical features.
- OneHotEncoder: Encodes categorical features when present.
- ColumnTransformer: Organizes the preprocessing operations.

The preprocessor is fitted on the training data and then applied to the test data to avoid fitting preprocessing transformations on the test set.

🤖 Machine Learning Algorithms

Six regression algorithms are trained and evaluated.

No.| Algorithm| Purpose
1| Linear Regression| Establishes a linear regression baseline
2| Decision Tree Regressor| Learns decision-based relationships
3| Random Forest Regressor| Combines multiple decision trees
4| XGBoost Regressor| Uses gradient boosting for reg
The notebook trains each model on the preprocessed training data and generates predictions on the test dataset.

📈 Model Evaluation

The models are evaluated using four regression metrics.
Metric
Description
MAE
Mean Absolute Error
MSE
Mean Squared Error
RMSE
Root Mean Squared Error
R² Score
Measures how well the model explains variation in the target
The notebook creates a comparison table containing the evaluation results for all six models.
It also generates visual comparisons using:
R² scores.
RMSE values.
Model selection: The model with the highest test-set R² score is selected as the final model.
The actual metric values and selected model can be found in the executed notebook.
🌟 Feature Importance
The project uses the trained Random Forest Regressor to examine feature importance.
The notebook:
Extracts feature names from the preprocessing pipeline.
Calculates Random Forest feature importance.
Sorts the features by importance.
Displays the top 15 features.
Visualizes the feature importance values.
Feature importance helps identify which input features contribute most to the Random Forest model's predictions. These values indicate model-specific importance, not necessarily causation.
📉 Test-Set Performance Analysis
The project performs additional analysis on the test-set predictions.
It includes:
Comparison of actual and predicted examination scores.
Visualization of actual versus predicted scores.
Categorization of predicted scores.
Display of the first 20 test-set predictions.
Counts of students in each predicted performance category.
Performance Categories
The notebook defines three categories based on predicted examination scores.
Predicted Score
Performance Category
Below 60
At Risk
60 to below 75
Needs Improvement
75 or above
On Track
These categories are project-defined thresholds intended to make predictions easier to interpret. They should not be treated as official academic classifications.
💾 Model Saving and Loading
After evaluating the six models, the notebook selects the model with the highest test-set R² score.
The selected model and preprocessing pipeline are saved using Joblib.
Saved Model Files
File
Purpose
student_performance_model.pkl
Stores the selected trained regression model
student_preprocessor.pkl
Stores the fitted preprocessing pipeline
The notebook saves these files in the Colab runtime at the following paths:
/content/student_performance_model.pkl
/content/student_preprocessor.pkl
The notebook subsequently loads the saved model and preprocessor for prediction.
Note: These files are created in the Colab runtime. They must be downloaded or saved to persistent storage separately if you want to reuse them after the runtime ends.
🧑‍💻 Interactive Student Performance Prediction
The project includes an interactive prediction section that accepts new student information.
How It Works
Loads the saved model and preprocessing pipeline.
Asks the user how many students to evaluate.
Collects the five input features for each student.
Validates numerical inputs against the ranges in the dataset.
Checks that numerical values are valid and whole-number inputs are used where appropriate.
Preprocesses the collected student information.
Generates predictions using the trained models.
Displays the selected model's predicted examination scores.
Assigns a performance category to each prediction.
Prediction Output
For each student, the notebook displays:
Predicted examination score.
Predicted performance category.
The notebook also displays predictions from the individual trained models for comparison.
The actual predicted scores depend on the student inputs and the trained models.
🛠️ Technologies Used
Python
Google Colab
Pandas
NumPy
Matplotlib
Scikit-learn
XGBoost
Joblib
Jupyter Notebook
📂 Repository Structure
The GitHub repository contains the following files:
Students-Performance-Prediction-Data-Science-ML/
│
├── README.md
└── Data Science Project.ipynb
The notebook contains the project implementation, analysis, model training, evaluation, and interactive prediction code.
The saved model files are generated separately when the relevant notebook cells are executed.
▶️ How to Run the Project
Option 1: Google Colab
Open the notebook from this GitHub repository.
Open it in Google Colab.
Upload or mount the dataset ZIP file.
Update the dataset path in the data-collection cell if necessary.
Run the notebook cells in order.
Review the EDA visualizations and model evaluation results.
Execute the model-saving cells.
Run the interactive prediction section and enter student details.
Option 2: Local Python Environment
Download or clone the repository.
Install the required Python libraries.
Make the dataset CSV file available.
Update the dataset path in the notebook.
Run the notebook using Jupyter Notebook or JupyterLab.
Execute the cells in order.
Install Required Libraries
pip install pandas numpy matplotlib scikit-learn xgboost joblib jupyter
Important: The notebook initially loads the dataset from Google Drive using a Colab-specific path. When running locally, update this path and ensure that the dataset is available.
The interactive prediction section also uses Python's input() function, which is suitable for an interactive notebook environment.
📌 Key Highlights
Complete data-cleaning and data-quality workflow.
Exploratory data analysis and correlation analysis.
Six machine learning regression models.
Evaluation using MAE, MSE, RMSE, and R².
Model comparison and automated best-model selection.
Random Forest feature importance analysis.
Actual-versus-predicted score visualization.
Test-set performance categorization.
Model and preprocessing pipeline persistence using Joblib.
Interactive predictions using new student inputs.
🔮 Future Improvements
Potential extensions include:
Developing a web interface for student performance predictions.
Adding more relevant features to improve predictive performance.
Performing systematic hyperparameter tuning.
Comparing model performance across different data splits.
Improving prediction interpretability.
Adding automated tests and a reproducible execution environment.
Evaluating model generalization on additional datasets.
⚠️ Limitations
Predictions depend on the dataset, selected features, and training procedure.
Model performance should be assessed using the actual evaluation results.
The performance categories are custom thresholds and are not official academic standards.
Predictions should be interpreted as estimates rather than guaranteed examination outcomes.
The notebook requires the dataset to be available at the configured path.
Model files saved in a temporary Colab runtime may need to be downloaded or stored persistently for future use.
👩‍💻 Author
Reena
Data Science Project using Machine Learning 
