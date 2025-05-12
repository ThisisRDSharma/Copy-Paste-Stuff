Commentary on Thresholding Approach for Fraud Model Monitoring
In monitoring the performance of our fraud detection model, one of the key metrics we evaluate is the monthly count of True Positives (TPR)—that is, the number of fraudulent transactions correctly identified by the model and confirmed as fraud through downstream disposition.

🔹 Context and Metric Characteristics
Across historical data, we observe that the number of TPRs per month ranges between 25 and 55.

However, the denominator—total number of transactions per month—ranges between 85,000 and 95,000, with an average of ~88,000 and a standard deviation of ~3,000.

This results in a TPR rate of approximately 0.049%, a value so small that rate-based thresholds (e.g., percentage thresholds) become impractical and overly sensitive to minor fluctuations in volume.

🔹 Thresholding Methodology
Given the above, we propose a volume-adjusted absolute thresholding framework for ongoing performance monitoring:

Volume Banding:
We define the expected operational range of monthly transaction volume using ±1.5 standard deviations from the historical mean.

Expected range: 85,000 to 91,000 transactions/month

This band captures ~87% of the expected distribution under normal operating conditions.

Absolute TPR Thresholds (Business-Driven):
For months where the transaction count lies within the above volume band, we evaluate the model's TPR using absolute counts, not rates. This simplifies interpretation and avoids instability from very low base rate calculations.

Based on historical patterns and business input, we define the thresholds as:

Green: ≤ 200 TPRs (within normal range)

Amber: 201–400 TPRs (moderate increase, warrants attention)

Red: > 400 TPRs (significant spike, investigate immediately)

🔹 Justification for the Approach
Practicality: Rate-based metrics are unreliable in this context due to the extremely low fraud base rate. An increase from 0.045% to 0.055% may appear statistically large, but in absolute terms, it could be driven by just a handful of cases.

Business-Driven, Not Arbitrary: While the thresholds are not derived from statistical confidence intervals, they are informed by a clear understanding of historical volumes, observed TPR ranges, and operational risk appetite.

Clarity for Stakeholders: Using absolute TPR counts offers a more intuitive and actionable monitoring framework, especially for business teams and operational reviewers.


## This is just a sample sheet nothing to do with actual numbers of EWB. Reason for sharing sheet is to check the formulas I have used such that you can use the same in EWB's environment. Please dont attempt to take this sheet in EWB. OPen in EWB to refer to the formula and replicate same formula and structure in your EWB sheet.


## Intentinally I have not written the write metric we are finding but just to illustrate

Monitoring Approval/Decline Rates
In monitoring the model's output over time, particularly approval and decline rates, it is critical that the thresholding approach is not only statistically sound but also balanced and interpretable across both metrics.

🔹 Limitations of Percentage Deviation Approach
Using a percentage deviation from the baseline presents significant challenges due to the asymmetry in baseline proportions:

Baseline approval rate: ~85%

Baseline decline rate: ~15%

Applying a ±25% deviation tolerance:

Approval: ±25% of 85% → green zone range becomes 64% to 106%

Decline: ±25% of 15% → green zone becomes 11% to 19%

This results in:

A disproportionately large acceptable range for approvals.

A narrow, highly sensitive band for declines.

An overall imbalance, making the thresholds inconsistent and hard to interpret jointly.

🔹 Rationale for Standard Deviation-Based Approach
To address this imbalance, we propose using a standard deviation-based thresholding framework. This method:

Sets green/amber/red thresholds around the baseline based on actual distributional variability, not fixed percentages.

Applies the same statistical principle to both approval and decline rates.

Ensures that the sum of approval and decline rates across thresholds logically adds up to 100%, maintaining interpretational consistency.

## Now this one is for model where we can only track success and declined transactions

NOTE: See before 6:30 today, I am not asking to work on any new but to complete the thresholds basis the logic shared above and share the sheet before 6



