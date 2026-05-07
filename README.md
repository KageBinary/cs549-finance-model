## cs549-finance-model

### Overview

This repository contains code for the **CS 549 Finance Model** project. The code loads financial data, trains and evaluates models, and produces the metrics and figures referenced in the project report.

This README provides:

- **How to run the code**
- **Dependencies and installation**
- **Execution environment used for the report**

You should keep this file up to date if you change any scripts, file names, or dependencies.

---

### Environment

- **Programming language**: Python 3.10+ (project tested with Python 3.10/3.11)
- **Operating system**: Developed and tested on Windows 10 (should also work on macOS/Linux with minor path changes)
- **Package manager**: `pip` (via `python -m pip`) or `conda`
- **Recommended setup**: Isolated virtual environment

To create and activate a virtual environment on Windows:

```bash
python -m venv .venv
.\.venv\Scripts\activate
```

On macOS/Linux:

```bash
python -m venv .venv
source .venv/bin/activate
```

---

### Dependencies

Install all required Python packages using:

```bash
pip install -r requirements.txt
```

Your `requirements.txt` already lists the exact libraries and versions used in this environment (for example, `numpy`, `pandas`, `scikit-learn`, `matplotlib`, `seaborn`, `mlxtend`, `quadprog`, Jupyter-related packages, and supporting utilities).  

If you add new libraries in your scripts or notebooks, remember to also add them to `requirements.txt` so that anyone installing from this file fully reproduces your environment.

---

### Project Structure

The key files in this repository are:

- `analysis.ipynb` – main Jupyter notebook containing the finance model code, analysis, and visualizations referenced in the report  
- `aug_personal_transactions_with_UserId.csv` – primary dataset used by the notebook  
- `report.tex` – LaTeX source for the written report  
- `report.*` – auxiliary files generated when compiling the LaTeX report (e.g., `.aux`, `.log`, `.out`, `.fdb_latexmk`, `.fls`)  
- `REQUIREMENTS.md` – additional documentation about required packages (complements `requirements.txt`)  
- `README.md` – this documentation file

---

### How to Run the Code

1. **Clone the repository**

   ```bash
   git clone <your-repo-url> cs549-finance-model
   cd cs549-finance-model
   ```

2. **Create and activate the virtual environment**

   ```bash
   python -m venv .venv
   .\.venv\Scripts\activate
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Prepare the data**

   - Place your dataset files in the `data/` directory (for example, `data/finance_data.csv`).
   - If your scripts expect different filenames or paths, update them accordingly.

5. **Run the main script**

   From the project root:

   ```bash
   python main.py
   ```

   or, if your entry point has a different name:

   ```bash
   python src/train_model.py
   ```

   The script will typically:

   - Load the dataset(s)
   - Perform preprocessing and feature engineering
   - Train and evaluate the financial model(s)
   - Print metrics to the console and/or save them to `results/`
   - Optionally generate plots and save them under `figures/` or `results/plots/`

6. **Command-line arguments**

   If your code uses command-line arguments, run it with the appropriate options. For example:

   ```bash
   python main.py --config configs/base.yaml --seed 42
   ```

   Check the `argparse` (or equivalent) setup in your code for the full list of options.

---

### Running Notebooks (Optional)

If some or all of your analysis is in Jupyter notebooks (for example, `notebooks/finance_model.ipynb`):

1. Activate your environment:

   ```bash
   .\.venv\Scripts\activate
   ```

2. Start Jupyter:

   ```bash
   jupyter notebook
   ```

3. Open the notebook from the browser and run all cells top to bottom to reproduce the analysis and figures.

---

### Reproducing Report Results

To reproduce the results reported in your project write-up:

1. **Use the same environment**
   - Python 3.10+ and the exact package versions in `requirements.txt`.
2. **Run scripts in the documented order**
   - For example:
     - `python preprocess.py`
     - `python main.py`
     - `python evaluate.py`
3. **Verify outputs**
   - Confirm that metrics in `results/` and plots in `figures/` match those presented in the report (within expected randomness). If your code uses randomness, set a fixed random seed via configuration or command-line arguments.

---

### Troubleshooting

- **Missing package errors**  
  Ensure your virtual environment is activated and re-run:

  ```bash
  pip install -r requirements.txt
  ```

- **Path or file-not-found errors**  
  Make sure you are running commands from the project root and that input data files exist in the expected locations (usually under `data/`).

- **Different results than the report**  
  Check that:
  - You are using the same dataset version.
  - You are using the same configuration/parameters.
  - Your package versions match those in `requirements.txt`.

