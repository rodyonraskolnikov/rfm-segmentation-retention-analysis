# 🚕 BiTaksi RFM Segmentation Project

## 1. Objective
Segment 1 000 customers by Recency-Frequency-Monetary (RFM) scoring, identify key segments, and design data-backed marketing actions.

## 2. Dataset
| Column | Description |
|--------|-------------|
| Customer ID | Unique rider ID |
| LastTransactionDate | Last trip date |
| Frequency (Usage in Last 12 Months) | Trips in past year |
| Total Spending (TL) | Spend in past year |

## 3. Method
1. **Calculate Recency** (days since 31-Dec-2024)
2. **Assign R, F, M scores** (quintiles → 1-5)
3. **Create RFM_Score** (`R_Score``F_Score``M_Score`)
4. **Label segments**  
   *Champions, Loyal Big-Spenders, Potential Loyalists, Promising, New Customers, At-Risk*

## 4. Key Findings
| Segment | Users | Revenue (TL) | Rev / User |
|---------|------:|-------------:|-----------:|
| Champions | X | Y | Z |
| Loyal Big-Spenders | … | … | … |
| At-Risk | … | … | … |

<small>(*Full KPI table in the notebook*)</small>

### Behaviour differences  
![Segment comparison](images/segment_metrics.png)

### Highest-value segment  
Champions (≤ 1 % of users) generate ≈ 15 % of revenue.

### Churn-risk segment  
At-Risk (26 % of revenue) haven’t ridden for ~9 months.

## 5. Marketing Recommendations
| Segment | Actions |
|---------|---------|
| **Champions / Loyal Big-Spenders** | VIP tier, milestone rewards, beta access |
| **At-Risk** | ₺200 “We Miss You” credit, win-back email, survey + credit |
| **Emerging (New + Promising + Potential)** | Welcome bonus, ride bundles, referral multipliers, geo-targeted deals (Kadıköy, İzmir, etc.) |

## 6. How to Run
1. Clone repo  
2. `pip install -r requirements.txt`  
3. Open `rfm_analysis.ipynb` and run all cells

## 7. Project Structure
