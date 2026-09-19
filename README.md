# Industrial-Way-To-Handle-Machine-Learning-Project

## 📌 Overview

This project uses **Machine Learning to classify breast cancer cases** as **Benign** or **Malignant** based on different cell-related features.

The project uses a **Random Forest Classifier** along with a preprocessing pipeline to handle missing values and train the model efficiently.

The complete workflow includes:

* Loading and preparing the dataset
* Converting the raw `.data` file into CSV format
* Handling missing values
* Splitting the dataset into training and testing sets
* Training a Random Forest model
* Making predictions
* Evaluating model performance
* Visualizing feature importance
* Saving and loading the trained model

---

## 🎯 Objective

The main objective of this project is to build a machine learning classification model that can learn patterns from breast cancer data and classify a given case into:

* **2 → Benign**
* **4 → Malignant**

The project is designed as a machine learning practice project to understand the complete ML workflow from **data preprocessing to model evaluation and model persistence**.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas** – Data loading and manipulation
* **NumPy** – Numerical operations
* **Matplotlib** – Data visualization
* **Scikit-learn** – Machine learning and evaluation
* **Joblib** – Saving and loading the trained model

---

## 🤖 Machine Learning Algorithm

### Random Forest Classifier

The project uses a **Random Forest Classifier** with 300 decision trees.

Random Forest combines multiple decision trees to make predictions. It is suitable for classification problems and can capture relationships between different input features.

The model is implemented inside a Scikit-learn `Pipeline` together with missing-value imputation.

---

## 📊 Dataset

The project uses the **Breast Cancer Wisconsin dataset**.

The dataset contains cell-related features such as:

| Feature                  | Description                   |
| ------------------------ | ----------------------------- |
| ClumpThickness           | Clump thickness measurement   |
| UniformityCellSize       | Uniformity of cell size       |
| UniformityCellShape      | Uniformity of cell shape      |
| MarginalAdhesion         | Marginal adhesion measurement |
| SingleEpithelialCellSize | Single epithelial cell size   |
| BareNuclei               | Bare nuclei measurement       |
| BlandChromatin           | Bland chromatin measurement   |
| NormalNucleoli           | Normal nucleoli measurement   |
| Mitoses                  | Mitoses measurement           |
| CancerType               | Target class                  |

The `CodeNumber` column is used as an identifier and is not included as a model feature.

---

## 🔄 Project Workflow

```text
Raw Dataset
     ↓
Load Dataset
     ↓
Add Column Headers
     ↓
Handle Missing Values
     ↓
Convert Features to Numeric
     ↓
Train-Test Split
     ↓
SimpleImputer
     ↓
Random Forest Classifier
     ↓
Model Training
     ↓
Prediction
     ↓
Model Evaluation
     ↓
Feature Importance
     ↓
Save Trained Model
```

---

## 🧹 Data Preprocessing

The dataset may contain missing values represented by `?`.

The project converts these values into `NaN` and uses **SimpleImputer with median strategy** to handle missing values during model training.

This preprocessing step is included inside the machine learning pipeline:

```text
SimpleImputer
      ↓
RandomForestClassifier
```

This keeps preprocessing and model training together in a single pipeline.

---

## 📚 Train-Test Split

The dataset is divided into:

* **70% Training Data**
* **30% Testing Data**

The split uses `stratify` so that the class distribution is maintained between the training and testing datasets.

---

## 📈 Model Evaluation

The trained model is evaluated using:

### Accuracy

Measures the percentage of correctly classified samples.

### Classification Report

Provides:

* Precision
* Recall
* F1-score
* Support

### Confusion Matrix

Shows the number of correctly and incorrectly classified samples for each class.

The project also displays the confusion matrix using Matplotlib.

---

## 🔍 Feature Importance

Random Forest provides feature importance values.

The project visualizes these values to understand which input features contributed more to the model's predictions.

This helps provide a basic understanding of which dataset attributes the trained model considered important.

---

## 💾 Model Saving and Loading

The trained machine learning pipeline is saved using **Joblib**:

```text
bc_rf_pipeline.joblib
```

The saved model can later be loaded and used for predictions without training the model again.

---

## 📁 Project Structure

```text
Breast-Cancer-Classification/
│
├── 47_IndustrialBreastCancer.py
├── breast-cancer-wisconsin.data
├── breast-cancer-wisconsin.csv
├── bc_rf_pipeline.joblib
└── README.md
```

> Keep the dataset and generated model file in the project folder only if you intend to include them in your GitHub repository.

---

## ▶️ How to Run the Project

### 1. Clone the Repository

```bash
git clone <your-github-repository-url>
```

### 2. Navigate to the Project Folder

```bash
cd Breast-Cancer-Classification
```

### 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib scikit-learn joblib
```

### 4. Run the Python Program

```bash
python 47_IndustrialBreastCancer.py
```

The program will:

1. Load the dataset
2. Perform preprocessing
3. Split the data
4. Train the Random Forest model
5. Generate predictions
6. Display evaluation results
7. Display feature importance
8. Save the trained model
9. Load the saved model and test a sample prediction

---

## 📌 Key Features

* Machine Learning classification
* Random Forest algorithm
* Missing-value handling
* Scikit-learn Pipeline
* Train/Test data splitting
* Accuracy evaluation
* Classification report
* Confusion matrix
* Feature importance visualization
* Model saving and loading using Joblib

---

## 🚀 Future Improvements

Possible improvements for this project include:

* Adding a user-friendly web interface
* Comparing multiple classification algorithms
* Hyperparameter tuning
* Adding cross-validation
* Creating interactive visualizations
* Deploying the trained model as a web application

---

## 👩‍💻 Author

**Laxmi Nandkumar Shinde**

Bachelor of Engineering – Information Technology

---

## 📜 Disclaimer

This project is developed for **educational and machine learning practice purposes**. It is not intended to provide medical diagnosis or replace professional medical advice.
