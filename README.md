# OOB Score Demo using Random Forest

This project demonstrates the concept of **Out-of-Bag (OOB) score** using a **Random Forest Classifier**.  
OOB score is used to estimate the model’s accuracy **without using a separate test dataset**.

---

## What is OOB Score?

When training a Random Forest:
- Each tree is trained on a bootstrap sample of the data
- Some samples are left out (called **Out-of-Bag samples**)
- These OOB samples are used to evaluate the model internally

This makes OOB score a useful alternative to train-test split or cross-validation.

---

## Project Workflow

- Load dataset
- Perform basic preprocessing
- Train Random Forest Classifier with `oob_score=True`
- Compare:
  - Training accuracy
  - Test accuracy
  - OOB score
- Analyze how well OOB score estimates model performance

---

## Algorithms Used

- Random Forest Classifier

---

## Libraries Used

- Python
- NumPy
- Pandas
- Scikit-learn
- Matplotlib (optional for visualization)

---

## Key Learning Outcomes

- Understanding Out-of-Bag sampling
- How Random Forest evaluates unseen data internally
- Difference between OOB score and test accuracy
- Why OOB score is useful for ensemble models

---

## Use Case

This project is helpful for:
- Learning ensemble methods
- Understanding model evaluation techniques
- Avoiding overfitting in Random Forest models
