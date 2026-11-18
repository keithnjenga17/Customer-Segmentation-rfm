# Dataset Documentation

## 1. Dataset Overview

This project uses the **Online Retail II** dataset obtained from the UCI Machine Learning Repository.

The dataset contains transactional records from a UK-based online retail business covering the period from **1 December 2009 to 9 December 2011**.

It provides information about customer purchases, products, invoices, transaction dates, quantities and prices.

The dataset is used to analyse customer purchasing behaviour and develop customer segments using RFM analysis and K-Means clustering.

## 2. Dataset Source

- **Dataset:** Online Retail II
- **Source:** UCI Machine Learning Repository
- **Original Creator:** Daqing Chen
- **Publication Year:** 2019
- **Licence:** CC BY 4.0

**Official download page:**

https://archive.ics.uci.edu/dataset/502/online+retail+ii

**Dataset DOI:**

https://doi.org/10.24432/C5CG6D

## 3. Download Instructions

The original dataset is not included in this repository because of its file size.

To obtain the dataset:

1. Visit the [UCI Online Retail II dataset page](https://archive.ics.uci.edu/dataset/502/online+retail+ii).
2. Download the dataset files provided on the page.
3. Extract the downloaded files if they are provided in a compressed format.
4. Locate the original Excel workbook containing the transaction records.
5. Place the downloaded workbook in the appropriate project data directory if you are reproducing the original data preparation workflow.

**Note:** The segmentation notebooks use the cleaned transaction dataset generated during the data preparation stage of the related customer churn project. If you are running the segmentation project independently, you will need to reproduce that cleaning process before generating the RFM dataset.

## 4. Data Preparation

The original transaction data was cleaned before being used for customer analysis.

The preparation process included:

- Combining transaction records from the two worksheets.
- Removing duplicate records.
- Excluding transactions without valid customer identifiers.
- Removing cancelled transactions.
- Excluding invalid quantities and unit prices.
- Calculating transaction revenue.

The resulting cleaned transaction dataset was used to calculate customer-level Recency, Frequency and Monetary metrics.

## 5. Files Generated During the Project

The following datasets are generated throughout the segmentation workflow:

| File | Description |
|---|---|
| `purchase_clean.csv` | Cleaned transaction-level dataset used to calculate RFM metrics |
| `rfm.csv` | Customer-level dataset containing Recency, Frequency and Monetary values |
| `rfm_scaled.csv` | Standardised RFM features used for K-Means clustering |
| `customer_segments.csv` | Final customer-level dataset containing assigned segments and recommended actions |

These files are generated during the project workflow and are not part of the original UCI dataset.

## 6. Dataset Attribution

Chen, D. (2019). Online Retail II [Dataset]. UCI Machine Learning Repository.

https://doi.org/10.24432/C5CG6D

The dataset is distributed under the Creative Commons Attribution 4.0 International (CC BY 4.0) licence.

