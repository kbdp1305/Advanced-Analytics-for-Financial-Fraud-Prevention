
# Risk Transaction Clustering & Anomaly Detection

## Overview
This project performs an end-to-end exploratory data analysis (EDA), anomaly detection, clustering, and strategic decision modeling on bank transaction data to identify and manage high-risk transactions. It balances financial profitability with user experience constraints.

## Dataset Details
The analysis is based on the `bank_transactions_data_2.csv` dataset, containing the following primary features:
* **TransactionID, AccountID, MerchantID:** Identifiers for the transaction entities.
* **TransactionAmount, AccountBalance:** Financial numerical attributes.
* **CustomerAge, CustomerOccupation:** Demographic data.
* **TransactionDuration, LoginAttempts:** Interaction and friction metrics.
* **Channel, Location, IP Address, DeviceID:** Contextual context points.

## Methodology

### 1. Data Preprocessing & Initial Inspection
* **Data Cleaning:** Checking for missing values, confirming data types, and ensuring appropriate formats for further analysis.
* **Feature Engineering:** Log transformations to reduce skewness.

### 2. Exploratory Data Analysis (EDA)
* **Transaction Analysis:** Analyzed raw distributions, log distributions, cumulative distributions (CDF), and detected outliers using the Interquartile Range (IQR) method.

### 3. Machine Learning Models
The notebook applies several unsupervised machine learning techniques to evaluate risks and detect patterns:
* **Isolation Forest:** For anomaly and fraud detection.
* **Clustering Algorithms:** K-Means, DBSCAN, and Gaussian Mixture Models to segment transactions based on features like transaction amount, duration, and account balance.
* **Principal Component Analysis (PCA):** For dimensionality reduction and visualizing clusters.

### 4. Strategic Decision Insight & Profitability Analysis
* Developed a financial recovery vs. intervention cost model.
* **Profit Curve:** Showed that profit is strongly driven by early high-risk segments, but marginal gains decrease as coverage expands.
* **Adjusted Decision Insight:** Pure profit maximization may lead to over-intervention (false positives, user friction). The optimal strategy balances:
  * Maximum financial recovery
  * Efficiency (risk per user)
  * User impact tolerance

## Key Takeaways
> From a purely financial perspective, expanding coverage broadly remains profitable under current assumptions. However, this ignores real-world constraints such as user friction and false positives.
> While broad intervention can maximize financial recovery, the optimal decision must balance **profit, efficiency, and user experience**, rather than relying on a single metric.

## Next Steps
* Introduce more realistic cost modeling:
  * Separate **false positive cost vs true fraud savings**.
* Combine models to form a unified:
  * Profit curve
  * Efficiency curve
  * Decision curve

## Technologies & Libraries Used
* **Python 3.12**
* Data Manipulation: `pandas`, `numpy`
* Visualization: `matplotlib`, `seaborn`
* Machine Learning: `scikit-learn` (`IsolationForest`, `KMeans`, `DBSCAN`, `GaussianMixture`, `PCA`, `LabelEncoder`, `StandardScaler`)

## How to Run
1. Ensure all required libraries are installed (`pip install pandas numpy matplotlib seaborn scikit-learn`).
2. Download the dataset and update the file path in the data loading cell.
3. Execute the notebook sequentially to reproduce the visual insights and clustering models.
README.md

## Author
**Krisna Bayu Dharma Putra**
Email: [dharma.work.dev@gmail.com](mailto:dharma.work.dev@gmail.com)
GitHub: https://github.com/kbdp1305
