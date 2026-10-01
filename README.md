# Wine Quality Neural Network

**Neural-network regression case study in R for predicting wine quality from physicochemical measurements**

## Executive Summary
This project demonstrates a neural-network workflow for a continuous quality outcome. The original coursework correctly included dummy encoding, train/test partitioning, feature scaling, and reverse-scaling of predictions, but its notebook retained text/code from an unrelated energy-efficiency example and omitted the line that actually trained `wine.model`.

The revised notebook repairs those issues while preserving the analytical approach supported by the coursework.

## Workflow
- Read and clean wine-quality data
- Treat wine color as a categorical feature
- Dummy-encode categorical predictors
- Create a reproducible 70/30 train/test split
- Scale predictors using training-data ranges
- Scale the continuous quality outcome
- Train a single-hidden-layer neural network
- Predict held-out observations
- Reverse-transform predictions to the original quality scale
- Evaluate test MSE, RMSE, MAE, and correlation

## Why Scaling Matters
Neural networks are sensitive to predictor scale. Range scaling keeps features on comparable numerical ranges and can improve optimization stability. Preprocessing is learned from the **training data** and then applied to the test set to reduce leakage.

## Repository Structure
```text
wine-quality-neural-network/
├── README.md
├── analysis/
│   └── wine_quality_neural_network.Rmd
└── requirements_R.txt
```

## Data Note
The source coursework referenced `winequality.xlsx`, but the file was not included in the uploaded repository. The notebook expects it at `data/winequality.xlsx`. No accuracy or error number is claimed until the model is rerun against that source data.

## Interview Talking Point
> I built a neural-network regression workflow for wine quality. I dummy-encoded the categorical color variable, split the data into training and test sets, learned preprocessing from the training set, range-scaled the predictors and target, trained a single-hidden-layer network, and evaluated predictions after transforming them back to the original scale. A key lesson was preventing leakage by fitting preprocessing on training data only.

## Limitations
A stronger production analysis would compare the neural network with simpler baselines, tune network architecture through resampling, assess stability across repeated splits, and document whether the added model complexity creates meaningful predictive improvement.
