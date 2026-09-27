# ICE Task 2: Introduction to Linear Regression for Medical Aid Cost Prediction

Student: Sifiso Mahlangu

## Overview

ICE Task 2 submission. A notebook that loads the Medical Cost Personal Dataset,
explores it, preprocesses it, and trains a Linear Regression model in scikit-learn
to predict medical insurance `charges` from a client's age, sex, BMI, number of
children, smoking status and region.

## Files

| File | Description |
|---|---|
| `ICE_Task2_Medical_Insurance_LinearRegression.ipynb` | The full notebook: all ten tasks, with Markdown explanations, EDA visualisations, preprocessing, model training, predictions, evaluation and the reflection discussion. Fully executed, outputs included. |
| `insurance.csv` | The dataset used (Medical Cost Personal Dataset, 1,338 rows, 7 columns). |
| `build_notebook.py` | The script that generates the notebook programmatically (kept for reproducibility; not required for grading). |

## Dataset

Source: [Kaggle - Medical Cost Personal Dataset](https://www.kaggle.com/datasets/mirichoi0218/insurance)
(`mirichoi0218/insurance`), obtained via its public CSV mirror.

| Feature | Description |
|---|---|
| age | Age of the client |
| sex | Gender of the client |
| bmi | Body Mass Index |
| children | Number of dependants |
| smoker | Smoking status |
| region | Geographic region |
| charges | Medical insurance cost (target variable) |

## How to run

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook ICE_Task2_Medical_Insurance_LinearRegression.ipynb
```

Run all cells top to bottom. `random_state=42` is fixed throughout, so the train/test
split, model coefficients and evaluation metrics will reproduce exactly.

## Summary of results

- Trained a Linear Regression model on an 80/20 train/test split (1,069 training rows,
  268 test rows, after removing one exact duplicate record).
- Test-set performance: MAE = $4,177.05, RMSE = $5,956.34, R2 = 0.807 (the model
  explains about 81% of the variance in charges).
- Smoking status is the strongest single driver of charges (smokers average roughly
  four times the charges of non-smokers), followed by age and BMI, with a pronounced
  smoker x BMI interaction. Full discussion is in the notebook's Task 10 reflection.

## Rubric coverage

| Task | Marks | Covered |
|---|---|---|
| 1. Import Required Libraries | 10 | Yes |
| 2. Load and Explore the Dataset | 15 | Yes |
| 3. Exploratory Data Analysis | 20 | Yes |
| 4. Data Preprocessing | 15 | Yes |
| 5. Define Features and Target Variable | 10 | Yes |
| 6. Split Dataset into Training and Testing Sets | 10 | Yes |
| 7. Train Linear Regression Model | 10 | Yes |
| 8. Make Predictions | 5 | Yes |
| 9. Evaluate Model Performance | 5 | Yes |
| 10. Reflection | 5 | Yes |
| Markdown explanations throughout | 10 | Yes |
