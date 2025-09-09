# Decision Tree and Random Forest 
This project uses a dataset to classify breast cancer tumors as malignant or benign using Decision Tree and Random Forest classifiers. The objective is to compare model performance, analyze overfitting, interpret feature importance, and evaluate the models using cross-validation.
##  Dataset Overview

**Attribute information** 

**1) ID number**

**2) Diagnosis** (M = malignant, B = benign)


Ten real-valued features are computed for each cell nucleus:

**a) radius** (mean of distances from center to points on the perimeter)

**b) texture** (standard deviation of gray-scale values)

**c) perimeter**

**d) area**
**e) smoothness** (local variation in radius lengths)

**f) compactness** (perimeter^2 / area - 1.0)

**g) concavity** (severity of concave portions of the contour)

**h) concave point**s (number of concave portions of the contour)

**i) symmetry**

**j) fractal dimension** ("coastline approximation" - 1)

- **Source**: UCI Breast Cancer Wisconsin (Diagnostic) Dataset
- 
- **Shape**: 569 rows × 32 columns
- 
- **Target**: `diagnosis`  
  - `M` (Malignant) → 1  
  - `B` (Benign) → 0
 

##  Technologies Used

- Python
- Scikit-learn
- Pandas
- Matplotlib
- Seaborn

**Conclusion**

**Decision Tree Classifier:**
Achieved 100% training accuracy but around 94.7% test accuracy, indicating overfitting.

Visualization of the tree showed high complexity, and analysis of varying tree depth confirmed that beyond a certain point (depth ~3–5), test accuracy decreases while training accuracy remains perfect.

This demonstrates that without regularization (like depth limitation), Decision Trees can memorize the training data, leading to poor generalization.

**Random Forest Classifier:**

Provided a more balanced performance, with high training accuracy and improved generalization on test data.

It effectively reduces overfitting by averaging multiple decision trees, each trained on different subsets of data.

Feature importance analysis revealed which attributes most strongly influenced the predictions—helping in interpretability and potential feature selection.

**Cross-Validation (planned step):**

Though not executed here due to tool limitations, using cross-validation would further validate the stability of the Random Forest model and ensure its performance is not due to random splits.

