# CodeAlpha Data Science Internship

A collection of practical data science and machine learning projects completed as part of the **CodeAlpha Data Science Internship**.

This repository showcases the application of Python, data analysis, exploratory data analysis (EDA), supervised machine learning, model evaluation, and analytical problem-solving through two independent projects.

## Internship Projects

| # | Project | Domain | Status |
|---|---|---|---|
| 01 | [Iris Flower Classification](Task_1_Iris_Flower_Classification/) | Machine Learning · Classification | Completed |
| 03 | [Car Price Prediction](Task_3_Car_Price_Prediction_with_Machine_Learning/) | Machine Learning · Regression | Completed |

---

## Project 1: Iris Flower Classification

**Domain:** Supervised Machine Learning · Classification

**Objective:** Develop and evaluate machine learning classification models to predict the species of an Iris flower based on its physical measurements.

### Dataset Overview

- 150 observations
- 4 numerical features:
  - Sepal Length
  - Sepal Width
  - Petal Length
  - Petal Width
- 3 target classes:
  - Iris-setosa
  - Iris-versicolor
  - Iris-virginica

### Methodology

1. Data loading and initial inspection
2. Data quality assessment
3. Exploratory Data Analysis (EDA)
4. Feature preparation and train-test splitting
5. Feature standardization using Scikit-learn pipelines
6. Model training using K-Nearest Neighbors (KNN) and Decision Tree
7. Model evaluation using classification metrics
8. Confusion matrix analysis and model comparison

### Model Performance

| Model | Test Accuracy |
|---|---:|
| K-Nearest Neighbors (KNN) | 93.33% |
| Decision Tree | 93.33% |

Both models correctly classified 28 out of 30 test observations.

Although they achieved identical accuracy, their confusion matrices revealed different classification error patterns, particularly between Iris-versicolor and Iris-virginica.

### Key Learning Outcomes

- Understanding supervised classification problems
- Exploratory analysis of numerical features
- Feature standardization and preprocessing pipelines
- Training and comparing classification algorithms
- Evaluating precision, recall, F1-score, and accuracy
- Interpreting confusion matrices and classification errors

**Project Notebook:** [Iris Flower Classification](Task_1_Iris_Flower_Classification/notebooks/Iris_Flower_Classification.ipynb)

---

## Project 3: Car Price Prediction with Machine Learning

**Domain:** Supervised Machine Learning · Regression

**Objective:** Develop and compare regression models to predict used car selling prices based on relevant vehicle characteristics.

### Dataset Overview

- Original dataset: 301 observations and 9 columns
- Cleaned dataset: 299 observations after removing 2 duplicate records
- Target variable: `Selling_Price`

**Features:**

- `Car_Name`
- `Year`
- `Present_Price`
- `Driven_kms`
- `Fuel_Type`
- `Selling_type`
- `Transmission`
- `Owner`

### Methodology

1. Data loading and initial inspection
2. Data quality assessment and duplicate removal
3. Exploratory Data Analysis (EDA)
4. Feature selection and preparation
5. Numerical scaling and categorical encoding
6. Model development using Scikit-learn pipelines
7. Regression model evaluation using MAE, MSE, RMSE, and R²
8. Five-fold cross-validation
9. Out-of-fold prediction and error analysis
10. Final model comparison and selection

### Machine Learning Algorithms

Four regression algorithms were trained and evaluated:

- Linear Regression
- Decision Tree Regression
- Random Forest Regression
- Gradient Boosting Regression

### Test-Set Model Comparison

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Linear Regression | 1.4725 | 2.5245 | 0.7527 |
| Decision Tree | 1.1048 | 2.0957 | 0.8296 |
| Random Forest | 1.5448 | 3.7864 | 0.4437 |
| Gradient Boosting | 1.1473 | 2.5314 | 0.7514 |

### Cross-Validation Results

| Model | Mean CV RMSE |
|---|---:|
| Random Forest | 1.4850 |
| Gradient Boosting | 1.5746 |
| Linear Regression | 1.6479 |
| Decision Tree | 2.0125 |

### Selected Model: Gradient Boosting Regression

Gradient Boosting was retained as the final model because it offered a reasonable compromise between test-set and cross-validation performance.

Its test-set performance was:

| Evaluation Metric | Result |
|---|---:|
| MAE | 1.1473 |
| MSE | 6.4080 |
| RMSE | 2.5314 |
| R² | 0.7514 |

**Model Selection Considerations:**

- Decision Tree achieved the lowest test-set RMSE.
- Random Forest achieved the lowest mean cross-validation RMSE.
- Gradient Boosting provided a practical compromise between the two evaluation approaches.

The final selection reflects a considered model comparison rather than choosing an algorithm based on a single metric.

### Key Learning Outcomes

- Data cleaning and quality assessment
- Exploratory analysis of numerical and categorical features
- Regression modeling and feature engineering
- Numerical scaling and one-hot encoding
- Scikit-learn pipelines and ColumnTransformer
- Model evaluation using multiple regression metrics
- Cross-validation and out-of-fold predictions
- Prediction error and residual analysis
- Comparing models using test-set and cross-validation performance

**Project Notebook:** [Car Price Prediction](Task_3_Car_Price_Prediction_with_Machine_Learning/notebooks/Car_Price_Prediction.ipynb)

---

## Technologies and Libraries

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Jupyter Notebook | Interactive development and documentation |
| Visual Studio Code | Development environment |
| Pandas | Data manipulation and analysis |
| NumPy | Numerical computing |
| Matplotlib | Data visualization |
| Seaborn | Statistical data visualization |
| Scikit-learn | Machine learning, preprocessing, pipelines, and model evaluation |

---

## Repository Structure

```text
codealpha-data-science-internship/
│
├── Task_1_Iris_Flower_Classification/
│   ├── data/
│   │   └── Iris.csv
│   ├── notebooks/
│   │   └── Iris_Flower_Classification.ipynb
│   └── requirements.txt
│
├── Task_3_Car_Price_Prediction_with_Machine_Learning/
│   ├── data/
│   │   └── car data.csv
│   ├── notebooks/
│   │   └── Car_Price_Prediction.ipynb
│   └── requirements.txt
│
├── .gitignore
└── README.md
```

---

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/FarazIbrahim/codealpha-data-science-internship.git
cd codealpha-data-science-internship
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate the environment:

**Windows (PowerShell):**

```powershell
.venv\Scripts\Activate.ps1
```

**Linux/macOS:**

```bash
source .venv/bin/activate
```

### 3. Install project dependencies

Each project maintains its own `requirements.txt`.

**For Iris Flower Classification:**

```bash
pip install -r Task_1_Iris_Flower_Classification/requirements.txt
```

**For Car Price Prediction:**

```bash
pip install -r Task_3_Car_Price_Prediction_with_Machine_Learning/requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Navigate to the relevant project's `notebooks/` directory and open the notebook.

Execute the cells in order to reproduce the analysis and model results.

---

## Skills Demonstrated

- Python programming for data science
- Data cleaning and preprocessing
- Exploratory Data Analysis (EDA)
- Data visualization and interpretation
- Supervised machine learning
- Classification and regression
- Feature engineering and preprocessing
- Scikit-learn pipelines
- Model evaluation and comparison
- Cross-validation
- Error analysis and analytical interpretation
- Documenting reproducible data science workflows

---

## Acknowledgment

These projects were completed as part of the **CodeAlpha Data Science Internship**, providing practical experience in applying data science and machine learning techniques to analytical problems.

## Author

**Faraz Ibrahim**

Data Science Intern | CodeAlpha