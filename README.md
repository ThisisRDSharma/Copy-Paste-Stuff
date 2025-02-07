The choice of a **quarterly review frequency** for **Account False Positive Ratio (AFPR)**, which is the ratio of false positives to true positives, is based on both **statistical stability** and **operational efficiency**. Below is the **technical rationale** behind this decision:  

### **1. Statistical Stability & Variance Control**
- **AFPR fluctuates over short periods**: Since AFPR depends on the number of false positives and true positives, a **shorter monitoring window (e.g., monthly or bi-weekly)** may introduce **high variance** due to sudden shifts in fraud patterns, rule updates, or operational changes.  
- **Quarterly aggregation smooths out noise**: By analyzing AFPR over a longer period, the impact of short-term anomalies is reduced, leading to a **more reliable trend analysis**.

### **2. Sample Size & Data Sufficiency**
- **Fraud cases are relatively rare events**: In cases where fraud volume is low, shorter time windows may not capture enough fraud instances, leading to an unreliable AFPR calculation.  
- **Quarterly intervals ensure meaningful volume**: More data points in a quarter allow for a robust estimation of AFPR, reducing potential bias from low sample sizes.

### **3. Operational Impact & Investigation Load**
- **High false positives = investigation fatigue**: Frequent monitoring (e.g., bi-weekly) might create unnecessary operational burden by triggering too many interventions without clear trends.  
- **Quarterly review supports strategic tuning**: Instead of reacting to short-term fluctuations, fraud teams can **identify consistent patterns** and make more **impactful model adjustments**.

### **4. Model Performance Trends & Adjustments**
- **Fraud models take time to learn & adjust**: Sudden changes in AFPR may not always indicate actual model degradation but rather temporary shifts in fraud behavior.  
- **Quarterly evaluation ensures meaningful insights**: Longer monitoring periods help in assessing the impact of previous model changes and whether recalibration is needed.

### **Conclusion**
The quarterly frequency for AFPR is a **balance between statistical accuracy, operational feasibility, and meaningful trend analysis**. It ensures **stable evaluation** while avoiding overreactions to short-term volatility. However, if AFPR is observed to be deteriorating significantly, an **ad-hoc deep dive** or **monthly monitoring** might be warranted.
