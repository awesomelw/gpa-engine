# GPA Prediction Engine

A notebook-based machine learning project for predicting student GPA from semester-level academic and demographic data.

The project walks through data loading, exploratory analysis, cleaning, feature engineering, model training, time-aware validation, tuning, and model explanation. The final workflow uses tree-based modeling with a temporal train/test split so the evaluation better reflects how the model would perform on future semesters.

## Files

- `GPA Engine.ipynb` - main notebook with the full analysis and modeling workflow.
- `my_data.csv` - local dataset used by the notebook.
- `.gitignore` - keeps local environment files such as `.venv/` out of Git.

## What It Does

- Cleans unrealistic GPA and study-hour values.
- Explores GPA trends by semester, major, tutoring status, and other student attributes.
- Builds a prediction model using engineered features from the student records.
- Uses `TimeSeriesSplit` for fairer validation on time-ordered semester data.
- Includes model explainability with SHAP so the strongest prediction drivers are easier to interpret.

## Setup

Create and activate a virtual environment:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

Install the main notebook dependencies:

```powershell
python -m pip install pandas numpy matplotlib seaborn scipy scikit-learn xgboost shap ipykernel
```

Then open `GPA Engine.ipynb` in VS Code or Jupyter and select the `.venv` interpreter.

## Notes

The dataset is large and expected to stay local. If you move or rename `my_data.csv`, update the data-loading cell in the notebook before running it.
