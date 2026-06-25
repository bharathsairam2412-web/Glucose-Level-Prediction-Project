# Glucose Level Prediction Project

This project predicts glucose levels and classifies high glucose risk ($\ge 100\text{ mg/dL}$) using clinical and behavioral health features from the Framingham Heart Study dataset. It presents a complete end-to-end machine learning pipeline implemented in Python.

### Key Objectives
* Build predictive classification models to identify patients at risk of elevated glucose levels.
* Analyze behavioral risk factors (smoking, medication) and clinical features (systolic/diastolic blood pressure, heart rate, BMI, total cholesterol) that correlate with elevated glucose.

### Workflow & Implementation
1. **Data Preprocessing & Imputation:** Addressed missing data by imputing continuous variables with their median values and categorical features with their mode.
2. **Feature Engineering:** Converted categorical parameters and utilized dummy variable encoding. Created a binary target variable `High_Glucose` (threshold $\ge 100\text{ mg/dL}$).
3. **Data Scaling:** Applied standard scaling (`StandardScaler`) to features to ensure model convergence.
4. **Model Training & Evaluation:** Split the dataset (80% training, 20% testing) and trained classifiers configured with class balancing (`class_weight='balanced'`) to handle class imbalance:
   * **Logistic Regression:** Achieved ~77% accuracy with balanced sensitivity, suitable as a screening benchmark.
   * **Random Forest Classifier:** Achieved ~92% accuracy with robust performance across metrics.

### Project Structure
* `Glucose_Prediction_Summary_(1).ipynb`: Jupyter Notebook detailing data cleaning, exploration, modeling, and evaluation.
* `framingham.csv`: Source dataset from the Framingham Heart Study.

### Technologies Used
* Python 3
* Pandas & NumPy (Data manipulation)
* Matplotlib & Seaborn (Data visualization)
* Scikit-Learn (Preprocessing, training, and evaluation)
