# Assignment_DAI101_Rohan_23114088

## Detailed Report: Ecommerce Delivery Analytics Data Analysis

### 1. Introduction
This report presents the data cleaning and exploratory data analysis (EDA) of the *Ecommerce Delivery Analytics* dataset. The dataset contains multiple numerical and categorical variables representing various attributes of ecommerce delivery performance. It is expected to have missing values, duplicate records, and outliers. The analysis is designed to address these issues and reveal underlying patterns and relationships within the data.

### 2. Data Cleaning

#### 2.1. Data Loading and Inspection
- **Loading the Dataset:** The dataset was imported using the `pandas` library.
- **Inspection:** Basic information such as data shape, data types, and a preview of the first few rows were examined. This initial inspection helped identify the nature of the variables (numerical vs. categorical) and any potential issues like missing or inconsistent entries.

#### 2.2. Handling Missing Values
- **Technique:** Missing values were addressed using either imputation (where appropriate) or by removing records, depending on the severity and context.
- **Rationale:** Ensuring that missing data do not bias the analysis is crucial. For example, if only a few records have missing values, they might be removed; however, if a column has many missing values, imputation might be preferred.

#### 2.3. Removing Duplicate Records
- **Detection and Removal:** The dataset was checked for duplicate rows using Pandas functions, and duplicates were removed to ensure the integrity of subsequent analysis.
- **Impact:** Removing duplicates prevents skewed statistical summaries and incorrect correlation assessments.

#### 2.4. Outlier Detection and Treatment
- **Method:** The Interquartile Range (IQR) method was employed on numerical columns to detect outliers. Data points falling outside 1.5 times the IQR below the first quartile or above the third quartile were considered outliers.
- **Treatment:** Identified outliers were either removed or flagged, depending on their impact on the overall analysis.

#### 2.5. Standardizing Categorical Values
- **Process:** Categorical variables were standardized by correcting typos, converting strings to lower-case, and trimming any extraneous whitespace.
- **Benefit:** This step ensures that similar values are not treated as distinct categories, which is critical for accurate frequency counts and group comparisons.

### 3. Exploratory Data Analysis (EDA)

#### 3.1. Univariate Analysis
- **Summary Statistics:** For numerical columns, statistics such as mean, median, mode, variance, and skewness were calculated. This provided insights into the central tendencies and dispersion of each variable.
- **Frequency Distributions:** For categorical variables, count plots and frequency distributions were generated to understand the prevalence of each category.
- **Visualizations:**
  - **Histograms:** Used to visualize the distribution of numerical variables.
  - **Box Plots:** Helped identify the spread and potential outliers in the data.

#### 3.2. Bivariate Analysis
- **Correlation Matrix:** A heatmap was used to display the correlations among numerical variables, helping to identify strong relationships or multicollinearity.
- **Scatter Plots:** Selected pairs of numerical variables were plotted to visualize continuous variable relationships.
- **Comparative Plots:** Bar plots, violin plots, and box plots were created to compare numerical variables across different categories, highlighting differences between groups.

#### 3.3. Multivariate Analysis
- **Pair Plots:** To analyze multiple relationships simultaneously, pair plots were generated. These plots help in visualizing interactions between pairs of numerical variables, with a categorical variable used as a hue for differentiation.
- **Heatmaps:** A detailed heatmap of the correlation matrix was created for numerical variables with more than 20 distinct values, providing a comprehensive view of the variable interactions.
- **Grouped Comparisons:** Box plots were used to compare the distribution of a numerical variable across different levels of a categorical variable. The plots were organized in groups of four per row to ensure clarity and readability.

### 4. Detailed Functionalities Implemented

#### Data Cleaning Code
- The code performs data inspection, handling of missing values, duplicate removal, outlier treatment via the IQR method, and categorical value standardization.

#### Univariate Analysis Code
- It computes summary statistics, creates histograms and box plots for numerical variables, and generates count plots for categorical variables.

#### Bivariate Analysis Code
- It calculates a correlation matrix (visualized via a heatmap) and generates scatter plots for examining relationships between pairs of numerical variables.

#### Multivariate Analysis Code
The analysis uses:
- **Pair Plots** for multiple variable relationships, split into groups of four columns per row to maintain readability.
- **Correlation Heatmaps** with enlarged figures for clear visualization.
- **Grouped Comparisons** (box plots) to identify the combined effects of multiple features.

### 5. Expected Outcomes
By the end of this analysis, the following outcomes are achieved:
- **Cleaned Dataset:** The dataset is free from duplicates, has minimal missing values, and has outliers either removed or accounted for. Categorical variables are standardized.
- **Insightful Descriptive Statistics:** Summary statistics provide a clear understanding of the distribution and central tendencies of each variable.
- **Understanding of Variable Relationships:** Bivariate and multivariate analyses reveal significant correlations and interactions between variables.
- **Visualization of Data Distributions:** Graphs and plots (histograms, scatter plots, pair plots, heatmaps) facilitate a deeper understanding of data patterns, trends, and anomalies.

### 6. Conclusion
This analysis has demonstrated the application of rigorous data cleaning and comprehensive exploratory data analysis techniques. By systematically addressing missing values, duplicates, outliers, and inconsistencies, the dataset was prepared for meaningful analysis. Univariate, bivariate, and multivariate techniques provided valuable insights into the data structure and relationships among variables. These insights can serve as a foundation for further predictive modeling or decision-making processes in the context of ecommerce delivery analytics.

The methods applied not only ensure data integrity but also help in uncovering complex interactions within the dataset, fulfilling the assignment’s requirements. For further analysis, additional advanced modeling or machine learning techniques can be explored based on the insights gathered.

