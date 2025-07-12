# 📊 Telco Customer Churn Prediction using K-Nearest Neighbors (KNN)

## 📌 Project Overview

This project uses the **K-Nearest Neighbors (KNN)** algorithm to predict customer churn in the telecom industry.  
It helps companies identify which customers are likely to leave and take actions to improve customer retention.

---

## 📁 Dataset Information

- **📄 File name**: `WA_Fn-UseC_-Telco-Customer-Churn.csv`  
- **🎯 Target variable**: `Churn` (1 = Yes, 0 = No)  
- **🔢 Features** include:

  - `gender`
  - `SeniorCitizen`
  - `Partner`
  - `Dependents`
  - `tenure`
  - `PhoneService`
  - `InternetService`
  - `Contract`
  - `MonthlyCharges`
  - `TotalCharges`
  - `PaymentMethod`
  - `Churn`

---

## 🧹 Data Preprocessing

1. ✅ Loaded dataset using `pandas`  
2. 🔍 Checked data types and missing values  
3. ⚠️ Detected outliers in `MonthlyCharges` using **Z-score**  
4. 🔁 Encoded categorical variables with `LabelEncoder`  
5. 📤 Split the data into `X` (features) and `y` (labels)

---

## 🛠️ Model Training

- 🧠 Model: **KNeighborsClassifier** from `scikit-learn`  
- 🔢 Neighbors (`k`): 150  
- 📊 Data Split: 80% training and 20% testing  
- ✅ Trained using `kn.fit(xtrain, ytrain)`

---

## 📈 Evaluation

- 📍 Predictions made with `kn.predict(xtest)`  
- 🧮 Evaluated using:

  - `accuracy_score(ytest, ypred)` ✔️  
  - `confusion_matrix(ytest, ypred)` 🔲  

---

## 📌 Key Observations

- 🧾 All object-type columns were successfully label encoded  
- 🧍‍♂️ A large number of neighbors (k = 150) makes predictions smoother but less sensitive  
- ⚠️ Outliers detected but not removed (could affect results)

---

## 🧰 Libraries Used

- `pandas` 🐼  
- `numpy` 🔢  
- `seaborn` 📊  
- `scikit-learn` 🤖  
- `scipy.stats` 📏

---

## 🚀 Future Improvements

- 🔍 Tune `k` with **GridSearchCV**  
- ⚖️ Scale features using `StandardScaler` for better KNN results  
- 🔁 Try other models: Random Forest, SVM, XGBoost  
- 📊 Visualize confusion matrix using Seaborn  
- 🔄 Use cross-validation for robust accuracy

---

## 🙏 Acknowledgments

- 📂 Dataset from IBM Sample Datasets  
- 💡 Inspired by telecom churn prediction use-cases

---

## 📜 License

This project is licensed under the **MIT License** ✅
