The following tables show how each measure can be directly applied during the data cleaning process to ensure datasets are consistent, accurate, and free of anomalies.
# Table 1: Measures of Central Tendency in Data Cleaning

| Measure | Formula | Hint: Data Cleaning Aspect | Scenario 1 | Scenario 2 |
|---------|---------|-----------------------------|------------|------------|
| **Mean (Arithmetic Mean)** | \( \mu = \frac{1}{n} \sum_{i=1}^{n} x_i \) | Use to detect outliers; a large deviation from the mean could indicate a data anomaly. | Identifying incorrect entries in average sales data (e.g., unusually high values). | Spotting extreme temperature records in weather data. |
| **Median** | - If \( n \) is odd: Middle value.  
  - If \( n \) is even: \( \text{Median} = \frac{x_{(n/2)} + x_{(n/2+1)}}{2} \) | Use when the data has skewness or outliers; the median is not affected by extreme values. | Analyzing typical house prices in a city where some houses are extremely expensive. | Handling income data with extreme high earners. |
| **Mode** | Most frequently occurring value in the dataset. | Identify data entry errors (e.g., a mode that is nonsensical or unexpected) or check for categorical consistency. | Verifying the most frequent category in customer feedback (e.g., satisfaction levels). | Checking the most common product ID in a sales dataset. |
| **Harmonic Mean** | \( HM = \frac{n}{\sum_{i=1}^{n} \frac{1}{x_i}} \) | Use to average rates or ratios where outliers in the denominators may indicate erroneous entries. | Detecting anomalies in average speed data across vehicles. | Validating the average price per unit in cost calculations. |
| **Geometric Mean** | \( GM = \sqrt[n]{\prod_{i=1}^{n} x_i} \) | Use to analyze growth rates or percentages and ensure data follows expected trends. | Validating annual growth rates of sales across regions. | Checking for unrealistic percentage growth in investment portfolios. |



# Table 2: Measures of Dispersion in Data Cleaning

| Measure | Formula | Hint: Data Cleaning Aspect | Scenario 1 | Scenario 2 |
|---------|---------|-----------------------------|------------|------------|
| **Range** | \( R = \text{Max}(x) - \text{Min}(x) \) | Use to detect extreme values that may indicate outliers or data entry errors. | Identifying unreasonable temperature ranges in weather data. | Spotting errors in sales revenue with extreme max or min values. |
| **Variance (Population)** | \( \sigma^2 = \frac{1}{n} \sum_{i=1}^{n} (x_i - \mu)^2 \) | Use to identify datasets with large spread, which might indicate inconsistent data quality. | Checking variability in the weights of packaged goods. | Assessing spread in product prices for consistency checks. |
| **Variance (Sample)** | \( s^2 = \frac{1}{n-1} \sum_{i=1}^{n} (x_i - \bar{x})^2 \) | Use to detect irregular variability in sample data compared to population expectations. | Identifying variability in a sample of student grades for consistency. | Finding high variability in rainfall data from multiple regions. |
| **Standard Deviation (Population)** | \( \sigma = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (x_i - \mu)^2} \) | Use to identify anomalous deviations from the mean and highlight potential errors. | Detecting large deviations in employee salary records. | Spotting deviations in factory product weights. |
| **Standard Deviation (Sample)** | \( s = \sqrt{\frac{1}{n-1} \sum_{i=1}^{n} (x_i - \bar{x})^2} \) | Use to validate sample consistency and ensure data aligns with population expectations. | Verifying profit spread in sampled businesses. | Validating consistency in agricultural yield data samples. |
| **Interquartile Range (IQR)** | \( IQR = Q_3 - Q_1 \), where \( Q_1 \) is the 25th percentile and \( Q_3 \) is the 75th percentile. | Use to detect outliers by identifying values outside the lower and upper bounds of \( Q_1 - 1.5 \cdot IQR \). | Flagging outliers in house prices in a city. | Identifying unusual delivery times in logistics data. |
| **Mean Absolute Deviation** | \( MAD = \frac{1}{n} \sum_{i=1}^{n} |x_i - \mu| \) | Use for simpler variability checks when variance is too sensitive to extreme values. | - | - |
| **Coefficient of Variation** | \( CV = \frac{\sigma}{\mu} \times 100\% \) | Use to compare relative variability across datasets with different units or scales. | Comparing spread in sales data across regions with different revenue sizes. | Assessing consistency in test scores across different subjects. |
| **Skewness** | \( \text{Skewness} = \frac{\frac{1}{n} \sum_{i=1}^{n} (x_i - \mu)^3}{\sigma^3} \) | Use to identify asymmetry in the dataset; high skewness might indicate incorrect or incomplete data. | Detecting skewness in income data to find data entry errors for extreme earners. | Spotting data issues in product sales showing extreme one-sided demand. |
| **Kurtosis** | \( \text{Kurtosis} = \frac{\frac{1}{n} \sum_{i=1}^{n} (x_i - \mu)^4}{\sigma^4} - 3 \) | Use to check tailedness; high kurtosis could indicate unusual extreme events. | Identifying heavy-tailed distributions in financial risk modeling. | Flagging excessive outliers in insurance claim amounts. |



# Data Cleaning Use Cases:

## 1. Central Tendency:
- **Mean**: Detect outliers that may pull the average up or down.
- **Median**: Use for datasets with skewed distributions or significant outliers.
- **Mode**: Identify common categories and detect inconsistent entries.
- **Harmonic/Geometric Means**: Useful for ensuring rates and ratios follow expected patterns.

## 2. Dispersion:
- Use **range** for spotting extremes.
- **Variance** and **standard deviation** help assess overall data spread.
- **IQR** and **MAD** are robust for detecting outliers in skewed data.
- **Skewness** and **kurtosis** provide deeper insights into the shape of the data, helping find irregularities.


