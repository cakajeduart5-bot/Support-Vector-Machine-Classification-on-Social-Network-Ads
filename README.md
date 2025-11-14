# Support Vector Machine Classification on Social Network Ads

## Overview
This project applies Support Vector Machines (SVM) to classify whether a user is likely to purchase a product based on social network advertisement data. The goal is to understand how SVMs separate classes using optimal hyperplanes and how kernel functions affect model performance.

## Objectives
- Clean and preprocess a structured advertising dataset.
- Visualize distributions and identify patterns through EDA.
- Train both linear and non-linear SVM models.
- Compare performance using various kernels (linear, RBF, polynomial).
- Evaluate results using confusion matrices and classification metrics.

## Dataset
A synthetic social network advertisement dataset containing:
- Age  
- Estimated Salary  
- Purchased (target label)

## Workflow Summary
1. **Data Loading & Cleaning**  
   - Handle missing values  
   - Format features  

2. **Exploratory Data Analysis**  
   - Scatterplots  
   - Histograms  
   - Correlation insights  

3. **Train-Test Split & Scaling**  
   - StandardScaler applied to numerical features  

4. **Model Training**  
   - Linear SVM  
   - RBF SVM  
   - Polynomial SVM  

5. **Model Evaluation**  
   - Accuracy  
   - F1-score  
   - Confusion Matrix  

## Results
- Kernel SVM (RBF) outperformed linear SVM for non-linear patterns.
- Clear margin boundaries were observed in visualisations post-scaling.
- Classification metrics confirm non-linear decision boundaries are most suitable.

## Technologies Used
- Python  
- NumPy  
- Pandas  
- Matplotlib  
- Seaborn  
- Scikit-Learn  

## How to Run
```bash
pip install -r requirements.txt
jupyter notebook
```

---

*This project was completed as part of the Python for Data Science and Machine Learning Bootcamp course on Udemy.*
