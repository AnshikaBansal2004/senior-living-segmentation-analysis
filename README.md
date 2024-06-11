# Senior Living Facility Segmentation Analysis

## Problem Statement
A senior living facility aims to enhance its services and optimize resident satisfaction. The facility collects various data points related to its residents, including demographics, preferences, and activity engagement. The objective is to segment the resident population based on their characteristics and behaviors and analyze each segment to identify opportunities for personalized care and service improvements.

## Approach
1. **Data Collection and Preparation:** Gather comprehensive resident data. Cleanse and preprocess the data, handling missing values, outliers, and data inconsistencies.
2. **Feature Engineering:** Perform feature engineering techniques, such as data transformation, scaling, and encoding, to prepare the features for analysis.
3. **Dimensionality Reduction:** Reduce dimensionality with Principal Component Analysis (PCA) to increase interpretability and minimize information loss.
4. **Segmentation Algorithm Selection and Model Development:** Use the Elbow Method to determine the number of clusters for K-means clustering. Analyze each cluster's characteristics, preferences, and behaviors.
5. **Cluster Profiling:** Utilize descriptive statistics, data visualization, and exploratory data analysis techniques to understand cluster patterns and identify key differentiating factors.

## Solution Overview
- Divided the DataFrame into two main groups: one for residents (based on RESIDENTID) and another for units (based on UNITNUMBER and FACILITYID).
- Selected columns for segmentation, including FACILITYID, UNITNUMBER, UNITCLASS, RESIDENTID, PAYOR, OCCUPANCYTYPE, etc.
- Applied PCA on the unit DataFrame and reduced it to 3 columns (PC1, PC2, PC3).
- Chose k=3 clusters using the K-means algorithm.

## Insights
- **Cluster 0: Most Profitable Segment**
    - Contains over 100,000 residents.
    - Majority prefer 'Studio (0)' unit types.
    - Short-term stays are popular, contributing to higher turnover and potentially increased revenue.

- **Cluster 1: Largest and Diverse Segment**
    - Comprises over 200,000 residents.
    - Majority prefer 'Single BedRoom (1)' unit types.
    - Diverse payor types and occupancy types.

- **Cluster 2: Niche Segment with Unique Characteristics**
    - The smallest cluster with over 50,000 residents.
    - Shows a unique lifestyle or care requirements.
    - Short-term stays are less common.

## Conclusion
The segmentation analysis highlights distinct customer segments with unique preferences and characteristics. Leveraging these insights, senior living facilities can tailor their offerings, marketing strategies, and services to meet the specific needs of each cluster, leading to enhanced resident satisfaction and higher profitability.

## Libraries and Modules
- pandas
- numpy
- matplotlib.pyplot
- seaborn
- sklearn.preprocessing.LabelEncoder
- scipy.stats
- sklearn.preprocessing.StandardScaler
- sklearn.cluster.KMeans
- sklearn.decomposition.PCA
- yellowbrick.cluster.KElbowVisualizer
- plotly.express

## How to Use
1. Clone the repository to your local machine.
2. Install the required libraries and modules using pip install.
3. Run the Jupyter Notebook or Python script to perform the segmentation analysis.

