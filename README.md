<style>
  .col2 {
    columns: 2 200px;         /* number of columns and width in pixels*/
    -webkit-columns: 2 200px; /* chrome, safari */
    -moz-columns: 2 200px;    /* firefox */
  }
  .col3 {
    columns: 2 100px;
    -webkit-columns: 2 100px;
    -moz-columns: 2 100px;
  }
  .myClass_border
  {
   border: 3px solid black;
    padding: 2px;
    margin: 2px;
  }
</style>
Statistic and Statistical languages
-----------------------------------

### Branches of statistics

**Descriptive Statistics**

-   Organizing, Summarizing Information
    -   Data and Variables
    -   Population and Samples
    -   Observational and Experimental Studies
-   Graphical methods
    -   Categorical Data
    -   Numeric Data
-   Numerical methods
    -   Center of the data
    -   Variability
    -   Relative Standing
    -   Association and Correlation
    -   Regression

**Inferential Statistics**

-   Probability
    -   Probability of Events
    -   Probability distributions
-   Estimation
-   Decision making

### Statistical Tools

Excel - Spreadsheet software that uses a grid of cells arranged in
numbered rows and letter-named columns to organize data

Python object-oriented programing language - Computer science language
design to be highly extensible with interfaces to existing applications.
Organizes and manipulates data within objects leveraging similar data
packages as R.

**R - Interpreted programing language that use vectors of data elements
to organize data into lists or dataframe**

Analytical Methods with practice using R
----------------------------------------

### Measures of centrality, variability and relative standing

#### Data types and Variables

**Categorical** (or qualitative) if the individual observations are
categorical responses.  
**Numerical** (or quantitative) if the individual observations are
numerical responses *where numerical operations generally have meaning*.

-   Discrete if the possible values are isolated points on the number
    line.
-   Continuous if the set of possible values form an entire interval on
    the number line.

Variable: A variable is any characteristic whose value may change from
one individual to another.

-   A **univariate** data set consists of observations on a single
    variable made on individuals in a sample or population.
-   A **bivariate** data set consists of observations on two variables
    made on individuals in a sample or population.
-   A **multivariate** data set consists of observations on two or more
    variables made on individuals in a sample or population.

**Population**: The entire collection of individuals or objects about
which information is desired is called the population.  
**Sample**: A sample is a subset of the population, selected for study
in some prescribed manner.

#### Centrality

The **sample mean** of a numeric sample
*x*<sub>1</sub>, *x*<sub>2</sub>, …, *x*<sub>*n*</sub>, usually denoted
by *x̄*, is the sum of the observations divided by the number
observations in the sample.
$\\bar{x} = \\frac{x\_1+x\_2+\\cdots +x\_n}{n} = \\frac{\\sum (x)}{n}$.
The **population mean** is denoted by *μ*, is the average of all x
values in the entire population. The **centroid** is the observation, in
the sample, that is closest to the mean value.

Problems with the mean

1.  The mean is not necessarily like any of the observations
2.  The mean is sensitive to outliers

The **sample median** is obtained by first ordering the n observations
from smallest to largest (with any repeated values included, so that
every sample observation appears in the ordered list). Then finding the
middle value if n is odd or the mean of the middle two values if n is
even. A **trimmed mean** is computed by deleting a selected number (or
percentage) of values from each end of an ordered list, and finally
computing the mean of the remaining values. The sample median and
trimmed mean are not sensitive to outliers.

#### Variability of Data

-   Range: Quick, does not represent all the data
    Range = maximum − minimum
-   Standard deviation, s: Typical numeric representation of the
    deviation from the mean
-   Quartiles: A measure of variability less sensitive to outliers than
    s
    -   Lower quartile (Q1) = median of the lower half of the data set
    -   Upper Quartile (Q3) = median of the upper half of the data set
    -   Interquartile range (iqr) = upper quartile - lower quartile
    -   An observations is an outlier if it is more than 1.5 iqr away
        from the nearest quartile
    -   An outlier is **extreme** if it is more than 3 iqr from the
        nearest quartile and it is a **mild** outlier otherwise

