In fraud detection, the threshold levels used in model validation depend on the specific goals of the fraud detection system (e.g., minimizing false positives, maximizing fraud detection rate) and the business context (e.g., cost of fraud, customer experience). These thresholds are typically applied to scores or outputs from machine learning models, and they help decide whether a transaction, account, or action is classified as fraudulent or not. Here are the common threshold levels used in industry for fraud model validation:

### 1. **False Positive Rate (FPR) and False Negative Rate (FNR)**:
   - **False Positive Rate (FPR)**: The proportion of non-fraudulent cases incorrectly labeled as fraud.
   - **False Negative Rate (FNR)**: The proportion of fraudulent cases incorrectly labeled as non-fraud.

   In industry, there is usually a balance sought between these two rates. A typical threshold might be:
   - **FPR**: < 5% (depending on business requirements, this could vary).
   - **FNR**: Ideally, < 1% for high-accuracy fraud detection.

   These thresholds are used to fine-tune fraud models and adjust decision thresholds to balance detection with minimizing disruption to legitimate customers.

### 2. **Precision and Recall**:
   - **Precision** (Positive Predictive Value): The proportion of flagged fraudulent cases that are truly fraudulent.
   - **Recall** (True Positive Rate): The proportion of actual fraudulent cases that are correctly identified by the model.

   In fraud detection, **precision** is often prioritized to avoid inconveniencing legitimate users. Common thresholds might be:
   - **Precision**: > 90% (or > 95% for high-stakes environments like banking).
   - **Recall**: > 80% to 90% for fraud models, but this depends on whether minimizing false negatives (missing fraudulent cases) is more important than minimizing false positives (incorrectly flagging legitimate transactions).

### 3. **Area Under the ROC Curve (AUC-ROC)**:
   - **AUC-ROC** (Area Under the Receiver Operating Characteristic Curve) is a measure of a model’s ability to distinguish between classes (fraud vs. non-fraud).
   - In practice, an AUC score of **0.80–0.90** is considered good for fraud detection models, while a score **above 0.90** is considered excellent.

   A threshold of **0.85 or higher** is often used as a benchmark for acceptable model performance.

### 4. **F1 Score**:
   The **F1 Score** is the harmonic mean of precision and recall. A balance between these metrics is important when both false positives and false negatives are costly.
   - **Threshold for F1 Score**: Industry benchmarks vary, but a score above **0.80** is often considered acceptable, depending on business goals.

### 5. **Confusion Matrix**:
   The confusion matrix is used to assess the classification performance by comparing actual versus predicted fraud cases. Key metrics derived from the confusion matrix include:
   - **True Positives (TP)**: Correctly identified fraud cases.
   - **True Negatives (TN)**: Correctly identified non-fraud cases.
   - **False Positives (FP)**: Legitimate cases incorrectly flagged as fraud.
   - **False Negatives (FN)**: Fraudulent cases missed by the model.
   
   Common thresholds for evaluation:
   - **Accuracy**: While not always the best metric for fraud detection, an accuracy of **> 90%** is generally acceptable in many fraud detection systems, but this depends on the class imbalance (fraud is often rare).
   - **TP > 80%**: Identifying fraud cases is a key priority.

### 6. **Cost-based Thresholds (Business Impact)**:
   Many fraud detection models are fine-tuned with **business costs** in mind, meaning the thresholds are based on the expected **cost of fraud** and the **cost of false positives**.
   - The **cost of fraud** can include financial losses and brand reputation damage.
   - The **cost of false positives** includes operational costs, customer inconvenience, and customer churn.
   
   These thresholds depend on the risk appetite of the business and can vary significantly across industries (e.g., e-commerce, banking, insurance).

### 7. **Operational Thresholds**:
   - **Transaction Limits**: For certain fraud detection systems, a threshold might be based on the monetary amount of a transaction. For example, transactions above **$1000** might be flagged for manual review, or for higher-risk regions, fraud detection models may use **dynamic thresholds** based on behavior or user risk profiles.
   - **Risk Scores**: Many fraud detection models generate a "risk score," and a threshold (e.g., **0.7** or **70%)** might be set to flag a transaction as potentially fraudulent.

### 8. **Time-based Thresholds**:
   - Some systems set thresholds based on **time windows**, such as how quickly multiple transactions occur in a given period, e.g., flagging a user who makes 5 transactions in 5 minutes above a certain dollar amount.
   
### Example: Threshold Selection for a Fraud Model
- **Precision**: 95%
- **Recall**: 85%
- **F1 Score**: 0.90
- **AUC**: 0.88
- **False Positive Rate**: <5%
- **False Negative Rate**: <1%

**Application of thresholds**: 
- If fraud detection is for a bank, the threshold might be set higher on **precision** to avoid flagging too many legitimate transactions, while being flexible on **recall** to ensure that most fraud is detected.
- For an e-commerce platform, where customer inconvenience is more costly than missing a few fraudulent orders, the emphasis might be on higher **recall** to catch more fraud, even if it means some legitimate transactions are flagged for review.

### Conclusion
Thresholds in fraud detection models are set based on the desired balance between detecting fraud and minimizing customer inconvenience. Key metrics include precision, recall, F1 score, and AUC, but business-specific thresholds (like the cost of fraud vs. operational costs) are also highly relevant.




No, we are not making any changes in the Log as this document include production level changes for enhancement in functionality done so far. On other hand, MRM/Model document change log includes information on updates have been made based on findings shared by reviewer into the document.












