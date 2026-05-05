# CS549 Project Requirements
## Track 1: Financial Transaction Category Classification

**Deadline:** May 8, 2026 11:59pm — NO late submissions accepted

---

## Submission Checklist

- [ ] Final report as PDF (max 13 pages, excluding references/appendices)
- [ ] All code files in a zip (runnable `.py` or `.ipynb` files)
- [ ] README with run instructions and environment info
- [ ] Everything bundled into **one single `.zip` file**

---

## Report Structure (Required Sections)

1. **Title Section** — project title + team member names
2. **Abstract** — objectives, methods, results, conclusions
3. **Introduction** — background on Track 1, dataset overview, project objectives
4. **Related Work** *(optional)* — existing research, how your approach compares
5. **Methodology** — preprocessing steps, model selection/justification, hyperparameter tuning
6. **Results** — evaluation metrics per model, confusion matrices, ROC curves
7. **Discussion** — key findings, comparative analysis, limitations
8. **Conclusion** — outcomes summary, future work
9. **Individual Contributions** — specific tasks per team member
10. **References** — all sources including any GenAI used

---

## Grading Rubric

| Category                   | Weight |
|----------------------------|--------|
| Introduction & Background  | 5%     |
| Data Preprocessing         | 20%    |
| Model Implementation       | 30%    |
| Evaluation & Analysis      | 20%    |
| Report Quality             | 15%    |
| Individual Contributions   | 10%    |

---

## Project Requirements

### 1. Data Preprocessing (address at least 2)
- [ ] Handle missing values
- [ ] Remove duplicate records
- [ ] Feature extraction/encoding (e.g., encode `Category`, parse `Date`, encode `Transaction Type`)
- [ ] Feature scaling (normalize/standardize numerical features like `Amount`)
- [ ] Handle imbalanced data (oversampling, undersampling, SMOTE, etc.)

### 2. Model Development (3–4 models minimum, each member implements at least 1)
- [ ] Model 1: _______________
- [ ] Model 2: _______________
- [ ] Model 3: _______________
- [ ] Model 4: _______________ *(if applicable)*
- [ ] Hyperparameter tuning via cross-validation for each model

Candidate models for classification:
- Logistic Regression
- Random Forest
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- Neural Network / Multi-Layer Perceptron (MLP)

### 3. Model Evaluation
- [ ] Accuracy (overall and per-class)
- [ ] Precision, Recall, F1-Score
- [ ] Runtime analysis
- [ ] Confusion matrix (visualization)
- [ ] ROC curves (if applicable)
- [ ] Comparative analysis of all models

---

## Dataset

**File:** `aug_personal_transactions_with_UserId.csv`

**Columns:** User ID, Date, Description, Amount, Transaction Type, Category, Account Name

**Target variable:** `Category` (multi-class classification)

---

## Formatting

- Font: Times New Roman or similar, 11–12pt
- Margins: 1 inch
- Template: NeurIPS LaTeX format (`report.tex`)
- Max pages: 13 (excluding references and appendices)

---

## Code Requirements

- Python 3
- Well-documented and reproducible
- All external sources and libraries must be cited
- GenAI usage must be disclosed

## Key Libraries (install via pip)
```
pandas
numpy
scikit-learn
matplotlib
seaborn
imbalanced-learn
jupyter
```
