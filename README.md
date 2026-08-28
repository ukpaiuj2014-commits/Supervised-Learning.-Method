# Student Dropout Prediction

Machine-learning project for identifying students at risk of academic withdrawal so that institutions can prioritize early support and intervention.

## Project objective

Student attrition can have academic, financial and social consequences for both students and institutions. The objective of this project is to build and compare supervised machine-learning models that can identify patterns associated with dropout risk.

The project evaluates:

- XGBoost
- Multi-Layer Perceptron (MLP)
- Baseline supervised-learning approaches
- Feature engineering and class-imbalance handling
- Hyperparameter tuning
- Classification-model evaluation

## Why this problem matters

A useful early-warning model should do more than maximize overall accuracy. It should help identify high-risk students early enough for support teams to act, while making the limitations of the prediction clear.

Potential applications include:

- Early-warning systems
- Targeted student support
- Retention planning
- Academic-risk monitoring
- Data-informed intervention design

## Workflow

1. Data inspection and quality checks
2. Exploratory data analysis
3. Categorical encoding and numerical preprocessing
4. Feature engineering
5. Class-imbalance handling
6. Train/validation/test splitting
7. Baseline model development
8. XGBoost modelling
9. Neural-network comparison
10. Hyperparameter tuning
11. Evaluation using classification metrics
12. Interpretation of findings and limitations

## Models

### XGBoost

XGBoost was used as the main tree-based ensemble model because it performs strongly on structured/tabular data and can capture nonlinear relationships and interactions between predictors.

### Multi-Layer Perceptron

A neural-network model was developed as a comparison to the tree-based approach.

## Reported results

The current project record reports:

- **ROC-AUC: 0.99**
- **Accuracy: 97.6%**

These figures should be reproduced directly from the final held-out evaluation before being presented as production performance.

> Important: strong evaluation scores do not automatically imply that a model is ready for deployment. Leakage, class balance, temporal validity, fairness and calibration should be checked before operational use.

## Evaluation principles

For a student-risk model, useful evaluation should include more than accuracy:

- ROC-AUC
- Precision
- Recall
- F1-score
- Confusion matrix
- Class-specific error analysis
- Calibration where probabilities are used for intervention prioritisation

Recall is particularly important when the cost of failing to identify an at-risk student is high.

## Responsible-use considerations

A student-dropout model should support human decision-making, not replace it.

Before operational deployment, the system should be reviewed for:

- Bias across demographic or socioeconomic groups
- Data leakage
- Over-reliance on protected or sensitive attributes
- Probability calibration
- False-positive and false-negative consequences
- Explainability for support teams
- Appropriate governance and access controls

## Tech stack

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- TensorFlow / Keras
- Matplotlib
- Seaborn
- Jupyter Notebook

## Repository structure

```text
student-dropout-prediction-ml/
├── README.md
├── requirements.txt
├── data/
│   └── README.md
├── notebooks/
│   └── README.md
├── reports/
│   └── figures/
└── docs/
    └── MIGRATION_GUIDE.md
```

## Recommended visuals for the README

When the notebook is cleaned, export and add:

1. Target/class distribution
2. Confusion matrix for the final model
3. ROC curve
4. Feature-importance or SHAP summary plot
5. Training/validation learning curve for the MLP if available

## Future development

- Reproduce all final metrics from a clean held-out test set
- Add probability calibration
- Add SHAP-based explainability
- Add fairness checks across relevant student groups
- Package preprocessing and model inference into a reproducible pipeline
- Add automated tests for preprocessing and inference
- Build a lightweight demonstration interface only after the model pipeline is validated

## Skills demonstrated

`Classification` · `XGBoost` · `Neural Networks` · `Feature Engineering` ·
`Class Imbalance` · `Hyperparameter Tuning` · `Model Evaluation` ·
`Responsible AI` · `Python`
