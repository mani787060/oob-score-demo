# 🌳 Out-of-Bag (OOB) Score Demo using Random Forest

A beginner-friendly Machine Learning project demonstrating how the **Out-of-Bag (OOB) Score** works in a **Random Forest Classifier** using the **Heart Disease UCI Dataset**.

Unlike traditional evaluation methods that require a separate validation set, the OOB Score provides an internal estimate of model performance by utilizing samples that were not selected during bootstrap sampling.

---

## 📌 Project Objective

The primary goal of this project is to understand:

- What Out-of-Bag (OOB) Score is
- How bootstrap sampling works in Random Forest
- How OOB samples are used for internal validation
- Difference between OOB Score and Test Accuracy
- When OOB Score can replace a validation set

---

## 📂 Dataset

**Dataset:** `heart_disease_uci.csv`

The dataset contains patient medical information used to predict the presence of heart disease.

Typical features include:

- Age
- Sex
- Chest Pain Type
- Resting Blood Pressure
- Cholesterol
- Maximum Heart Rate
- Exercise Induced Angina
- ST Depression
- Major Vessels
- Thalassemia
- Target (Heart Disease)

---

## 🌲 What is Out-of-Bag (OOB) Score?

Random Forest trains multiple Decision Trees using **Bootstrap Sampling**.

During bootstrap sampling:

- Random samples are selected **with replacement**
- Approximately **63%** of the training samples are used to train each tree
- The remaining **37%** are left out

These left-out samples are called **Out-of-Bag (OOB) Samples**.

Instead of wasting these unused samples, Random Forest predicts them and computes an internal accuracy known as the **OOB Score**.

This makes OOB Score an efficient alternative to a separate validation dataset.

---

## 🔄 Project Workflow

1. Load the Heart Disease dataset
2. Perform data preprocessing
3. Split features and target
4. Train a Random Forest Classifier
5. Enable:

```python
oob_score=True
```

6. Calculate

- Training Accuracy
- Testing Accuracy
- OOB Score

7. Compare all evaluation metrics

8. Analyze model performance

---

## 🛠 Technologies Used

- Python
- NumPy
- Pandas
- Scikit-learn
- Matplotlib

---

## 📊 Model Used

- Random Forest Classifier

Important parameters:

- `n_estimators`
- `bootstrap=True`
- `oob_score=True`
- `random_state`

---

## 📈 Evaluation Metrics

The project compares:

- ✅ Training Accuracy
- ✅ Testing Accuracy
- ✅ Out-of-Bag (OOB) Score

This comparison helps understand whether the model is:

- Overfitting
- Generalizing well
- Reliably evaluated using OOB samples

---

## 🎯 Key Learnings

After completing this project, you will understand:

- Bootstrap Sampling
- Bagging
- Ensemble Learning
- Out-of-Bag Validation
- Internal Model Evaluation
- Random Forest Training Process
- Difference between OOB Score and Test Accuracy

---

## 💡 Why OOB Score Matters

Advantages:

- No separate validation set required
- Efficient use of training data
- Fast model evaluation
- Built-in validation for Random Forest
- Helps detect overfitting

Limitations:

- Available only for bootstrap-based ensemble methods
- May differ slightly from an independent test set

---

## 📁 Project Structure

```
OOB-Score-Demo/
│
├── heart_disease_uci.csv
├── OOB Score Demo.ipynb
├── README.md
└── requirements.txt
```

---

## 🚀 Future Improvements

- Hyperparameter tuning
- Compare OOB Score with Cross Validation
- Feature Importance Visualization
- Confusion Matrix
- ROC-AUC Curve
- Precision-Recall Analysis

---

## 📚 References

- Scikit-learn Documentation
- Random Forest by Leo Breiman
- UCI Heart Disease Dataset
