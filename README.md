# Pima Indians Diabetes — analysis notebook

## What's in this folder

| File | What it is |
|---|---|
| `pima_analysis.ipynb` | **The analysis. Open this one.** |
| `pina-indians-cleaned-v2.csv` | The data the notebook reads (729 rows × 9 columns) |
| `glucose_vs_outcome.png` | The chart produced in section 6 |
| `requirements.txt` | The Python packages needed to run the notebook |

## To just read it

Open `pima_analysis.ipynb` in JupyterLab, VS Code, or at <https://nbviewer.org>.
Every code cell has saved output, and the chart is embedded as an image, so the whole
analysis is readable without running anything or installing anything.

## To actually run it

1. **Keep the CSV in the same folder as the notebook.** The notebook reads it by relative
   filename, so moving it elsewhere causes a `FileNotFoundError`.
2. Install the packages:
   ```bash
   pip install -r requirements.txt
   ```
3. Open the notebook and choose a Python kernel that has those packages. The notebook
   stores a kernel name, so you may be asked to pick one — any Python 3 environment with
   pandas, matplotlib, scikit-learn and scipy will do.
4. Run all cells.

Running it also rewrites `glucose_vs_outcome.png` in this folder. That is expected.

## One thing to be careful about

The CSV filename is spelled **`pina-indians-cleaned-v2.csv`** — "pina", not "pima". That
misspelling is deliberate: the notebook reads that exact name, so **renaming the file will
break the notebook**.

## What the notebook covers

1. Load the cleaned dataset
2. Total rows and columns
3. Column types and completeness
4. Summary statistics
5. Two different summaries — counts by BMI band × outcome, and mean/median by outcome
6. A simple linear regression with Glucose as the predictor and Outcome as the target,
   with a bar chart of the observed diabetes rate per glucose band and the fitted line

`requirements.txt` lists the exact package versions that were used.
