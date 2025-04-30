# Bank Transaction Fraud Detection

A machine learning project that uses clustering techniques to detect potentially fraudulent banking transactions.

## Project Overview

This project implements an unsupervised machine learning approach to identify unusual patterns in banking transactions that may indicate fraudulent activities. Using clustering algorithms, the system groups similar transactions and highlights outliers that deviate significantly from normal transaction patterns.

## Dataset

The dataset contains banking transaction records with the following key features:
- Transaction amount
- Transaction type (Credit/Debit)
- Location
- Channel (Branch, Online, Mobile)
- Customer demographics (Age, Occupation)
- Transaction details (Duration, Login attempts)
- Account balance
- Various derived features (Transaction gap, IP usage, etc.)

## Methodology

The project follows these key steps:
1. **Exploratory Data Analysis (EDA)** - Understanding the distribution and relationships between variables
2. **Feature Engineering** - Creating new features such as:
   - Transaction gap dates
   - Device and IP usage patterns
   - Amount ratio (transaction amount to account balance)
   - Merchant preferences
3. **Data Preprocessing** - Encoding categorical variables, scaling numerical features
4. **Clustering** - Using K-means algorithm to group similar transactions
5. **Anomaly Detection** - Identifying potential frauds as outliers or members of suspicious clusters

## Key Findings

- **Three distinct transaction clusters** were identified with different risk profiles:
  - **Cluster 1**: Low fraud risk - Small transaction amounts, low amount-to-balance ratios
  - **Cluster 2**: High fraud risk - Large transaction amounts, very high amount-to-balance ratios
  - **Cluster 3**: Medium fraud risk - Moderate-to-high transaction amounts with reasonable ratios

- **Potential fraud indicators** include:
  - Unusually high transaction amounts
  - High transaction amount to account balance ratios
  - Unusual IP or device usage patterns
  - Suspicious transaction durations

## Files

- `[Clustering] Submission Akhir BMLP_Filza Rahma Muflihah_Bank Transaction.ipynb`: Jupyter notebook containing the complete analysis
- `bank transaction segmentation.csv`: Processed data with cluster assignments

## Usage

1. Clone this repository
2. Install the required dependencies:
   ```
   pip install pandas numpy matplotlib seaborn scikit-learn yellowbrick
   ```
3. Run the Jupyter notebook to see the complete analysis

## Future Work

- Implement real-time fraud detection system
- Incorporate supervised learning with labeled fraud data
- Develop an alert system for potentially fraudulent transactions
- Explore additional features for improved fraud detection
