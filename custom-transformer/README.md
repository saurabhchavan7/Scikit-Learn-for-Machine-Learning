## Transformers in scikit-learn

### Definition
A transformer is a specific type of estimator used for transforming datasets.

### Functions
- **Preprocessing tasks**: Scaling, encoding categorical variables, handling missing values, feature extraction.

### Methods
- **fit**: Learns parameters from the data.
- **transform**: Applies the transformation to the data.
- **fit_transform**: Combines `fit` and `transform` in one step.

### Examples of Built-in Transformers
- **StandardScaler**: Scales features to have zero mean and unit variance.
- **OneHotEncoder**: Encodes categorical features as a one-hot numeric array.
- **SimpleImputer**: Fills missing values with specified values or strategies.
- **PCA (Principal Component Analysis)**: Reduces the dimensionality of data.

### Disadvantages of Transformers
- **Applies to the entire dataset**: When a transformer is applied, it transforms all columns/features of the dataset. This could be problematic if different transformations are needed for different features.
- **Limited built-in transformers**: Not all possible transformations are available in scikit-learn. This necessitates creating custom transformers for specific needs.

---

## Creating Custom Transformers

### Purpose
To handle specific data transformations or preprocessing steps not covered by built-in transformers.

### Approaches
- **Function approach**: Used when the transformation does not require learning from the data (e.g., scaling by a fixed value).
- **Class approach**: Used when the transformation requires learning from the data (e.g., scaling based on mean and standard deviation).
