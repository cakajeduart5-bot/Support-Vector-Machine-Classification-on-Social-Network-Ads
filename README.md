# Support Vector Machine: Iris Flower Classification

A multi-class classification project utilizing Support Vector Machines (SVM) to categorize iris flowers based on sepal and petal dimensions.

---

## Project Overview
This project demonstrates the effectiveness of **Support Vector Machines** in high-dimensional feature spaces. Using the classic Iris dataset, I trained an SVM model with an **RBF kernel**, optimized via **GridSearch**, to achieve a highly accurate classification boundary between three distinct species.

---

## Exploratory Data Analysis
Before modeling, I analyzed the feature distributions to determine the separability of the classes.

### 1. Species Distribution (Pairplot)
![Iris Pairplot](iris_pairplot.png)  
The pairplot reveals that the *Setosa* species is perfectly linearly separable, while *Versicolor* and *Virginica* have slight overlap, requiring a non-linear kernel like RBF for optimal classification.

### 2. Petal vs. Sepal Density
![KDE Plot](setosa_kde.png)  
Focusing on the *Setosa* species, a Kernel Density Estimate (KDE) plot shows a very tight cluster for petal length and width, serving as a primary differentiator for the model.

---

## Model Training & Optimization
I implemented the `SVC` model from Scikit-Learn. To find the optimal hyperparameters, I utilized **GridSearchCV** to tune the `C` (regularization) and `gamma` (kernel coefficient) parameters.

### Model Performance Metrics
The final model was evaluated on a 30% test split, yielding exceptional precision and recall across all categories.

![SVM Report](svm_report.png)

### Confusion Matrix
![Confusion Matrix](svm_confusion_matrix.png)  
The confusion matrix confirms that the model correctly classified nearly every instance, with only minimal confusion between the closely related *Versicolor* and *Virginica* species.

---

## Key Takeaways
* **The Power of Kernels**: The RBF kernel allowed the SVM to create complex, non-linear decision boundaries that a simple linear model would struggle with.
* **Hyperparameter Tuning**: GridSearch proved essential; by testing values for `C` and `gamma`, I was able to find the "sweet spot" that maximized accuracy without overfitting the training data.
* **Linear vs. Non-Linear**: While one species was easily separable, the SVM's margin-based logic was critical for handling the overlapping distributions of the other two species.

---

## How to Run
```bash
pip install pandas seaborn scikit-learn
jupyter notebook "Support Vector Machines Project.ipynb"
