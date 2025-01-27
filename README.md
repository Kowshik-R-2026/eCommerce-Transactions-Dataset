# eCommerce Transactions Analysis

This repository contains the implementation of the **eCommerce Transactions Analysis** assignment. The assignment involves three main tasks: **Exploratory Data Analysis (EDA)**, building a **Lookalike Model**, and performing **Customer Segmentation** using clustering techniques. Each task has been implemented step-by-step, and the outputs are provided as required in the assignment.

---

## Project Structure
The repository contains the following files:

─ Customers.csv # Dataset: Customer information 
─ Products.csv # Dataset: Product information 
─ Transactions.csv # Dataset: Transaction information

markdown
Copy
Edit

---

## Task Descriptions and Strategies

### **Task 1: Exploratory Data Analysis (EDA)**
#### Objective:
Perform an in-depth EDA on the given datasets and derive at least 5 business insights.

#### Steps:
1. **Data Loading**: Load `Customers.csv`, `Products.csv`, and `Transactions.csv` using pandas.
2. **Data Cleaning**: Handle missing values, check for duplicates, and ensure consistent data formats.
3. **Feature Engineering**: Derive additional features like:
   - **Total Transaction Count per Customer**.
   - **Average Purchase Value per Customer**.
   - **Customer Signup Age** (from SignupDate).
4. **Visualization**:
   - Analyze customer distribution by region.
   - Study product popularity by category.
   - Visualize transaction trends over time.
   - Correlate transaction values with product prices.
   - Identify top customers by total purchase value.

---

### **Task 2: Lookalike Model**
#### Objective:
Build a model that recommends 3 similar customers based on profile and transaction history for the first 20 customers.

#### Steps:
1. **Data Preparation**:
   - Combine customer, product, and transaction datasets.
   - Aggregate features such as total purchase value, average transaction value, and product preferences.
2. **Feature Engineering**:
   - Encode categorical variables like product categories and regions.
   - Normalize numerical features for similarity computation.
3. **Similarity Computation**:
   - Use cosine similarity or Euclidean distance on aggregated customer profiles.
   - Compute similarity scores between all customers.
4. **Recommendation**:
   - For each of the first 20 customers, recommend the top 3 most similar customers along with their similarity scores.
5. **Output Format**:
   - Save recommendations in a CSV file (`Lookalike.csv`) with the format:
     ```
     CustomerID, Lookalikes
     C0001, [(C0010, 0.85), (C0020, 0.82), (C0030, 0.80)]
     ```

---

### **Task 3: Customer Segmentation**
#### Objective:
Segment customers using clustering techniques and evaluate the results using clustering metrics (DB Index).

#### Steps:
1. **Data Preparation**:
   - Merge customer profiles with transaction summaries.
   - Select relevant features for clustering, e.g., total transaction value, average transaction value, and days since signup.
2. **Clustering Algorithm**:
   - Use K-Means, DBSCAN, or Hierarchical Clustering.
   - Experiment with different numbers of clusters (2-10).
   - Evaluate each model using the DB Index and silhouette scores.
3. **Visualization**:
   - Create scatterplots for clusters across different feature pairs.
   - Visualize cluster distributions using bar charts and heatmaps.
   - Provide a 3D scatter plot for better cluster interpretation.
4. **Insights**:
   - Report the number of clusters formed, DB Index value, and characteristics of each cluster.


## Prerequisites

- Python 3.8+
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `scipy`

Install the required libraries using:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy
