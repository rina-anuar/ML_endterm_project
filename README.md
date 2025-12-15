# Endterm Project: Introduction to Machine Learning [CSCI3237]

## **Overview**

Machine learning classification project focused on wine quality prediction. This project analyzes physicochemical properties of wine to predict quality ratings using various classification and regression techniques.

# Wine Quality Analysis

Wine quality assessment is a critical aspect of the wine industry, traditionally performed by human experts through sensory evaluation. This project leverages machine learning to predict wine quality based on objective physicochemical measurements, providing a data-driven approach to quality assessment.

## Background

Wine quality is influenced by numerous factors including chemical composition, production methods, and storage conditions. By analyzing measurable properties such as acidity, sugar content, and alcohol percentage, we can build predictive models that assist in quality control and production optimization.

## Dataset Features

Our dataset contains the following physicochemical properties:

### Chemical Composition Features

1. **Fixed Acidity** (g/dm³)
   - Non-volatile acids that don't evaporate easily (tartaric acid, malic acid)
   - Contributes to wine's taste and stability

2. **Volatile Acidity** (g/dm³)
   - Amount of acetic acid; high levels can lead to unpleasant vinegar taste
   - Indicator of wine spoilage

3. **Citric Acid** (g/dm³)
   - Adds freshness and flavor to wines
   - Acts as a natural preservative

4. **Residual Sugar** (g/dm³)
   - Sugar remaining after fermentation
   - Determines sweetness level (dry to sweet)

5. **Chlorides** (g/dm³)
   - Salt content in wine
   - Affects taste perception

### Sulfur Compounds

6. **Free Sulfur Dioxide** (mg/dm³)
   - Prevents microbial growth and oxidation
   - Free form of SO₂

7. **Total Sulfur Dioxide** (mg/dm³)
   - Total amount of SO₂ (free + bound forms)
   - Important for wine preservation

### Physical Properties

8. **Density** (g/cm³)
   - Mass per unit volume
   - Related to alcohol and sugar content

9. **pH**
   - Measure of acidity/alkalinity (scale 0-14)
   - Affects taste, color, and microbial stability
   - Most wines range from 3-4 pH

10. **Sulphates** (g/dm³)
    - Wine additive contributing to SO₂ levels
    - Acts as antimicrobial and antioxidant

11. **Alcohol** (% vol)
    - Percentage of alcohol by volume
    - Affects body, taste, and mouthfeel

### Target Variable

12. **Quality** (score)
    - Sensory evaluation score (typically 0-10)
    - Based on expert wine taster assessments

## Applications

This machine learning approach can be used for:
- Quality control in wine production
- Identifying key factors affecting wine quality
- Optimizing fermentation processes
- Predicting market value based on chemical composition
- Assisting winemakers in decision-making
- Standardizing quality assessment procedures

## Important Considerations

Wine quality is subjective and influenced by personal preferences. While physicochemical properties provide objective measurements, human sensory evaluation remains valuable. This model should be used as a complementary tool alongside traditional wine tasting expertise.

<hr />

# Team Members

- **Anuar Rina** - Main Team Leader
- **Li Artur**  - Architecture Designer, Distributor
- **Karim Adiyar** - Model Development
- **Adylkhanov Alisher** - Evaluation & Testing
- **Ulasova Gaukhar** - Data Processing

# Dataset

Description of the dataset used in this project

- **Source**: [Wine Quality Dataset](https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009)
- **Type**: Red Wine / White Wine 
- **Size**: Approximately 1,599 samples (red wine) or 4,898 samples (white wine)
- **Features**: 11 physicochemical properties + 1 quality target variable + ID

### Feature Summary
- **Input Variables**: 11 continuous numerical features
- **Output Variable**: Quality (integer score, typically 3-8)
- **Missing Values**: Dataset is complete with no missing values

<hr />

# Project Structure

- `data/` - Folder containing `.csv` files and wine quality database
- `main/` - Main code execution files
- `notebooks/` - Jupyter notebooks for exploration, documentation, and testing
- `models/` - Trained model files and checkpoints
- `visualizations/` - Generated plots and analysis figures

<hr />

# Prerequisites

- Jupyter Notebooks
- Python 3.10+
- Basic understanding of machine learning concepts
- Familiarity with data analysis libraries

# Installation Setup

```bash
git clone https://github.com/leeaso/endterm_project
cd endterm_project
```

### Initialize Your Own Virtual Environment (Recommended)

```bash
python -m venv venv
```

**Important**: Do not commit your virtual environment to version control.

## To Activate Your Virtual Environment

### MacOS/Linux
```bash
source venv/bin/activate
```
Use `deactivate` in bash to deactivate venv

---

### Windows
```bash
venv\Scripts\activate
```

# Install Dependencies

```bash
pip install -r requirements.txt
```

### Required Libraries
- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
- jupyter
- scipy

---

# Milestones

### 1. Data Preprocessing
- Data loading and initial inspection
- Handling outliers and anomalies
- Feature scaling and normalization
- Train-test-validation split
- Data distribution analysis

### 2. Exploratory Data Analysis (EDA)
- Statistical summary of all features
- Distribution plots and histograms
- Correlation analysis between features
- Quality distribution investigation
- Relationship between chemical properties and quality
- Feature importance preliminary analysis

### 3. Feature Engineering
- Feature selection techniques
- Creating interaction features
- Polynomial features exploration
- Dimensionality reduction (PCA if needed)

### 4. Model Development
- Baseline model establishment
- Multiple algorithm comparison:
  - Linear Regression
  - Logistic Regression
  - Decision Trees
  - Random Forest
  - Support Vector Machines (SVM)
  - Gradient Boosting (XGBoost, LightGBM)
  - Neural Networks (optional)
- Hyperparameter tuning
- Cross-validation

### 5. Evaluation Metrics
- **For Regression Approach**:
  - Mean Squared Error (MSE)
  - Root Mean Squared Error (RMSE)
  - Mean Absolute Error (MAE)
  - R² Score

- **For Classification Approach**:
  - Accuracy
  - Precision
  - Recall
  - F1-Score
  - Confusion Matrix
  - ROC-AUC Curve (if applicable)
  - Class-wise performance analysis

### 6. Model Interpretation
- Feature importance analysis
- SHAP values (optional)
- Error analysis
- Model limitations and biases

### 7. Final Report & Presentation
- Comprehensive documentation
- Results visualization
- Model comparison summary
- Conclusions and recommendations
- Future work suggestions

---

# Methodology

## Approach Options

### Option 1: Regression
Treat quality as a continuous variable (0-10 scale) and use regression algorithms to predict the exact quality score.

### Option 2: Classification
Convert quality scores into categories:
- **Low Quality**: 3-4
- **Medium Quality**: 5-6
- **High Quality**: 7-8

### Option 3: Multi-class Classification
Treat each quality score (3, 4, 5, 6, 7, 8) as a separate class.

---

# Expected Challenges

1. **Class Imbalance**: Quality scores may be concentrated around medium values (5-6)
2. **Feature Correlation**: Some chemical properties may be highly correlated
3. **Subjective Target**: Quality ratings are based on human perception
4. **Limited Features**: Only 11 input features may limit prediction accuracy

---

# References

1. UCI Machine Learning Repository - Wine Quality Dataset

2. Scikit-learn Documentation: https://scikit-learn.org/

---

# License

- No License yet

---

# Acknowledgements

- **Instructor**: Jaylet Oliver
- **Data Source**: UCI Machine Learning Repository / Kaggle

---

**Course**: Introduction to Machine Learning  
**Semester**: Autumn, 2025
**University**: Kazakh-British Technical University

---

## Contact

For questions or collaboration inquiries, please contact team members through university email or GitHub repository issues.

---
# ML_endterm_project
