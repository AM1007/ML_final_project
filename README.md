# ML_final_project

Final project Machine Learning Fundamentals and Applications

[https://www.kaggle.com/competitions/ml-fundamentals-and-applications-2024-10-01](https://www.kaggle.com/competitions/ml-fundamentals-and-applications-2024-10-01)

This anonymized dataset includes a mix of numerical and categorical data points that capture various aspects of customer behavior. The goal is to predict if a customer might leave or continue using the service. The dataset includes details such as demographics, service usage patterns, billing history, and interactions with support services.

### The data is organized into three parts:

Training Set: for teaching the model patterns in the data.
Testing Set: for checking model performance as you build and improve it.
Validation Set: for making final predictions and getting scores on Kaggle.

### The key steps of getting the solution

#### 1. Exploratory Data Analysis (EDA)

- Data loading and initial structure inspection: Loaded training and testing data to explore features and target variable y.
- Identified and separated numerical and categorical features for specific preprocessing.

#### 2. Data Preprocessing

- **Imputation:**
  - For numerical features: Used median imputation to handle missing values.
  - For categorical features: Filled missing values with "missing" as a placeholder.
- **Feature Scaling:**
  - Applied StandardScaler to numerical features for consistent scaling.
- **Categorical Encoding:**
- Used OneHotEncoder for categorical variables to convert categories into numerical format, handling unknown categories by ignoring them.

#### 3. Class Balancing

- Applied **SMOTE (Synthetic Minority Over-sampling Technique)** within the pipeline to balance the class distribution in y, generating synthetic samples for the minority class.

#### 4. Model Selection and Training

- **Pipeline Construction:**
  - Built a comprehensive pipeline (ImbPipeline) integrating preprocessing, SMOTE balancing, and modeling with AdaBoostClassifier.
- **Cross-Validation:**
  - Conducted 5-fold cross-validation with balanced accuracy scoring to ensure the model’s robustness and to address class imbalance.

#### 5. Evaluation and Metrics

- Printed cross-validation scores and calculated the mean balanced accuracy to evaluate model stability and performance.

#### 6. Final Model Training and Prediction

- **Final Model Training:**
  - Trained the model on the entire training dataset for more robust predictions.
- **Prediction and Submission:**
  -Generated predictions for the test set.
  - Created a submission file, submission.csv, containing predicted values of y for each instance in the test dataset, ready for upload to Kaggle.
