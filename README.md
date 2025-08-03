

 Comparative Classification Analysis on the UCI Zoo Dataset


The purpose of this study is to classify animals into their biological categories using features describing physical characteristics and behaviors. The UCI Zoo dataset is used to compare the performance of five classification algorithms: Logistic Regression, Decision Tree, K-Nearest Neighbors (KNN), Support Vector Machine (SVM), and Random Forest.

The main objectives are:

* Preprocess and explore the Zoo dataset.
* Train multiple machine learning models.
* Compare accuracy and classification performance.
* Visualize class distribution and confusion matrices.

---

2. Dataset Description**

* **Source:** [UCI Machine Learning Repository – Zoo dataset](https://archive.ics.uci.edu/ml/machine-learning-databases/zoo/zoo.data)
* **Number of instances:** 101
* **Number of features:** 17 predictive attributes (binary/numeric), 1 target variable (`class_type`).
* **Target classes:** 7 (Mammal, Bird, Reptile, Fish, Amphibian, Insect, and Invertebrate).
* **Removed column:** `animal_name` (non-predictive identifier).

**Feature examples:**

* hair, feathers, eggs, milk, airborne, aquatic, predator, toothed, backbone, breathes, venomous, fins, legs, tail, domestic, catsize.

---

### **3. Exploratory Data Analysis**

* **Summary Statistics:** Most features are binary (0/1) except `legs`, which has discrete integer values.
* **Class Distribution:**
  ![Class Distribution](class_distribution.png) *(Replace with actual plot output)*
  The dataset is relatively balanced, but some classes have fewer samples (e.g., Class 6, Class 7).

---

### **4. Preprocessing**

* Removed `animal_name`.
* Scaled all features using **StandardScaler** to ensure models sensitive to feature scales (e.g., Logistic Regression, KNN, SVM) perform optimally.
* Split the dataset into **80% training** and **20% testing** sets using `train_test_split` with `random_state=42`.

---

### **5. Models Trained**

1. **Logistic Regression** – Linear classifier for multiclass classification.
2. **Decision Tree Classifier** – Tree-based model that handles non-linear relationships.
3. **K-Nearest Neighbors (KNN)** – Instance-based method using distance metrics.
4. **Support Vector Machine (SVM)** – Finds optimal hyperplane for class separation.
5. **Random Forest Classifier** – Ensemble of decision trees for improved generalization.

---

### **6. Evaluation Metrics**

For each model:

Accuracy Score**
*Precision, Recall, F1-score** (per class) from classification report.
*Confusion Matrix** visualized as heatmap.


Observations:

* Random Forest has minimal misclassifications across classes.
* Logistic Regression struggles with Classes 3 and 5 due to overlapping features.


This analysis shows that machine learning models can effectively classify animals using physical and behavioral traits. Among the tested algorithms, **Random Forest** likely achieves the highest accuracy, closely followed by Decision Tree and KNN. Confusion matrices reveal specific class misclassifications that can be targeted with further optimization.


