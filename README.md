# Telco Customer Churn Prediction using K-Nearest Neighbors (KNN)

## Project Overview

This project uses the K-Nearest Neighbors (KNN) algorithm to predict customer churn in the telecommunications industry. Churn prediction helps businesses understand why customers are leaving and take proactive steps to retain them. The model is trained on customer attributes and contract details from the Telco Customer Churn dataset.

---

## Dataset Information

- **File name**: WA_Fn-UseC_-Telco-Customer-Churn.csv  
- **Target variable**: Churn (1 = Yes, 0 = No)  
- **Number of features**: Multiple categorical and numerical columns including:

  - gender
  - SeniorCitizen
  - Partner
  - Dependents
  - tenure
  - PhoneService
  - InternetService
  - Contract
  - MonthlyCharges
  - TotalCharges
  - PaymentMethod
  - Churn

---

## Data Preprocessing

1. Loaded the dataset using pandas  
2. Checked for missing values using `data.isnull().sum()`  
3. Detected outliers in `MonthlyCharges` using Z-score  
4. Converted categorical columns to numeric using `LabelEncoder`  
5. Split the dataset into features (X) and label (y)

---

## Model Training

- Used K-Nearest Neighbors Classifier from scikit-learn  
- Chose number of neighbors = 150  
- Split the data into training and testing sets (80% train, 20% test)  
- Trained the model using `kn.fit(xtrain, ytrain)`  

---

## Evaluation

- Made predictions using `kn.predict(xtest)`  
- Evaluated the model with the following metrics:

  - **Accuracy Score** using `accuracy_score(ytest, ypred)`
  - **Confusion Matrix** using `confusion_matrix(ytest, ypred)`

---

## Observations

- All categorical columns were successfully encoded
- Large number of neighbors (150) leads to a smoother decision boundary
- Z-score was used to check for outliers but no data points were dropped

---

## Libraries Used

- pandas  
- numpy  
- seaborn  
- scikit-learn  
- scipy (for z-score)

---

## Future Work

- Use GridSearchCV to find the optimal number of neighbors  
- Normalize numeric features with StandardScaler before training  
- Compare performance with other models like Random Forest, SVM, or XGBoost  
- Visualize results with a confusion matrix heatmap  
- Implement cross-validation to improve generalization  

---

## Acknowledgments

- Dataset provided by IBM Sample Datasets  
- Inspired by real-world use cases in telecom customer retention

---

## License

This project is licensed under the MIT License.
