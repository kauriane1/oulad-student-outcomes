# Predicting Student Academic Outcomes Using Machine Learning and Deep Learning

## 1. Project Overview

This project uses machine learning and deep learning to predict student academic outcomes using the Open University Learning Analytics Dataset (OULAD).

The goal is to explore whether student demographic information, educational background, and early engagement with online learning activities can help identify students at risk of failing or withdrawing, as well as students likely to pass or achieve distinction.

The project compares traditional machine learning models with neural networks to examine their predictive performance and their potential use in early-warning analytics.

## 2. Problem Statement

Student disengagement and poor academic performance can be difficult to identify early. Predictive models may help educators identify students who could benefit from additional academic support.

This project uses Virtual Learning Environment (VLE) activity from the first 28 days of a course, together with available student information, to predict the final academic outcome.

The target classes are:

- Pass
- Fail
- Withdrawn
- Distinction

## 3. Dataset

The project uses the Open University Learning Analytics Dataset (OULAD).

The dataset contains student demographic information, course registration information, assessment information, and records of student interactions with the online learning platform.

**Dataset source:** https://analyse.kmi.open.ac.uk/open_dataset

The raw dataset is provided separately through the project Google Drive submission. It is not included in this GitHub repository.

## 4. Methodology

The project follows these main steps:

1. Load and inspect the OULAD data.
2. Clean the data and examine missing values and duplicates.
3. Filter VLE activity to the first 28 days.
4. Aggregate early engagement features, including total clicks, mean clicks per interaction, and distinct interaction days.
5. Combine the activity features with student information.
6. Split the data into training, validation, and test sets.
7. Impute missing values, encode categorical features, and scale numerical features where appropriate.
8. Train and compare traditional machine learning and deep learning models.
9. Evaluate model performance using accuracy, macro F1-score, confusion matrices, and multiclass ROC-AUC where computed.
10. Save the selected models and relevant preprocessing artifacts.

The test set is reserved for final evaluation after model selection.

## 5. Models

### Traditional Machine Learning

The experiments include:

- Logistic Regression
- Random Forest
- Tuned Random Forest
- Gradient Boosting

### Deep Learning

The experiments compare neural network architectures with different numbers of hidden layers, dropout configurations, and batch normalization.

TensorBoard is used to track training and validation experiments.

## 6. Evaluation

Models are compared using accuracy and macro F1-score. Additional evaluation methods include confusion matrices, class-level precision and recall, and multiclass ROC-AUC when calculated.

Macro F1-score is particularly useful because the four academic outcome classes are not equally represented in the dataset.

Final reported test results should be taken from the completed notebook and should not be confused with validation results.

## 7. Repository Contents

```text
oulad-student-outcomes/
├── notebook.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

Additional figures or source files may be included if needed. The raw dataset, TensorBoard logs, and saved model artifacts are provided separately in Google Drive.

## 8. Requirements

The project uses Python and the following libraries:

- NumPy
- Pandas
- Scikit-learn
- TensorFlow
- Matplotlib
- Seaborn
- TensorBoard
- Joblib

The exact package versions used in the working Colab environment are listed in `requirements.txt`.

## 9. How to Run the Project

1. Clone or download this repository.
2. Install a compatible Python version.
3. Install the required libraries:

   ```bash
   pip install -r requirements.txt
   ```

4. Download the OULAD dataset from the official source or access the dataset supplied through the project Google Drive.
5. Place the data files in the location expected by the notebook, or update the notebook's data-loading paths.
6. Open `notebook.ipynb` in Google Colab or Jupyter Notebook.
7. Run the notebook cells in order.

For deep learning experiments, use an environment compatible with the TensorFlow version specified in `requirements.txt`.

## 10. Saved Models and Experiment Logs

The Google Drive submission contains the saved model artifacts, including:

- `best_deep_learning_model.keras`
- `best_gradient_boosting_model.joblib`
- `deep_learning_label_encoder.joblib`
- `feature_scaler.joblib`
- `gradient_boosting_full_pipeline.joblib`

The `gradient_boosting_full_pipeline.joblib` artifact includes the fitted preprocessing pipeline and Gradient Boosting classifier, allowing predictions from the original input features.

TensorBoard training and validation logs are also provided separately in Google Drive.

## 11. Limitations

The model's predictions are estimates and should not be treated as definitive judgments about individual students. Student outcomes may be influenced by factors that are not included in the dataset.

The first-28-day activity window supports an early-warning approach, but withdrawal timing and other potential sources of target leakage must be considered when interpreting the results.

The dataset reflects a particular educational context, so results may not generalize to every institution or student population.

## 12. Project Resources

- **GitHub repository:** https://github.com/kauriane1/oulad-student-outcomes
- **Project report:** [Insert your report or Google Drive URL]
- **Dataset and saved models:** [Insert your Google Drive URL]
- **Presentation video:** [Insert your video URL]

## 13. Author

**Auriane KALISA**


Machine Learning and Deep Learning Project