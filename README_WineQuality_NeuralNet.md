# 🍷 Wine Quality Prediction — Neural Network Regression

**Course:** MBA Business Data Analytics — A04  
**Tools:** R · neuralnet · caret · dummy variables · min-max scaling  
**Dataset:** UCI Wine Quality (red + white wine, chemical properties → quality score)

---

## Business Problem

Can a neural network predict wine quality scores from measurable chemical properties like acidity, sulfur dioxide, alcohol content, and pH? This type of model supports quality control decisions in food and beverage manufacturing.

---

## What I Did

**1. Data Preparation**  
- Read wine quality dataset; created dummy variables for `color` (red/white) using `dummyVars()`
- 70/30 train/test split with stratified sampling via `createDataPartition()`

**2. Feature Scaling**  
Applied min-max normalization using `caret::preProcess(method = "range")` to training and test sets. Scaling is critical for neural networks — unscaled features cause gradient saturation and prevent convergence.

**3. Neural Network Training**  
- Used `neuralnet` package with single hidden layer
- Built formula programmatically with `as.formula(paste(...))`
- Trained on scaled features → scaled quality output

**4. Prediction & Evaluation**  
- Applied `compute()` on scaled test features
- Reverse-scaled predictions back to original quality units using min-max ranges
- Evaluated with Mean Squared Error (MSE) on unscaled outputs

---

## Key Concepts Demonstrated

**Why scale?** Without normalization, variables with large ranges (e.g., total sulfur dioxide: 0–289) dominate gradient updates, and the network stalls before converging. Scaling forces all inputs to [0,1], allowing the optimizer to treat each feature equally.

**Why activation functions?** Without them, stacking layers is mathematically equivalent to a single linear model. Non-linear activation functions allow the network to learn curved decision boundaries — essential for complex data like wine quality.

---

## Files

| File | Description |
|---|---|
| `Moralesb-A04.Rmd` | Complete neural network pipeline with commentary |

---

## Skills Demonstrated

`neuralnet` · `caret` · Min-max scaling · Dummy variable encoding · `createDataPartition` · `compute()` · Reverse scaling · MSE evaluation · Feature engineering
