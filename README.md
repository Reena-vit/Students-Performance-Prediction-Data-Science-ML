# Students-Performance-Prediction-Data-Science-ML
🎓 Students Performance Prediction and Analysis Using Machine Learning

📌 Project Overview

This project focuses on analyzing student-related factors and predicting examination scores using Machine Learning regression algorithms.

The project explores student performance through data inspection, data cleaning, exploratory data analysis (EDA), correlation analysis, model training, evaluation, and performance prediction.

Six machine learning models are trained and compared using multiple evaluation metrics. The best-performing model is selected based on the highest R² score on the test dataset. The selected model and preprocessing pipeline are saved for future predictions.

The project also supports interactive predictions by accepting student details from the user and estimating their examination scores.

🎯 Objectives

- Analyze student performance data.
- Clean and preprocess the dataset.
- Perform Exploratory Data Analysis (EDA).
- Train and compare multiple Machine Learning models.
- Evaluate models using appropriate performance metrics.
- Identify important features affecting predictions.
- Select the best-performing model based on test-set R².
- Save the trained model and preprocessing pipeline.
- Predict examination scores for new student inputs.
- Categorize predicted performance into understandable groups.
  
📂 Dataset Description

The project uses student performance data for analysis and prediction.

Dataset Information

- Target Variable: "Exam_Score"
- Task Type: Regression
- Purpose: Predict student's exam scores.

🔍 Features Used for Prediction

The model uses the following input features:

1. "Hours_Studied" — Hours spent studying.
2. "Attendance" — Student attendance.
3. "Previous_Scores" — Scores from previous assessments.
4. "Sleep_Hours" — Hours of sleep.
5. "Tutoring_Sessions" — Number of tutoring sessions.

🧹 Data Cleaning and Preprocessing

The project includes data preparation steps to make the dataset suitable for Machine Learning.

- Checking for missing values.
- Checking for duplicate records.
- Separating input features and the target variable.
- Scaling numerical features where required.
- Encoding categorical features where required.
- Preparing the data for model training and testing.

📊 Exploratory Data Analysis (EDA)

Exploratory Data Analysis is used to understand the dataset, examine patterns, and explore relationships between student-related factors and exam scores.

🤖 Machine Learning Models

The project compares the following regression models:

1. Linear Regression
2. Decision Tree Regressor
3. Random Forest Regressor
4. XGBoost Regressor
5. Support Vector Regression (SVR)
6. Multi-Layer Perceptron (MLP) Regressor

📈 Model Evaluation

The models are evaluated using the following metrics:

- MAE (Mean Absolute Error): Measures the average absolute prediction error.
- MSE (Mean Squared Error): Measures the average squared prediction error.
- RMSE (Root Mean Squared Error): Measures prediction error on the target's scale.
- R² Score: Measures how well the model explains variation in the target variable.

The best-performing model is selected based on the test-set R² score, as implemented in the notebook.

🌟 Feature Importance

Random Forest feature importance is used to examine which input features contribute most to the model's predictions.

The project visualizes the top 15 features by importance, where supported by the trained model.

🔮 Student Performance Prediction

The notebook allows users to enter values for selected student features and obtain a predicted exam score.

🎯 Prediction Categories

The project uses these custom score categories:

- At Risk: Predicted score below 60.
- Needs Improvement: Predicted score from 60 to below 75.
- On Track: Predicted score of 75 or higher.

Note: These are project-defined categories, not official academic classifications.

💾 Saved Model Files

The notebook saves the trained model and preprocessing object for later use:

- "student_performance_model.pkl"
- "student_preprocessor.pkl"

🛠️ Technologies Used

- Python
- Pandas — Data manipulation and analysis.
- NumPy — Numerical operations.
- Matplotlib — Data visualization.
- Seaborn — Statistical visualization.
- Scikit-learn — Preprocessing, model training, and evaluation.
- XGBoost — Gradient boosting regression.
- Google Colab — Notebook development and execution.
- GitHub — Project storage and sharing.

📁 Project Structure

The repository contains the following files:

- "Data Science Project.ipynb" — Main notebook containing the analysis, training, evaluation, and prediction workflow.
- "README.md" — Project description and documentation.

🚀 How to Run the Project

1. Open the repository on GitHub.
2. Open "Data Science Project.ipynb".
3. Open the notebook in Google Colab.
4. Upload or connect to the dataset required by the notebook.
5. Check that the dataset path matches the location used in the code.
6. Run the notebook cells in order.
7. Review the data analysis, model comparison, evaluation results, and prediction section.

⚠️ Important

The notebook may use Google Colab or Google Drive paths. Update the dataset path if necessary before running it in another environment.

🔧 Future Improvements

- Build a simple web application for student score prediction.
- Add more visualizations and analysis.
- Test additional Machine Learning algorithms.
- Improve model performance through hyperparameter tuning.
- Explore additional features that may help explain student performance.

⚠️ Limitations

- Predictions depend on the dataset and the features used.
- Model performance may vary on new data.
- Predicted scores are estimates and should not be treated as guaranteed results.
- The model should support analysis, not determine a student's abilities or future.

👩‍💻 Author

Reena

Data Science Project using Machine Learning.
