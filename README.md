# Binary_classification_transactions

## Overview
This repository contains code and documentation for the model selection process and data preparation conducted for a machine learning project. The project aimed to classify instances using decision trees, logistic regression, and XGBoost models with as a target variable the 'transactions' and the other columns for learning the function that maps them to the transaction. Below, you'll find details on the libraries used, usage instructions, model selection rationale, data preparation steps, and evaluation metrics.

## File Structure 
- `Newdata-2.npy`: Excel file with all the ratings.
- `README.md`: This file providing an overview of the project.
- `requirements.txt`: Text file listing all the required dependencies for the project.
- `main.npy`: Main file to run.

## Libraries Used
Ensure you have the following libraries installed to run the code:
- pandas
- matplotlib
- seaborn
- numpy
- scipy
- imbalanced-learn
- xgboost
- optuna
- scikit-learn

## Usage
1. Clone the repository to your local machine: `git clone https://github.com/spirostefos/Binary_classification_transactions.git`
2. Navigate to the project directory: `cd Binary_classification_transactions`
3. Install the required dependencies: `pip install -r requirements.txt`
4. Run the main script to execute the project: `python main.py`
5. Execute the code cells in your preferred environment, ensuring the dataset is accessible.
6. Follow the provided code comments for each step, including data preprocessing, model training, evaluation, and visualization.
7. Experiment with different hyperparameters, architectures, and optimization techniques as described in the code.
8. Utilize the provided evaluation functions to assess the performance of the models, including ROC curves, classification reports, confusion matrices, etc.



## Model Selection

### Decision Trees (Baseline)
Decision trees were chosen as the baseline model due to their simplicity and interpretability. They require minimal data preparation and are suitable for handling larger datasets efficiently.

### Logistic Regression
Logistic regression was selected for its suitability in binary classification tasks and provision of probabilistic outputs. Despite being computationally efficient, it was sensitive to unbalanced datasets.

### XGBoost
XGBoost, employing gradient boosting, was chosen for its ability to improve overall accuracy by combining weaker models. It provides valuable feature importance insights and employs regularization techniques to prevent overfitting.

## Data Preparation

### Feature Engineering
- **Categorical Variable Conversion**: Non-numeric variables were encoded using Label Encoding.
- **Outlier Handling**: Z-score transformation was applied to reduce outliers.
- **Imbalanced Dataset Treatment**: Oversampling techniques were employed to address class imbalance.

## Model Training

### Hyperparameter Tuning
- **Decision Trees**: No hyperparameter tuning was performed for the baseline model.
- **Logistic Regression**: Hyperparameters were tuned using GridSearchCV method.
- **XGBoost**: Hyperparameters were optimized using the Optuna framework.

## Evaluation Metrics

### Results and Discussion

#### Model Performance
- XGBoost exhibited the highest F1 score among the baseline models, indicating better generalization.
- Logistic regression, despite tuning, showed comparable performance to the baseline model.

#### Feature Importance
Feature importance analysis provided insights into significant features, aiding in model interpretation and decision-making.

