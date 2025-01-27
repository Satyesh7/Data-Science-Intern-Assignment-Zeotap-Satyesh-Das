# Data-Science-Intern-Assignment-Zeotap-Satyesh-Das

# Customer Segmentation Project Documentation

## 1. Project Overview

*Purpose:* This project aims to segment customers based on their purchasing behavior and demographic information. The segmentation will help in understanding customer preferences and tailoring marketing efforts for better results.

*Key Features:*

* *Data Loading and Preprocessing:* Loads customer and transaction data from CSV files, handles missing values, and prepares data for analysis.
* *Feature Engineering:* Creates aggregated features like total_spent and total_transactions from transaction data.
* *Feature Encoding and Scaling:* Encodes categorical features (e.g., Region) using Label Encoding and scales numerical features using StandardScaler.
* *Clustering:* Uses KMeans clustering algorithm to segment customers into distinct groups.
* *Optimal Cluster Determination:* Employs the Davies-Bouldin index to determine the optimal number of clusters.
* *Visualization:* Generates scatter plots to visualize the resulting customer segments.

*Supported Platforms/Requirements:*

* Python 3.x
* Libraries: pandas, numpy, scikit-learn (StandardScaler, LabelEncoder, KMeans), matplotlib, seaborn


## 2. Getting Started

*Installation:*

Ensure you have Python 3.x installed.  Install the necessary libraries using pip:

bash
pip install pandas numpy scikit-learn matplotlib seaborn


*Dependencies:*

* pandas for data manipulation
* numpy for numerical operations
* scikit-learn for data preprocessing and clustering
* matplotlib and seaborn for data visualization

You will also need two CSV files named Customers.csv and Transactions.csv in the same directory as the Jupyter Notebook.  The structure of these files is not explicitly defined in the provided codebase, but it's assumed they contain relevant customer and transaction information respectively.


## 3. Usage

The project is implemented in a Jupyter Notebook (Satyesh_Das_clustering.ipynb).  The notebook performs the following steps:

1. *Loads data:* Reads customer and transaction data from Customers.csv and Transactions.csv.
2. *Merges and aggregates:* Merges the datasets and calculates total spending and number of transactions per customer.
3. *Preprocesses data:* Encodes the 'Region' column and scales numerical features.
4. *Finds optimal clusters:* Iterates through different numbers of clusters and uses the Davies-Bouldin index to find the optimal number.
5. *Performs clustering:* Applies KMeans with the optimal number of clusters.
6. *Visualizes results:* Creates a scatter plot to visualize the clusters.

To run the notebook:

1. Open Satyesh_Das_clustering.ipynb in Jupyter Notebook.
2. Execute the cells sequentially.


## 4. Code Structure

The project consists of the following files:

* **Satyesh_Das_clustering.ipynb:** The main Jupyter Notebook containing the customer segmentation code.  This notebook imports necessary libraries, loads data, performs preprocessing, clustering, and visualization.  Key functions are not explicitly defined as separate functions but are implemented within the notebook's cells.
* **Satyesh_Das_EDA.ipynb:**  (Likely Exploratory Data Analysis notebook - content not provided).
* **Satyesh_Das_lookalike.csv:** (CSV file - content not provided).
* **Satyesh_Das_lookalike.ipynb:** (Likely lookalike modeling notebook - content not provided).
* **LICENSE:**  (License file - content not provided).
* **README.md:** (Project README - content not provided).


## 5.  Example Code Snippet (from Satyesh_Das_clustering.ipynb)

This snippet shows how the data is merged and aggregated:

python
# Merge datasets and aggregate transaction data
data = pd.merge(customers,
                transactions.groupby('CustomerID').agg(
                    total_spent=('TotalValue', 'sum'),
                    total_transactions=('TransactionID', 'count')
                ).reset_index(),
                on='CustomerID', how='left').fillna(0)



## 6. Contributing

Contribution guidelines are not provided in the given codebase.


## 7. FAQ

No FAQ is provided in the given codebase.


## 8. License

License information is not provided in the given codebase.
