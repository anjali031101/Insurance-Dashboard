
# Insurance-Dashboard

![Insurance Dashboard](https://raw.githubusercontent.com/anjali031101/Insurance-Dashboard/main/Screenshot%202025-11-20%20034029.png)

## Problem Statement

- The purpose of this dashboard is to help Trust Era Insurance Pvt. Ltd. understand its customers, policies, and claim patterns more effectively.

The dashboard highlights:

  * How many customers are active vs. inactive
  * Which policy types bring in the highest premium
  * How claim amounts vary by customer age group
  * How many claims are pending, settled, or rejected
  * Overall performance in terms of premium, coverage, and claim amounts

These insights enable the company to strengthen customer retention, optimize underwriting decisions, and focus on areas needing improvement (for example, high pending claims or inactive users).


### Steps followed

Step 1: Loaded data into Power BI using a SQL Server (Import Query).

Step 2: Enabled Column Quality, Column Distribution, and Column Profile in Power Query.

Step 3: Enabled profiling on the entire dataset.

Step 4: Checked for null values and errors.

Step 5: Verified and corrected the data types of all columns.

Step 6: Applied a dark theme for a clean, professional look.

Step 7: Added slicers for PolicyNumber, ClaimNumber, CustomerID.

Step 8: Added KPI cards for Premium Amount, Coverage Amount, Claim Amount.

Step 9: Added gender tiles for Male and Female customer counts.

Step 10: Added a bar chart showing Number of Claims by Claim Status.

Step 11: Added the following visuals

a) Premium Amount by Policy Type

b) Claim Amount by Age Group – required a conditional column:

Age Group Conditional Column (Power Query)

Condition 1: Age ≤ 24 → Young Adult

Condition 2: Age ≤ 60 → Adult

Else: Elder

c) Active vs Inactive Users

Created using:

Condition: PolicyEndDate < Today’s Date → Inactive

Else: Active

(Note: Today’s Date in Power Query uses DateTime.Date(DateTime.LocalNow()))

Policy Type vs Claim Status Table (Pending, Rejected, Settled, Total)

Step 16: Inserted text boxes for company name and tagline.

Step 17: Added Row-Level Security (RLS) roles for restricted data access.

![Insurance Dashboard](./Screenshot%202025-11-20%20091247.png)


Step 18: Added a Drillthrough page for detailed policy analysis.

## Insights

A single-page report was created in Power BI Desktop and published to Power BI Service.

1. Customer Overview

Total customers: ~10,004

Female: 5,001

Male: 5,003

The customer base is almost evenly split.

2. Active vs Inactive Users

Active: ~5.82K

Inactive: ~4.19K

A high inactive count indicates scope for renewal and retention initiatives.

3. Key Financial Metrics

Total Premium Amount: 5.98M

Total Coverage Amount: 600.55M

Total Claim Amount: 16.91M

Coverage is much higher than premium, so claim trends are crucial to monitor.

4. Premium by Policy Type

Travel: ~2.5M

Health: ~1.2M

Auto: ~1.0M

Life: ~0.7M

Home: ~0.6M

Travel has the highest premium contribution.

5. Claim Amount by Age Group

Adult: 8.6M

Elder: 6.4M

Young Adult: 1.9M

Older age groups have higher claim amounts.

6. Claims by Status

Rejected: ~4.4K

Settled: ~3.4K

Pending: ~2.3K

Pending claims should be monitored for faster processing.

7. Policy Type vs Claim Status Table

Shows claim distribution across policy types, helping identify categories with high rejections or pending cases.
