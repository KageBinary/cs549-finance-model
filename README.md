## cs549-finance-model

Finance model project for CS 549. Loads personal transaction data, trains and evaluates models, and produces the figures and metrics in the report.

---

### Environment

- **OS**: Windows 10/11
- **Python**: 3.10+
- **Key packages**: numpy 2.2.6, pandas 2.3.3, scikit-learn 1.7.2, scipy 1.15.3, matplotlib 3.10.8, seaborn 0.13.2, mlxtend 0.23.4, quadprog 0.1.13, torch 2.10.0, JupyterLab 4.5.2

Full dependency list with exact versions is in `requirements.txt`.

---

### Setup

Create and activate a virtual environment, then install dependencies:

```bash
python -m venv .venv
```

Windows:
```bash
.\.venv\Scripts\activate
```

macOS/Linux:
```bash
source .venv/bin/activate
```

```bash
pip install -r requirements.txt
```

---

### Running the Notebook

Place `aug_personal_transactions_with_UserId.csv` in the same directory as the notebook, then launch Jupyter:

```bash
jupyter notebook
```

Open `analysis.ipynb` and run all cells top to bottom. The notebook covers data loading, preprocessing, model training, evaluation, and generates all figures referenced in the report.
