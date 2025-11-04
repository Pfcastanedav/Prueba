# Summary of 2_Xgboost

[<< Go back](../README.md)


## Extreme Gradient Boosting (Xgboost)
- **n_jobs**: -1
- **objective**: binary:logistic
- **eta**: 0.1
- **max_depth**: 7
- **min_child_weight**: 10
- **subsample**: 0.8
- **colsample_bytree**: 0.5
- **eval_metric**: f1
- **explain_level**: 1

## Validation
 - **validation_type**: kfold
 - **k_folds**: 5
 - **shuffle**: True

## Optimized metric
f1

## Training time

189.3 seconds

## Metric details
|           |      score |     threshold |
|:----------|-----------:|--------------:|
| logloss   | 0.00880106 | nan           |
| auc       | 0.999954   | nan           |
| f1        | 0.995956   |   0.68123     |
| accuracy  | 0.996429   |   0.68123     |
| precision | 1          |   0.98815     |
| recall    | 1          |   4.42911e-06 |
| mcc       | 0.992774   |   0.68123     |


## Metric details with threshold from accuracy metric
|           |      score |   threshold |
|:----------|-----------:|------------:|
| logloss   | 0.00880106 |   nan       |
| auc       | 0.999954   |   nan       |
| f1        | 0.995956   |     0.68123 |
| accuracy  | 0.996429   |     0.68123 |
| precision | 0.99905    |     0.68123 |
| recall    | 0.992882   |     0.68123 |
| mcc       | 0.992774   |     0.68123 |


## Confusion matrix (at threshold=0.68123)
|              |   Predicted as 0 |   Predicted as 1 |
|:-------------|-----------------:|-----------------:|
| Labeled as 0 |            37254 |               28 |
| Labeled as 1 |              211 |            29432 |

## Learning curves
![Learning curves](learning_curves.png)

## Permutation-based Importance
![Permutation-based Importance](permutation_importance.png)
## Confusion Matrix

![Confusion Matrix](confusion_matrix.png)


## Normalized Confusion Matrix

![Normalized Confusion Matrix](confusion_matrix_normalized.png)


## ROC Curve

![ROC Curve](roc_curve.png)


## Kolmogorov-Smirnov Statistic

![Kolmogorov-Smirnov Statistic](ks_statistic.png)


## Precision-Recall Curve

![Precision-Recall Curve](precision_recall_curve.png)


## Calibration Curve

![Calibration Curve](calibration_curve_curve.png)


## Cumulative Gains Curve

![Cumulative Gains Curve](cumulative_gains_curve.png)


## Lift Curve

![Lift Curve](lift_curve.png)



[<< Go back](../README.md)
