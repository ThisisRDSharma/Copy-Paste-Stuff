Here’s a more detailed **ROC Threshold RAG Classification with Monitoring Frequency & Escalation Plan** in a structured table format.  

---

### **Fraud Model ROC Threshold, Frequency, and Escalation Plan**  

| **RAG Status** | **ROC Threshold (AUC %)** | **Monitoring Frequency** | **Action Plan** | **Escalation Plan** |  
|--------------|------------------------|------------------|--------------|----------------|  
| ✅ **Green**   | **> 85%**  | **Quarterly** | - Continue monitoring model performance.  <br>- Track key fraud KPIs.  <br>- No intervention required unless declining trend observed. | - No escalation required. <br>- Regular model review by **Modelling Team** & **Fraud Risk Analysts**. |  
| ⚠️ **Amber**   | **70% - 85%**  | **Monthly** | - Investigate feature drift and performance degradation. <br>- Conduct model recalibration with new data. <br>- Adjust fraud detection thresholds if necessary. <br>- Increase monitoring of false positives/negatives. | - **Level 1:** Notify **Modelling Team** and **Fraud Risk Manager**. <br>- **Level 2:** If performance remains in Amber for 2 consecutive months, escalate to **Head of Risk & Fraud Team**. <br>- **Level 3:** If performance drops toward 70% threshold, initiate **model retraining or replacement assessment**. |  
| 🔴 **Red**   | **< 70%**  | **Bi-Weekly** | - Conduct immediate root cause analysis. <br>- Identify data drift, feature quality issues, or model deterioration. <br>- Implement emergency fraud detection measures (rule-based alerts, manual reviews). <br>- Start model retraining with latest data. | - **Level 1:** Immediate alert to **Modelling Team, Fraud Risk Manager & Compliance Team**. <br>- **Level 2:** If ROC remains <70% for **4 weeks**, escalate to **Head of Fraud & Senior Management**. <br>- **Level 3:** If no improvement in 8 weeks, **escalate to Regulatory & Compliance Authorities** (if required). <br>- **Final Step:** Deploy backup fraud models while retraining or replacing the underperforming model. |  

---

### **Key Takeaways:**
- **Green Models** are reviewed quarterly with no escalation unless a negative trend is detected.  
- **Amber Models** require **monthly** review, and if underperformance persists, escalation moves to **senior risk leaders**.  
- **Red Models** are checked **bi-weekly**, with a rapid escalation plan involving senior management, compliance, and potential regulatory action.  

Would you like to incorporate any specific KPIs or additional risk thresholds in the plan?
