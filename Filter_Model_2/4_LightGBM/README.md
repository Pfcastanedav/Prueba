# Summary of 4_LightGBM

[<< Go back](../README.md)


## LightGBM
- **n_jobs**: -1
- **objective**: binary
- **num_leaves**: 31
- **learning_rate**: 0.05
- **feature_fraction**: 0.9
- **bagging_fraction**: 0.9
- **min_data_in_leaf**: 10
- **metric**: custom
- **custom_eval_metric_name**: accuracy
- **explain_level**: 1

## Validation
 - **validation_type**: kfold
 - **k_folds**: 5
 - **shuffle**: True

## Optimized metric
accuracy

## Training time

68.8 seconds

## Metric details
|           |     score |     threshold |
|:----------|----------:|--------------:|
| logloss   | 0.0327974 | nan           |
| auc       | 0.999922  | nan           |
| f1        | 0.996227  |   0.731332    |
| accuracy  | 0.996668  |   0.731332    |
| precision | 1         |   0.958866    |
| recall    | 1         |   0.000571302 |
| mcc       | 0.993259  |   0.731332    |


## Metric details with threshold from accuracy metric
|           |     score |   threshold |
|:----------|----------:|------------:|
| logloss   | 0.0327974 |  nan        |
| auc       | 0.999922  |  nan        |
| f1        | 0.996227  |    0.731332 |
| accuracy  | 0.996668  |    0.731332 |
| precision | 0.999321  |    0.731332 |
| recall    | 0.993152  |    0.731332 |
| mcc       | 0.993259  |    0.731332 |


## Confusion matrix (at threshold=0.731332)
|              |   Predicted as 0 |   Predicted as 1 |
|:-------------|-----------------:|-----------------:|
| Labeled as 0 |            37262 |               20 |
| Labeled as 1 |              203 |            29440 |

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
