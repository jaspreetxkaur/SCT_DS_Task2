# SCT_DS_Task2 — Titanic EDA

**Objective.** Perform robust data cleaning and exploratory data analysis (EDA) on the Titanic dataset to uncover patterns, relationships, and actionable insights.

## Dataset
- Source: Kaggle Titanic (train.csv). Small and public; stored here as `data/titanic.csv`.
- Columns: Survival (target), Pclass, Sex, Age, SibSp, Parch, Fare, Embarked, etc.

## Cleaning Plan
- Handle missing: `Age` (impute), `Embarked` (mode), `Cabin` (drop or extract deck).
- Drop low-signal: `Ticket` (optional), high-missing `Cabin` (optional).
- Encode: `Sex`, `Embarked`; derive `FamilySize = SibSp + Parch + 1`, `IsAlone`, `Title` from `Name`.

## EDA Checklist
- Univariate: histograms/boxplots for `Age`, `Fare`; bar for `Pclass`, `Sex`, `Embarked`.
- Bivariate: `Survived` vs `Sex`, `Pclass`, `Age` (bins), `Fare` (bins), `FamilySize`.
- Multivariate: correlation heatmap for numeric; grouped bar/stacked bars.
- Key visuals saved to `/visuals`.

## How to run
```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
# open notebooks/eda_titanic.ipynb in Jupyter or upload to Colab



