# Diabetes Prediction Model

This project uses machine learning to predict whether a person is diabetic or non-diabetic based on medical attributes. It uses the Pima Indians Diabetes Dataset from Kaggle and applies supervised learning techniques.


## Dataset Details

- **Source:** Kaggle – Pima Indians Diabetes Dataset
- **Features:**
  - `pregnancies`: Number of times pregnant
  - `glucose`: Plasma glucose concentration
  - `diastolic`: Diastolic blood pressure (mm Hg)
  - `triceps`: Skin fold thickness (mm)
  - `insulin`: 2-Hour serum insulin (mu U/ml)
  - `bmi`: Body mass index (weight in kg/(height in m)^2)
  - `dpf`: Diabetes Pedigree Function (genetic risk)
  - `age`: Age in years
  - `diabetes`: Target label (1 = Diabetic, 0 = Non-Diabetic)

## Techniques Used

### Data Preprocessing:
- Removed missing values
- Handled outliers using **IQR capping**
- Standardized features using `StandardScaler`

### Visualization:
- **Boxplots** for outlier detection
- **Heatmap** for correlation analysis
- **3D scatter plot** for visualizing diabetes vs attributes
- **2D scatter plot** for clustering (`glucose` vs `bmi`)

### Unsupervised Learning (Clustering):
- Algorithm: **K-Means (k=2)**
- Scaled features before clustering
- Compared cluster labels with actual diabetes values
- Analyzed cluster centroids

### Supervised Learning (Classification):
- Algorithm: **SVM (Support Vector Machine)**
- Accuracy achieved: **77.76%**
- Target variable: `diabetes`
- Used train-test split and evaluated performance

## Result Summary

- **KMeans Clustering** identified two natural groups of patients
- **SVM classifier** achieved **77.76% accuracy**
- Good separation observed in glucose, BMI, and age for diabetic vs non-diabetic
