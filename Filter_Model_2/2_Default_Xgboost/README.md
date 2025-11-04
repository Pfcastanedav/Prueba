# Summary of 2_Default_Xgboost

[<< Go back](../README.md)


## Extreme Gradient Boosting (Xgboost)
- **n_jobs**: -1
- **objective**: binary:logistic
- **eta**: 0.075
- **max_depth**: 6
- **min_child_weight**: 1
- **subsample**: 1.0
- **colsample_bytree**: 1.0
- **eval_metric**: accuracy
- **explain_level**: 1

## Validation
 - **validation_type**: kfold
 - **k_folds**: 5
 - **shuffle**: True

## Optimized metric
accuracy

## Training time

168.6 seconds

## Metric details
|           |    score |     threshold |
|:----------|---------:|--------------:|
| logloss   | 0.074629 | nan           |
| auc       | 0.99956  | nan           |
| f1        | 0.995584 |   0.635117    |
| accuracy  | 0.9961   |   0.635117    |
| precision | 1        |   0.999233    |
| recall    | 1        |   3.08019e-06 |
| mcc       | 0.992108 |   0.635117    |


## Metric details with threshold from accuracy metric
|           |    score |   threshold |
|:----------|---------:|------------:|
| logloss   | 0.074629 |  nan        |
| auc       | 0.99956  |  nan        |
| f1        | 0.995584 |    0.635117 |
| accuracy  | 0.9961   |    0.635117 |
| precision | 0.998676 |    0.635117 |
| recall    | 0.992511 |    0.635117 |
| mcc       | 0.992108 |    0.635117 |


## Confusion matrix (at threshold=0.635117)
|              |   Predicted as 0 |   Predicted as 1 |
|:-------------|-----------------:|-----------------:|
| Labeled as 0 |            37243 |               39 |
| Labeled as 1 |              222 |            29421 |

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
