# Student Dropout Prediction — XGBoost vs Neural Network

An applied supervised-learning project for identifying students at risk of dropout across multiple stages of academic progression.

## Business problem

Early identification of dropout risk can help educational institutions prioritize student support, allocate resources, and design targeted retention interventions.

The project asks two practical questions:

1. How accurately can dropout risk be predicted at different stages of a student's progression?
2. How do a tree-based ensemble model and a neural network compare on discrimination and dropout-case detection?

## Machine-learning workflow

- Data inspection and quality checks
- Missing-data treatment
- Feature engineering, including age derived from date of birth
- Ordinal, binary, and one-hot encoding
- Train / validation / test partitioning
- XGBoost baseline and hyperparameter tuning
- MLP baseline and hyperparameter tuning
- StandardScaler fitted on training data for the neural network
- Accuracy, precision, recall, F1 and ROC-AUC comparison
- Feature-importance and loss-curve analysis

## Key results

| Stage | Model | Accuracy | Precision | Recall | F1 | ROC-AUC |
|---|---|---:|---:|---:|---:|---:|
| 1 | Tuned XGBoost | 0.8935 | 0.6830 | 0.5393 | 0.6027 | 0.8838 |
| 1 | Tuned Neural Network | 0.8899 | 0.6707 | 0.5206 | 0.5862 | 0.7378 |
| 2 | Tuned XGBoost | 0.8994 | 0.7079 | 0.5235 | 0.6019 | 0.9002 |
| 2 | Tuned Neural Network | 0.8974 | 0.6563 | 0.6163 | 0.6357 | 0.8763 |
| 3 | **Tuned XGBoost** | **0.9761** | **0.9338** | **0.8989** | **0.9160** | **0.9926** |
| 3 | Tuned Neural Network | 0.9710 | 0.9188 | 0.8781 | 0.8980 | 0.9854 |

### Main finding

**Tuned XGBoost at Stage 3 was the strongest overall model**, reaching 97.61% accuracy and 0.9926 ROC-AUC.

The analysis also reveals an important operational trade-off: later-stage data produces much stronger predictions, but earlier predictions give institutions more time to intervene. A real early-warning system should therefore optimize not only predictive performance, but also intervention timing and the cost of missed at-risk students.

## Responsible deployment considerations

Before operational use, this project should be extended with:

- probability calibration and decision-threshold analysis,
- subgroup/fairness evaluation,
- temporal or cohort-based validation,
- leakage checks,
- explainability for student-support teams,
- governance around sensitive student information.

The model should support human intervention decisions rather than automatically determine student outcomes.

## Repository structure

```text
student-dropout-prediction-ml/
├── README.md
├── requirements.txt
├── notebooks/
│   └── student_dropout_prediction.ipynb
├── docs/
│   └── PROJECT_NOTES.md
└── reports/
```

## Tech stack

Python · Pandas · NumPy · Scikit-learn · XGBoost · TensorFlow/Keras · Matplotlib · Seaborn

## Skills demonstrated

`Supervised Learning` · `Classification` · `XGBoost` · `Neural Networks` ·
`Feature Engineering` · `Hyperparameter Tuning` · `Model Evaluation` ·
`Data Leakage Prevention` · `Predictive Analytics` · `Responsible AI`
