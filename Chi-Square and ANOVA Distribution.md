# Chi-Square Distribution in Data Science
The **Chi-Square distribution** is widely used in statistics and data science for testing hypotheses related to categorical data, model fit, and variance estimation. 
It plays a key role in feature selection, A/B testing, and independence testing in ML applications.
- most common goodness of fit test

## Definition
The **Chi-Square (\( \chi^2 \)) distribution** is a probability distribution used in hypothesis testing and inferential statistics, particularly for categorical data analysis. It is defined as:

\[ X = Z_1^2 + Z_2^2 + \dots + Z_k^2 \]

where \( Z_i \sim N(0,1) \) are independent standard normal variables.

## Probability Density Function (PDF)
For a chi-square distributed random variable \( X \) with \( k \) degrees of freedom:

\[ f(x; k) = \frac{x^{(k/2 - 1)} e^{-x/2}}{2^{k/2} \Gamma(k/2)}, \quad x > 0 \]

where \( \Gamma(k/2) \) is the gamma function.

## Key Properties
- **Mean**: \( E[X] = k \)
- **Variance**: \( \text{Var}(X) = 2k \)
- **Skewness**: \( \sqrt{8/k} \)
- **Kurtosis**: \( 12/k \)
- Approaches **normal distribution** as \( k \) increases.

## Applications in Data Science
### 1. Chi-Square Goodness-of-Fit Test
- **Purpose**: Checks if a sample follows a specified distribution.
- **Formula**:
  \[ \chi^2 = \sum \frac{(O_i - E_i)^2}{E_i} \]
  where \( O_i \) = observed frequency, \( E_i \) = expected frequency.
- **Example**: Testing if a die is fair.

### 2. Chi-Square Test for Independence
- **Purpose**: Tests if two categorical variables are independent.
- **Formula**:
  \[ \chi^2 = \sum \frac{(O_{ij} - E_{ij})^2}{E_{ij}} \]
  where \( O_{ij} \) and \( E_{ij} \) are observed and expected values in a contingency table.
- **Example**: Checking if gender and product preference are related.

### 3. Variance Estimation in ML
- Used to estimate population variance from a sample:
  \[ \chi^2 = \frac{(n-1)s^2}{\sigma^2} \]
  where \( s^2 \) = sample variance, \( \sigma^2 \) = population variance, \( n \) = sample size.

### 4. Feature Selection in ML
- Chi-Square test is used in **feature selection** to identify significant features in classification problems.
- High \( \chi^2 \) values indicate strong relationships between features and target variables.

## Example Calculation
Given a contingency table for customer preference:

| Age Group | Prefer A | Prefer B | Total |
|-----------|---------|---------|-------|
| 18-25     | 40      | 60      | 100   |
| 26-35     | 50      | 50      | 100   |
| 36-45     | 30      | 70      | 100   |
| **Total** | 120     | 180     | 300   |

1. **Compute Expected Frequency**:
   \[ E = \frac{\text{Row Total} \times \text{Column Total}}{\text{Grand Total}} \]
   Example for (18-25, A): \( E = \frac{100 \times 120}{300} = 40 \)

2. **Compute \( \chi^2 \) Statistic**:
   \[ \chi^2 = \sum \frac{(O - E)^2}{E} \]
   Compare \( \chi^2 \) with the critical value from the chi-square table.

## Analysis of Variance (ANOVA) in Data Science
### Definition
ANOVA (Analysis of Variance) is a statistical method used to compare the means of multiple groups to determine if at least one group differs significantly from the others.

### Formula for One-Way ANOVA
\[ F = \frac{\text{Between-Group Variance}}{\text{Within-Group Variance}} = \frac{MS_{between}}{MS_{within}} \]
where:
- \( MS_{between} \) = Mean Square Between Groups
- \( MS_{within} \) = Mean Square Within Groups

### Applications
- **Comparing sales across different regions**
- **Assessing student performance across multiple schools**
- **Analyzing experimental results in A/B testing**

## Difference Between Chi-Square and ANOVA

| Feature       | Chi-Square Test | ANOVA |
|--------------|----------------|-------|
| Data Type    | Categorical     | Continuous |
| Purpose      | Tests independence of categorical variables | Compares means of multiple groups |
| Hypothesis   | Tests if variables are related | Tests if means of groups are different |
| Test Statistic | \( \chi^2 \) value | \( F \)-statistic |
| Example Use  | Checking if gender affects product preference | Comparing average test scores of different schools |

Both **Chi-Square** and **ANOVA** are crucial statistical tools in data science, used for different types of data and purposes.
While Chi-Square is useful for categorical data independence, ANOVA is ideal for comparing means of continuous data across groups.