#### Relative Standing

-   Frequency for a particular category is the number of times the
    category appears in the data set.
    -   Relative frequency for a particular category is the fraction or
        proportion of the time that the category appears in the data set
-   Percentile - Show percent of the observation in the data set fall at
    or below that value
-   Empirical Rule - Show percentage of observations within 1,2 and 3
    standard deviations for a normal distribution
    -   Approximately 68% of the observations are within 1 standard
        deviation of the mean.
    -   Approximately 95% of the observations are within 2 standard
        deviation of the mean.
    -   Approximately 99.7% of the observations are within 3 standard
        deviation of the mean.
-   Z Score - Standardized score of number of standard deviations from
    the mean and used to calculate percentile for a normal distribution.
    $\\text{Z} = \\frac{x- \\bar{x}}{S}$

<center>
<h4>
Descriptive Statistics
</h4>
</center>
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Numeric Method</th>
<th>Numeric</th>
<th>Categorical</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Center</td>
<td>Sample Mean <span class="math inline">$\bar{x} = \frac{x_1+x_2+\cdots +x_n}{n} = \frac{\sum (x)}{n}$</span></td>
<td>Sample proportion of success <span class="math inline">$\hat{p} = \frac {\text{number of S's in the sample}}{n}$</span></td>
</tr>
<tr class="even">
<td>Variability</td>
<td>Sample Standard deviation <span class="math inline">$s = \sqrt{\frac{1}{N-1} \sum_{i=1}^N (x_i - \overline{x})^2}$</span>, Estimating <span class="math inline">$\sigma = \frac{\sigma_\bar{x}}{\sqrt{n}}$</span></td>
<td>Estimating <span class="math inline"><em>μ</em><sub><em>p̂</em></sub> = <em>p</em></span>, <span class="math inline">$\sigma_\hat{p} = \sqrt{\frac{p(1-p)}{n}}$</span></td>
</tr>
<tr class="odd">
<td>Relative Standing Statistic</td>
<td><span class="math inline">$\text{z} = \frac{x- \bar{x}}{\sigma}$</span>, Percentage use <code>dnorm</code></td>
<td></td>
</tr>
</tbody>
</table>

Distributions:

-   Unimodal,bimodal & multimodal indicate number of clear peaks
-   Symmetric Mean = median, Positively skewed Mean &gt; median,
    Negatively skewed Mean &lt; median

### Metrics, targets and benchmarking

What is a [metric](https://en.wikipedia.org/wiki/Metric)? A ratio that
can be used to evaluate performance over time and between individuals,
teams, departments and organizations.

Analytic Interpretation with practice using R
---------------------------------------------

### Probability

Methods for Determining Probability

1.  **The classical approach**: Appropriate for experiments that can be
    described with equally likely outcomes.
2.  **The subjective approach**: Probabilities represent an individual’s
    judgment based on facts combined with personal evaluation of other
    information.
3.  **The relative frequency approach**: An estimate is based on an
    accumulation of experimental results. This estimate, usually derived
    empirically, presumes a replicable chance experiment.

**Law of Large Numbers**: As the number of repetitions of a chance
experiment increases, the chance that the relative frequency of
occurrence for an event will differ from the true probability of the
event by more than any very small number approaches zero.

Two events E and F are said to be **independent** if P(E\|F)=P(E). If E
and F are not independent, they are said to be **dependent events**.

Two events are **mutually exclusive** if they have no out-comes in
common. The term **disjoint** is also sometimes used to describe events
that have no outcomes in common.

<center>
<h4>
Probability Events
</h4>
</center>
<table>
<colgroup>
<col style="width: 52%" />
<col style="width: 48%" />
</colgroup>
<thead>
<tr class="header">
<th>Event</th>
<th>Probability</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>A</td>
<td><span class="math inline"><em>P</em>(<em>A</em>) ∈ [0, 1]</span></td>
</tr>
<tr class="even">
<td>Not A</td>
<td><span class="math inline"><em>P</em>(<em>A</em><sup><em>c</em></sup>) = 1 − <em>P</em>(<em>A</em>)</span>, <span class="math inline"><em>P</em>(<em>A</em><sup><em>c</em></sup>) + <em>P</em>(<em>A</em>) = 1</span></td>
</tr>
<tr class="odd">
<td>A or B</td>
<td><span class="math inline"><em>P</em>(<em>A</em> ∪ <em>B</em>) = <em>P</em>(<em>A</em>) + <em>P</em>(<em>B</em>) − <em>P</em>(<em>A</em> ∩ <em>B</em>)</span></td>
</tr>
<tr class="even">
<td>A or B</td>
<td><span class="math inline"><em>P</em>(<em>A</em> ∪ <em>B</em>) = <em>P</em>(<em>A</em>) + <em>P</em>(<em>B</em>)</span> If mutually exclusive</td>
</tr>
<tr class="odd">
<td>A and B</td>
<td><span class="math inline"><em>P</em>(<em>A</em> ∩ <em>B</em>)</span> = P(A</td>
</tr>
<tr class="even">
<td>A and B</td>
<td><span class="math inline"><em>P</em>(<em>A</em> ∩ <em>B</em>) = <em>P</em>(<em>A</em>)<em>P</em>(<em>B</em>)</span> If independent</td>
</tr>
<tr class="odd">
<td>A given B</td>
<td><span class="math inline">$P(A \mid B) = \frac{P(A \cap B)}{P(B)} = \frac{P(B|A)P(A)}{P(B)}$</span></td>
</tr>
</tbody>
</table>

If *B*<sub>1</sub>, *B*<sub>2</sub>, ...*B*<sub>*k*</sub> are mutually
exclusive events with *P*(*B*<sub>1</sub>) + *P*(*B*<sub>2</sub>) = 1
then for any event E.

-   Law of Total Probability
    *P*(*E*) = *P*(*E* ∩ *B*<sub>1</sub>) + *P*(*E* ∩ *B*<sub>2</sub>)  
-   Bays Rule
    $P(B\_1\|E) = \\frac{P(E\|B\_1)P(B\_1)}{P(E\|B\_1)P(B\_1) + P(E\|B\_2)P(B\_2)}$  
-   Discrete Probability: *μ*<sub>*x*</sub> = ∑*x**p*(*x*), Variance
    *σ*<sub>*x*</sub><sup>2</sup> = ∑(*x* − *μ*<sub>*x*</sub>)<sup>2</sup>*p*(*x*),
    ∑*p*(*x*) = 1
-   Binomial Distribution:
    $\\mu\_x = np \\text{ and } \\sigma\_x = \\sqrt{np(1-p)}$,
    $P(x) = \\binom n x p^x(1-p)^{n-x} \\text{ where } \\binom n x =\\frac{n!}{x!(n-x)!}$
-   Geometric Distibution: *P*(*x*) = *p*(1 − *p*)<sup>(*x* − 1)</sup>
-   Continuous Probability distribution: Normal, Uniform, etc. Total
    area under the density curve is equal to 1.

### Sampling Distrubtion

Any quantity computed from values in a sample is called a **statistic**.

The observed value of a statistic depends on the particular sample
selected from the population; typically, it varies from sample to
sample. This variability is called **sampling variability**. The
distribution of a statistic is called its **sampling distribution**.

When random samples are selected form a population, the following are
properties of the sampling distribution of *x̄*.

**Central Limit Theorem**: If n is large (n exceeds 30) or the
population distribution is normal, the standardized variable Z has
(approximately) a standard normal (z) distribution regardless of the
underlying distribution.

A **point estimate** of a population characteristic is a single number
that is based on sample data and represents a plausible value of the
characteristic

A **confidence interval** an interval of plausible values for a
population characteristic. It is constructed so that, with a chosen
degree of confidence, the value of the characteristic will be captured
inside the interval. \* The **bound on error estimation**, B, represents
the confidence interval quantity. Also called the **margin of error**.
\* The sample size, n, can be calulcated with the desired confidence
interval and bound of error.

The **confidence level** is the success rate of the method used to
construct a confidence interval.

When *σ* is unknown *μ* can be estimated with the Student’s **t
distribution** depending on the **degrees of freedom** which is the
number of values in the final calculation of a statistic that are free
to vary.

### Hypothesis Testing

The **null hypothesis**, denoted *H*<sub>0</sub> is a statement or claim
about a population characteristic that is initially assumed to be true.

The **alternate hypothesis**, denoted by *H*<sub>*a*</sub> is the
competing claim.  
The alternate hypothesis is a statement about the same population
characteristic that is used in the null hypothesis

Typically one assumes the null hypothesis to be true and then one of the
following conclusions are drawn.

1.  Reject *H*<sub>0</sub>
    -   Equivalent to saying that *H*<sub>*a*</sub> is correct or true
2.  Fail to reject *H*<sub>0</sub>
    -   Equivalent to saying that we have failed to show a statistically
        significant deviation from the claim

Hypothesis form:

*H*<sub>0</sub>: population characteristic = hypothesized value  
where the hypothesized value is a specific number determined by the
problem context.

The alternative (or alternate) hypothesis will have one of the following
three forms:

-   *H*<sub>*a*</sub>: population characteristic &gt; hypothesized value
-   *H*<sub>*a*</sub>: population characteristic &lt; hypothesized value
-   *H*<sub>*a*</sub>: population characteristic ≠ hypothesized value

Errors in Hypothesis Testing:

**Type I error (False Positive)** : The error of rejecting
*H*<sub>0</sub> when *H*<sub>0</sub> is true. Probability of a Type I
error is denoted *α* and is called the **level of significance** of the
test.

**Type II error (False Negative)**: The error of failing to rejected
*H*<sub>0</sub> when *H*<sub>0</sub> is false. Probability of a Type II
error is denoted by *β*.

Refer to wiki on [Type I & II
errors](https://en.wikipedia.org/wiki/Type_I_and_type_II_errors) in
healthcare the results for labs or risk algortims are evaluated by the
positive or negative desscribed as the [sensitivity and
specificity](https://en.wikipedia.org/wiki/Positive_and_negative_predictive_values).
Addiitonally, algorithms are evaluated with the Accuracy (ACC) and the
[ROC
curve](https://en.wikipedia.org/wiki/Receiver_operating_characteristic).

A **test statistic** is the function of sample data on which a
conclusion to reject or fail to reject *H*<sub>0</sub> is based.

The **P-value** (also called the **observed significance level**) is a
measure of inconsistency between the hypothesized value for a population
characteristic and the observed sample. A decision as to whether
*H*<sub>0</sub> should be rejected results from comparing the P-value to
the chosen *α*:

-   Reject *H*<sub>0</sub> if P-value  ≤ *α*.
-   Fail to reject *H*<sub>0</sub> if P-value &gt; *α*.

The **power of a test** is the probability of rejecting the null
hypothesis

When *H*<sub>0</sub> is false, the power is the probability that the
null hypothesis is rejected. Specifically, power = 1 - *β*.

Steps in a Hypothesis-Testing Analysis:

1.  Describe (determine) the population characteristic about which
    hypotheses are to be tested.
2.  State the null hypothesis *H*<sub>0</sub>.
3.  State the alternate hypothesis *H*<sub>*a*</sub>.
4.  Select the significance level *α* for the test.
5.  Display the test statistic to be used, with substitution of the
    hypothesized value identified in step 2 but without any computation
    at this point.
6.  Check to make sure that any assumptions required for the test are
    reasonable.
7.  Compute all quantities appearing in the test statistic and then the
    value of the test statistic itself.
8.  Determine the P-value associated with the observed value of the test
    statistic
9.  State the conclusion in the context of the problem, including the
    level of significance.

<center>
<h4>
Sample Distribution and Hypothesis Testing
</h4>
</center>
1.  Distribution of mean *x̄*: *μ*<sub>*x̄*</sub> = *μ*,
    $\\sigma\_\\bar{x} = \\frac{\\sigma}{\\sqrt{n}}$
2.  Distribution of proportion *p̂*: *μ*<sub>*p̂*</sub> = *p*,
    $\\sigma\_\\hat{p} = \\sqrt{\\frac{p(1-p)}{n}}$

<table>
<colgroup>
<col style="width: 21%" />
<col style="width: 19%" />
<col style="width: 19%" />
<col style="width: 19%" />
<col style="width: 19%" />
</colgroup>
<thead>
<tr class="header">
<th>Estimate</th>
<th>Bound on Error (B)</th>
<th>Confidence Interval</th>
<th>n with 95% confidence</th>
<th>Notes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span class="math inline">$\text{z} = \frac{x- \bar{x}}{\sigma}$</span></td>
<td><span class="math inline">$(\text{z critical value})*(\frac{\sigma}{\sqrt{n}})$</span></td>
<td><span class="math inline"><em>x̄</em> ± <em>B</em></span></td>
<td><span class="math inline">$n = (\frac{1.96\sigma}{B})^2$</span></td>
<td>Critical Value of 95%=1.96</td>
</tr>
<tr class="even">
<td><span class="math inline">$\text{z} = \frac{\hat{p}- p}{\sqrt{\frac{p(1-p)}{n}}}$</span></td>
<td><span class="math inline">$(\text{z critical value})*\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}$</span></td>
<td><span class="math inline"><em>p̂</em> ± <em>B</em></span></td>
<td><span class="math inline">$n = p(1-p)(\frac{1.96}{B})^2$</span></td>
<td>Use p=.5 for conservative estimates of n and always round up.</td>
</tr>
<tr class="odd">
<td><span class="math inline">$t = \frac{\bar{x}-\mu}{\frac{s}{\sqrt{n}}}$</span></td>
<td><span class="math inline">$(\text{t critical value})*(\frac{s}{\sqrt{n}})$</span></td>
<td><span class="math inline"><em>x̄</em> ± <em>B</em></span></td>
<td></td>
<td>df = n-1 and see table for t critical values</td>
</tr>
</tbody>
</table>

### Association and Correlation

**Positive Association** - Two variables are positively associated when
above-average values of one tend to accompany above-average values of
the other and below-average values tend similarly to occur together.
(i.e., Generally speaking, the y values tend to increase as the x values
increase.)

**Negative Association** - Two variables are negatively associated when
above-average values of one accompany below-average values of the other,
and vice versa. (i.e., Generally speaking, the y values tend to decrease
as the x values increase.)

Pearson **Correlation Coefficient**, r, is a measure of the strength of
the linear relationship between the two variables is called the Pierson
correlation coefficient.

**Association or correlation DOES NOT indicate causation**

### Regression and Prediction

Object of a regression analysis is to use information about one
variable, x, predict the value of a second variable, y. Multiple
regression uses multiple variables to predict y.

The most widely used criterion for measuring the goodness of fit of a
line **y = a + bx** to bivariate data
(*x*<sub>1</sub>, *y*<sub>1</sub>), (*x*<sub>2</sub>, *y*<sub>2</sub>), (*x*<sub>*n*</sub>, *y*<sub>*n*</sub>)
is the sum of the of the squared deviations about the line.

$$SSD = \\sum ^n \_{i=1} (y\_i - (a - bx\_i))^2$$

The line that gives the best fit to the data is the one that minimizes
this sum; it is called the **least squares** line or **simple
regression** line. The equation is represented by
***ŷ* = *a* + *b**x***.

The **predicted** or **fitted** values result form substituting each
sample x value into the equation for the least squares line. This gives

*ŷ*<sub>1</sub> = *a* + *b**x*<sub>1</sub> = 1st predicted value
*ŷ*<sub>2</sub> = *a* + *b**x*<sub>2</sub> = 2nd predicted value
*ŷ*<sub>*n*</sub> = *a* + *b**x*<sub>*n*</sub> = nth predicted value

The **residuals** for the least squares line are the values:
*y*<sub>1</sub> − *ŷ*<sub>1</sub>, *y*<sub>2</sub> − *ŷ*<sub>2</sub>, ..., *y*<sub>2</sub> − *ŷ*<sub>2</sub>

The **coefficient of determination**, denoted by *r*<sup>2</sup>, gives
the proportion of variation in y that can be attributed to an
approximate linear relationship between x and y. Note that the
coefficient of determination is the square of the Pearson correlation
coefficient.

The **standard deviation about the least squares line** is denoted
*s*<sub>*e*</sub> is interpreted as the “typical” amount by which an
observation deviates from the least squares line.

A general additive **multiple regression** model
*y* = *α* + *β*<sub>1</sub>*x*<sub>1</sub> + *β*<sub>2</sub>*x*<sub>2</sub> + … + *β*<sub>*k*</sub>*x*<sub>*k*</sub> + *e*

-   Polynomial regression model
    *y* = *α* + *β*<sub>1</sub>*x* + *β*<sub>2</sub>*x*<sup>2</sup> + … + *β*<sub>*k*</sub>*x*<sup>*k*</sup> + *e*  
-   Quadratic regression model
    *y* = *α* + *β*<sub>1</sub>*x* + *β*<sub>2</sub>*x*<sup>2</sup>

**Dummy variables** or **indicator variables** can be created to utilize
categorical variables in a regression model.

The **adjusted R-Squared** adjusts for the amount of explanatory
variables (k) added to the model relative to data points (n).

Regression steps for Bivariate Numeric Dataset

1.  Summarize with scatterplot
2.  Determine linear relationship
3.  Find equation of least-squares regression line
4.  Construct residual plot to look for patterns
5.  Compare *s*<sub>*e*</sub> and *r*<sup>2</sup>
6.  Decide if least-squares line is useful for predictions
7.  Use regression line for prediction

<center>
<big>Correlation and Regression</big>
</center>
<p>
Correlation Coefficient
$r = r\_{xy} = \\frac{\\sum (Z\_x Z\_y)}{n-1} = \\frac{1}{n-1} \\sum ^n \_{i=1} \\left( \\frac{x\_i - \\bar{x}}{s\_x} \\right) \\left( \\frac{y\_i - \\bar{y}}{s\_y} \\right)$

Least Squares Line ***ŷ* = *a* + *b**x*** where

-   Slope of
    $b = \\frac{S\_{xy}}{S\_{xx}} = \\frac{\\sum ((x -\\bar{x})(y -\\bar{y}))}{\\sum (x -\\bar{x})^2}$
-   Intercept of *a* = *ȳ* − *b**x̄*

Residual sum of squares  
$SSResid = \\sum ^n \_{i=1} (y\_i - (a + bx\_i))^2 = \\sum ^n \_{i=1} (y\_i - \\hat{y})^2$  
Total sum of squares, $SSTo = \\sum ^n \_{i=1} (y\_i - \\bar{y})^2$
</p>
<p>
Standard deviation about the least squares line  
$s\_e = \\sqrt{\\frac{SSResid}{n-2}} \\text{ or for multiple regression } s\_e = \\sqrt{\\frac{SSResid}{n-(k+1)}}$  
Standard deviation about the slope (b), confidence interval df = n - 2  
$s\_b = \\frac{S\_e}{\\sqrt{S\_{xx}}}, b \\pm (\\text{t critical value}) s\_b$  
Coefficient of determination

-   $r^2 = 1 - \\frac{\\text{SSResid}}{\\text{SSTo}}$  
-   Adjusted
    $r^2 = 1 - \[\\frac{n-1}{n-(k+1)}\] \\frac{\\text{SSResid}}{\\text{SSTo}}$

</p>
