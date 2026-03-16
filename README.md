# 🍷 Wine Quality Neural Network

**Course:** MBA Business Data Analytics — A04  
**Tools:** R · neuralnet · caret · ggplot2  
**Dataset:** Wine quality dataset with physicochemical predictors and quality score outcome

---

## Business Problem

Can wine quality be predicted from measurable chemical properties?  
This project uses a neural network to model nonlinear relationships between physicochemical variables and wine quality, showing how machine learning can support product quality evaluation.

---

## What I Did

**1. Data Preparation**  
- Loaded the wine quality dataset into R
- Reviewed structure, variable types, and summary statistics
- Prepared predictors and outcome for neural network modeling
- Applied scaling/normalization to improve model performance
- Created training and testing workflow for evaluation

**2. Neural Network Model Development**  
- Built a feedforward neural network using the `neuralnet` package
- Used physicochemical input variables to predict wine quality
- Tested hidden-layer structure and model fit
- Evaluated prediction output against observed values

**3. Model Evaluation**  
- Compared predicted vs. actual wine quality values
- Assessed model fit using error-based performance measures
- Interpreted how nonlinear modeling differs from traditional regression

---

## Model Insight

The neural network captured nonlinear relationships among wine attributes that may not be fully represented in standard linear models. This makes neural networks valuable when product quality is influenced by multiple interacting chemical properties.

---

## Business Value

- Demonstrated how machine learning can support product quality prediction
- Showed the usefulness of neural networks for nonlinear business problems
- Highlighted how measurable product attributes can be translated into predictive insight
- Reinforced the role of analytics in quality-focused decision-making

---

## Files

| File | Description |
|---|---|
| `moralesb-A04.Rmd` | Full neural network analysis and model workflow |

---

## Skills Demonstrated

`neuralnet` · Data preprocessing · Feature scaling · Predictive modeling · Nonlinear analysis · Model evaluation · Quality analytics · R Markdown
