# README: Banking Customer EDA

## Overview
This notebook performs an **Exploratory Data Analysis (EDA)** on a banking customer dataset with 3,000 records and 25 features. The analysis aims to uncover patterns, distributions, and relationships within customer financial data to support business decision-making and risk assessment.

## Dataset Information

- **Number of rows:** 3,000
- **Number of columns:** 25

### Key Features

| Category | Features |
|----------|----------|
| **Demographics** | Client ID, Name, Age, Location ID, Nationality, Occupation |
| **Banking Details** | Joined Bank, Banking Contact, Fee Structure, Loyalty Classification |
| **Financial** | Estimated Income, Superannuation Savings, Credit Card Balance, Bank Loans, Bank Deposits |
| **Accounts** | Checking Accounts, Saving Accounts, Foreign Currency Account, Business Lending |
| **Other** | Properties Owned, Risk Weighting, BRId, GenderId, IAId |

## Analysis Performed

### 1. Data Assessment
- Data shape inspection
- Data types verification (no missing values across all columns)
- Descriptive statistics generation

### 2. Feature Engineering
- Created `Income Band` column:
  - Low: Income < 100,000
  - Med: Income between 100,000 and 300,000
  - High: Income >= 300,000

### 3. Univariate Analysis
- Distribution analysis of categorical variables:
  - BRId, GenderId, IAId, Amount of Credit Cards
  - Nationality, Occupation, Fee Structure
  - Loyalty Classification, Properties Owned, Risk Weighting, Income Band
- Distribution analysis of numerical variables:
  - Estimated Income, Superannuation Savings, Credit Card Balance
  - Bank Loans, Bank Deposits, Checking Accounts
  - Saving Accounts, Foreign Currency Account, Business Lending

### 4. Bivariate Analysis
- Count plots exploring categorical variables with Nationality segmentation
- Histograms for numerical variable distributions

### 5. Correlation Analysis
- Correlation matrix heatmap for numerical features

## Key Insights

### Categorical Distributions
- BRId: Value 3 appears most frequently (1,352 records)
- GenderId: Nearly balanced (1,512 for value 2, 1,488 for value 1)
- Nationality: European dominates (1,309), followed by Asian (754)
- Fee Structure: High (1,476), Mid (962), Low (562)
- Loyalty Classification: Jade (1,331), Silver (767), Gold (585), Platinum (317)
- Income Band: Med (1,517), Low (1,027), High (456)
- Properties Owned: Relatively balanced across 0-3 properties

### Numerical Observations
- Estimated Income: Wide range (15,919 to 522,330)
- Bank Loans & Deposits: Highly variable with some accounts at zero
- Foreign Currency Account: Lower volume compared to other account types

### Correlations
- Strong positive correlations observed among:
  - Bank Deposits ↔ Checking Accounts ↔ Saving Accounts
  - Income ↔ Various financial indicators

## Requirements

```bash
pip install pandas matplotlib seaborn numpy
