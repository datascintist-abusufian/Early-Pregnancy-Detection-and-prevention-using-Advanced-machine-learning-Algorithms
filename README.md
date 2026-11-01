# Early Pregnancy Loss Prediction Using Machine Learning

This project predicts early pregnancy loss from demographic, obstetric, anthropometric and biochemical factors, with a focus on vitamin D deficiency. It compares classical, ensemble and deep-learning models, then checks them on larger and simulated datasets.

## Data

| File | Description |
| --- | --- |
| `VitaminD.xlsx` | Case-control study of vitamin D status and early pregnancy loss: 68 coded records, Rangpur Medical College & Hospital, Bangladesh, Feb 2023 to Feb 2024. Informed consent and IRB clearance were obtained, as described in the dataset documentation |
| `large_dataset_Diagnosis.csv` | Larger dataset with the same variable structure, used for scaling experiments |
| `simulated_patient_data.csv` | Simulated patient records for the federated-learning validation |
| `large_clinical_validation_textual_dataset.xlsx` | Textual clinical data for the sentiment and NLP analysis |

Full details are in `Proper Dataset Documentation_Pregnancy loss prediction.pdf`.

> **Data sharing.** `VitaminD.xlsx` is shared with the permission of the study team. Records are coded (study ID only) and contain no names, contact details or hospital record numbers.

## Notebooks

| Notebook | Purpose |
| --- | --- |
| `Early pregnancy loss demonstrations.ipynb`, `Early Pregnancy loss_2.ipynb` | Deep neural network, class rebalancing (ADASYN), XGBoost tuning, and SHAP and LIME explanations |
| `Early_pregnancy_loss_demonstrations_sufi_small_dataset.ipynb` | The same pipeline on the original study data |
| `Early_pregnancy_loss_demonstrations_deep learning model_large_dataset.ipynb` | Deep-learning model on the larger dataset, with cross-validation |
| `Multilayer perception model_*.ipynb` | Multilayer perceptron models on both datasets |
| `Hyperparameter_with_small_dataset_old_model (2).ipynb` | Tuning across five baseline classifiers |
| `Pregnancy_software_large dataset.ipynb` | LASSO feature selection, then LightGBM, CatBoost, stacking and voting ensembles |
| `Clinical_Validation_Early_pregnancy_.ipynb` | Simulated federated learning: partitioning, local training and aggregation |
| `Sentiment_Analysis_large_textual_dataset.ipynb` | NLP sentiment analysis of the textual clinical data (spaCy, TextBlob) |
| `Distribution_and_Frequency_on_small_dataset.ipynb` | Descriptive distributions |

## Running it

```bash
pip install pandas numpy scikit-learn imbalanced-learn xgboost lightgbm catboost tensorflow shap lime spacy textblob
```

The notebooks were written in Google Colab and read from `/content/`. Change these paths to run them locally.

## Licence

No licence has been declared yet. The clinical study data remain the property of the original study team.

## Author

Md Abu Sufian - ORCID [0009-0007-3503-6942](https://orcid.org/0009-0007-3503-6942)
