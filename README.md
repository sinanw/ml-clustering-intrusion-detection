# ML Clustering - Intrusion Detection
The aim of this project is to apply unsupervised machine learning to perform intrusion analysis and detection on a network traffic dataset. The data set was first cleaned and processed, and PCA was applied for dimensionality reduction, then we implemented KMeans algorithm to perform data clustering and analysis.

## Data Set (KDD Cup 1999)
The dataset used in this demo is: [KDD Cup 1999 - SA](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.fetch_kddcup99.html) provided by [sklearn](https://scikit-learn.org/stable/index.html) library: <br/>
- Since the original KDD Cup '99 dataset was initially created to produce a large training set for supervised learning algorithms, there is a large proportion of abnormal data that is unrealistic in the real world, and inappropriate for unsupervised anomaly detection.
- For this reason, we used the transformed SA version by sklearn which is obtained by selecting all the normal data, and a small proportion of abnormal data.
- The original data set is labeled with a class attribute, but this label was ignored since we are dealing with an unsupervised machine learning problem.


## Data Clustering Details
The project is implemented in three distinct steps simulating the essential data processing and analysis phases. <br/>
- Each step is represented in a corresponding notebook inside [notebooks](notebooks).
- Intermediate data files are stored as outputs/inputs for each processing phase.
- The data files were not uploaded to this repository due to constraints on the upload size. However, the whole analysis is easily reproducible.

### PHASE 1 - Data Cleaning
> Corresponding notebook:  [data-cleaning.ipynb](https://github.com/sinanw/ml-clustering-intrusion-detection/blob/main/notebooks/1-data-cleaning.ipynb)

Implemented data cleaning tasks:
1. Loading the dataset from sklearn library.
2. Exploring dataset summary and statistics.
3. Decoding byte string objects.
4. Dropping irrelevant columns.
5. Checking null values.
6. Checking the cleaned version of the dataset.
7. Storing the cleaned dataset to a csv file.

### PHASE 2 - Data Processing
> Corresponding notebook:  [data-preprocessing.ipynb](https://github.com/sinanw/ml-clustering-intrusion-detection/blob/main/notebooks/2-data-preprocessing.ipynb)

Implemented data processing and transformation tasks:
1. Loading dataset file into pandas DataFrame.
2. Exploring dataset summary and statistics.
3. Exploring categorical features and combining less-frequent values.
4. Encoding categorical features using [One-Hot Encoding](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.OneHotEncoder.html).
5. Implementing data normalization using [Standard Scaler](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html).
6. Checking the processed dataset and storing it to a csv file.

### PHASE 3 - Data Clustering and Analysis
> Corresponding notebook:  [data-analysis.ipynb](https://github.com/sinanw/ml-clustering-intrusion-detection/blob/main/notebooks/3-data-analysis.ipynb)

Implemented data analysis tasks:
1. Loading dataset file into pandas DataFrame.
2. Implementing dimensionality reduction using [Principal Component Analysis (PCA)](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html).
3. Selecting the best k value for KMeans algorithm using [Elbow Method](https://en.wikipedia.org/wiki/Elbow_method_(clustering)).
4. Implementing [KMeans](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html) algorithm for data clustering.
5. Performing anomaly detection based on KMeans clusters.



