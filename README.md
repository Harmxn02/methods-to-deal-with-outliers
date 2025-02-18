# Methods to deal with datasets with extreme outliers

## Background

We want to use a dataset on network data to train a machine learning model. The dataset contains a lot of columns with extreme outliers. We want to explore different methods to deal with these outliers.

The dataset in this repository will be the CICIDS2017 dataset, but the same is true for 1 other dataset.

## Testing methodolgy

We will apply each of the methods on a dataset, so that we obtain a new dataset. We will then train the same machine learning model on each of the datasets and compare the results using a classification report.

## Methods

1. Capping (Winsorization)
2. Trimming (Removing Outliers)
3. Transformation (Log, Square Root, Box-Cox)
4. Using Robust Statistics
5. Using Robust Scalers
6. Imputing Outliers with Statistical Estimates
7. Use a Model-Based Approach

### 1. Winsorization (capping)

In this method, we replace extreme values with a specified percentile value. For example, we can replace all values above the 95th percentile with the value at the 95th percentile. This method is also known as capping.

### 2. Trimming

In this method, we remove the extreme values from the dataset. For example, we can remove all values above the 95th percentile.

### 3. Transformation

In this method, we apply a transformation to the data to make it more normally distributed. For example we can take the log, square root, or Box-Cox transformation of the data.

### 4. Using Robust Statistics

In this method, we use robust statistics to estimate the mean and standard deviation of the data. This method is less sensitive to outliers than the standard mean and standard deviation.

### 5. Using Robust Scalers

In this method, we simply import the RobustScaler from the sklearn library and scale the data using this method.

### 6. Imputing Outliers with Statistical Estimates

In this method, we replace the outliers with statistical estimates. For example, we can replace the outliers with the mean or median of the data.

### 7. Use a Model-Based Approach

In this method, we train a regression model to predict expected values and flag outliers as those that deviate significantly from the predicted values.
