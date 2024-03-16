# Modern Mathematical Statistics with Applications Notes

## Chapter 1 Overview and Descriptive Statistics

### 1.1 The Language of Statistics

**Census.** all objects in the population

**Sample.** a subset of the population

------

**Categorical.** e.g. sex, collage major

**Quantitative.** e.g. height

------

**Univariate.** $X$

**Bivariate.** $(X_1,X_2)$​

**Multivariate.** $(X_1,X_2,\ldots,X_n)$ 

------

**Descriptive statistics.** mean, median, use *histograms, boxplots,* and *scatterplots*.

**Inferential statistics.** sample mean, etc.



### 1.2 Graphical Methods in Descriptive Statistics

**Sample size.** $\{X_1,X_2,\ldots,X_n\}$ has a sample size of $n$.

**Definition (Frequency).** The *frequency* of any particular $x$ value is simply the number of times that value occurs in the data set.

**Definition (Relative frequency).** 
$$
\text{relative frequency of a value}=\frac{\text{\# times the value occurs}}{\text{\# observations in the data set}}
$$
**Histogram.** requires subdividing the measurement axis into a suitable number of **class intervals** or **classes**.

Useful rule: $\#~classes \approx \sqrt{\#~observations}$

**Definition (Density).** For any class to be used in a histogram, the density of the data in that class is defined by:
$$
\text{density} = \frac{\text{relative frequency of the class}}{\text{class width}}
$$
**Histogram Shapes.** 

![](C:\Users\Yaze Li\AppData\Roaming\Typora\typora-user-images\image-20240315215716688.png)

------

**Categorical Data.** use a *pie chart* or *bar graph*.

### 1.3 Measures of Center

**Definition (Sample Mean).** The sample mean $\bar{x}$ of observations $x_1, x_2, \ldots, x_n$ is given by:
$$
\bar{x}=\frac{x_1+x_2+\cdots+x_n}{n}=\frac{\sum_{i=1}^n x_i}{n}
$$
**Definition (Sample Median).** 
$$
\tilde{x}= \begin{cases}
\bigl(\frac{n+1}{2}\bigr)\text{th ordered value},~~&n\text{ is odd}\\
\text{average of the }\bigl(\frac{n}{2}\bigr)\text{th and }\bigl(\frac{n}{2}+1\bigr)\text{th ordered value}.&n\text{ is even}
\end{cases}
$$

### 1.4 Measures of Variability

**Definition (Sample variance).** 
$$
s^2=\frac{\sum_{i=1}^n\left(x_i-\bar{x}\right)^2}{n-1}
$$
**Definition (Population standard deviation).** 
$$
\sigma^{2}=\frac{\sum_{i=1}^{N}\left(x_{i}-\mu\right)^{2}}{N}
$$

------

**Definition (Quartiles).** The lower quartile (or first quartile), $q_1$, is the median of the lower half of the data, and the upper quartile (or third quartile), $q_3$, is the median of the upper half.

**Definition (IQR).** A measure of spread that is resistant to outliers is the **interquartile range (iqr)**, given by:
$$
\text{iqr}=q_3-q_1
$$
**Definition (Outlier).** Any observation farther than 1.5iqr from the closest quartile is an outlier:
$$
x \text{is an outlier if }x<q_1-1.5\text{iqr or }x>q_3+1.5\text{iqr}
$$
**Definition.** An outlier is **extreme** if it is more than 3iqr from the nearest quartile, and it is **mild** otherwise.