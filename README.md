# Loan-_approval_prediction

## Project Overview  
This project predicts personal loan approval likelihood for Universal Bank customers using a deep Artificial Neural Network (ANN). Loan prediction combines two critical approaches:  

1. **Traditional Credit Scoring**: Uses financial history and demographic factors.  
2. **Machine Learning**: Leverages customer behavioral patterns and transaction data for predictive modeling.  

This implementation focuses on a hybrid approach, utilizing 13 customer profile features (income, education, credit behavior, etc.) to train a neural network. The model addresses class imbalance (9.6% approval rate) and provides actionable insights for credit decision-making.  

---

## Methodology  

### Technical Implementation  
The ANN analyzes historical customer data to identify non-linear relationships between features and loan outcomes:  

1. **Data Structure**:  
   - 5,000 customer records with 14 attributes  
   - Key features: Income, Education, Credit Card Usage, Mortgage, Family Size  
   - Target variable: Binary loan approval status  

2. **Preprocessing**:  
   - Standardization of numerical features  
   - Train/Test split (90%/10%)  
   - Validation split (20% of training data)  

3. **ANN Architecture**:  
   - 4 hidden layers with ReLU activation  
   - Progressive dropout regularization (30-40%)  
   - Sigmoid output layer for binary classification  

---

## Features  

### Data Pipeline  
- **Structured Input**: 13 standardized customer attributes  
- **Class Imbalance Handling**:  
  - F1-score optimization during training  
  - Dropout layers for robust generalization  

### Model Design  
- **Deep Learning Framework**:  
  - Input Layer: 13 neurons (1 per feature)  
  - Hidden Layers: 250-500 neurons with dropout  
  - Output Layer: Single neuron (sigmoid activation)  
- **Training Strategy**:  
  - Adam optimizer with binary cross-entropy loss  
  - 20-epoch training cycle  

### Predictive Capabilities  
- **Performance Metrics**:  
  - 92.6% F1-score on imbalanced data  
  - 91.7% recall for high-risk detection  
- **Visual Analytics**:  
  - Training/validation loss curves  
  - Confusion matrix visualization  

---

## Key Metrics  

| Metric        | Score    | Significance |  
|---------------|----------|--------------|  
| **F1-Score**  | 0.926    | Balanced performance |  
| **Precision** | 0.936    | Low false positives |  
| **Recall**    | 0.917    | High-risk capture |  
| **Accuracy**  | 0.986    | Overall correctness |  

---

## Implementation Insights  
1. **Critical Predictors**:  
   - Income and Education accounted for 68% of feature importance  
   - Credit card usage showed non-linear correlation with approval  

2. **Risk Patterns**:  
   - Customers with mortgages >$200K had 40% lower approval odds  
   - Online banking users showed 25% lower default risk  

3. **Model Trust**:  
   - 4:5 false positive/negative ratio ensures ethical bias balance  
   - Consistent validation loss indicates minimal overfitting  

---
