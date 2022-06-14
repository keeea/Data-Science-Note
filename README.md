# Inferential Statistics
## CLT and Sampling

### Standard Error
- Population standard deviation: σ
- Sample standard deviation: s
- Know σ: 
<img width="82" alt="image" src="https://user-images.githubusercontent.com/90301308/173152323-59065ef9-f361-4f54-91ca-6c5c0b54da73.png">

- Don't know σ: 
<img width="81" alt="image" src="https://user-images.githubusercontent.com/90301308/173152512-5afee502-c9d0-4542-b166-cc710b13c1e0.png">

### SD (σ or s) and SE（standard error): 
s: variability in sample data

SE: variability in point estimates from different samples of the same size and from the same population.

σ: variability in population data

### SE over Sample Size
As sample size n increase, sampling variability / SE is expected to decrease.

### Sample Distribution VS Sampling Distribution 
Every observatioon in the **sample distribution** is a **randomly sampled unit**, while every observation in **sampling distribution** is a **sample statistic**.

### Central Limit Theorem (CLT) Definition $ Conditions: 
CLT is about the  **distribution of point estimates**, and that given certain conditions, this  distribution will be **nearly normal**.
In the case of the **mean** the CLT tells us that if
(1a) the sample size is sufficiently large (n ≥ 30 or larger if the data are considerably skewed), or 

(1b) the population is known to have a normal distribution, and 

(2) the observations in the sample are independent, 
- random sample/assignment
- if sampling without replacement, n < 10% of population

then  the distribution of the sample mean will be nearly normal, centered at  the true population mean and with a standard error equal to the population standard deviation devided by the square root of the sample size.

<img width="349" alt="image" src="https://user-images.githubusercontent.com/90301308/173204255-aa1bbb97-a178-4ef4-b9e4-b9f5d716b9ff.png">

When  the population distribution is unknown, condition (1a) can be checked  using a histogram or some other visualization of the distribution of the  observed data in the sample. 

The larger the sample size (n), the  less important the shape of the distribution becomes, i.e. when n is  very large the sampling distribution will be nearly normal regardless of  the shape of the population distribution. 

### Application of CLT
**Q: Probability that mean/sum in a specific sample is at least xxx**

**A: Z-score to Prob**
1. In most case, CLT will not be directly applied to the individual observations, but mean or sum/size. 
2. And if the population distribution isn't normal, you could not apply Z-score to calculate probability.

## Confidence Intervals

### Confidence interval Definition & Interpretation 
- The plausible range of values for **a population parameter**. 
- point estimate ± z × SE (z is always a positive cutoff)
- Interpretation: “We are XX% confident that the true  population parameter is in this interval”

### CI Conditions:
1. **Independence**: Sampled observations must be independent.
- random sample/assignment
- if sampling without replacement, n < 10% of population
2. **Sample size/skew**: **n ≥ 30**, larger if the population distribution is very skewed.

### Margin of Error (ME) = z × SE
ME is the **degree of error** in results received from random sampling.

Approximate 95% CI: x bar ± **2SE**

### Confidence Level
The **percentage of random samples** which  yield confidence intervals that capture the true population parameter. 

Commonly used confidence levels in practice are 90%, 95%, 98%, and 99%.

### Accuracy VS Precision
**When Confidence Level+**

CI Width+  Accuracy+  Precision-

**When sample size +**

SE- ME- Precision+  Accuracy+

**How to increase both Accuracy and Precision?**
Increase sample size.
SE-  EM-  Width-  Precision+

### Required Sample Size for ME/Cl
<img width="365" alt="image" src="https://user-images.githubusercontent.com/90301308/173298945-6a77e175-b59e-4853-abf7-797506e68a3d.png">
- Round up
- To cut the margin of error by **half**, we need to **quadruple** our sample size

### Application of CI
- **Q: Given sample mean, sample sd, sample size, CL, what is population mean?**

- **Interpretation**:  **We are 95% confident that** Americans on average, have **3.40 to 4.24** bad mental health days per months.

- **What does a 95% CL mean in the context?**:  95% of **random samples** of **1151** Americans will yield confidence intervals that capture the true **population mean** of number of bad mental health days per month.

## Hypothesis Testing

### Hypothesis Claims:
1. **Null hypothesis**, which represents a skeptical perspective or the status quo, and 

2. **Alternative hypothesis**, which represents an alternative under consideration and is often represented by a range of possible parameter values.

- Note that the alternative hypothesis might be **one-sided** (μ < or > the null value) or **two-sided** (μ≠ the null value), and the choice depends on the research question. 

### Two Ways to Conduct hypothesis test
1. Simulation
2. Theoretical - rely on the CLT


### P-value
1. **Defination**: 

p-value is the **conditional probability** of obtaining a sample statistic **at least as extreme** as the one observed given that the **null hypothesis is true**. 

p−value=P(observed or more extreme sample statistic | H0 true)

2. **Calculation**: 

Calculate a p-value as the area under the **normal curve** beyond the **observed sample mean** (either in one tail or both, depending on the alternative hypothesis). Note that in doing so you can use a **Z score**.

3. **Interpretation:**

If in fact college students have been in 3 exclusive relationships on average, there is a 21% chance
that a random sample of 50 college students would yield a sample mean of 3.2 or higher


### Decision between the hypotheses
1. **with P-value**:

If the **p-value < the significance level**, r**eject the null hypothesis** since this means that obtaining a sample statistic at least as extreme as the observed data is **extremely unlikely** to happen just by chance, and conclude that the data provides evidence for the alternative hypothesis. 

If the **p-value > the significance level**, f**ail to reject the null hypothesis** since this means that obtaining a sample statistic at least as extreme as the observed data is **quite likely** to happen by chance, and conclude that the data does not provide evidence for the alternative hypothesis. 

2. **with Confidence interval**:

if a confidence interval **does not contain** the null value the null hypothesis should be **rejected** in favor of the alternative. 


### Hypothesis Testing Process
<img width="894" alt="image" src="https://user-images.githubusercontent.com/90301308/173486498-ad385a69-49c5-4504-bc8e-6651c9d0d666.png">


### Two Sided/Tailed Test
- We are interested in divergence in both direction.
- Calculation of p-value is different 
<img width="851" alt="image" src="https://user-images.githubusercontent.com/90301308/173486674-71697f73-f363-4f4f-86b1-7fde3089872d.png">


## Significance

### Sample Size
Calculate the required sample size to obtain a **given margin of error** at a **given confidence level** by working backwards from the given margin of error. 

### Otehr Unbiased Estimator
They also need to have nearly normal sampling distributions
<img width="560" alt="image" src="https://user-images.githubusercontent.com/90301308/173491867-f2c4c8b6-fa55-4491-8c4e-ec494b26e027.png">


### Two type of error Definition
- **Type 1** error is rejecting H0 when H0 is trueand, and the probability of doing so is α (significance level).
- **Type 2** error is failing to reject H0 when HA is true, and the probability of doing so is β.
- **Power** of a test is the probability of correctly rejecting H0, and the probability of doing so is 1 − β


### Chosing α(significance level) Based on Error
- Use a **smaller α** if **Type 1** error is relatively **riskier**.  
- Use a **larger α** if **Type 2** error is relatively **riskier**. 


### Type 2 Error Rate
- If the true **population average** is very **close** to the **null value**, it will be **difficult** to detect a difference (and reject H0).
- If the true **population average** is very **different** from the null value, it will be **easier** to detect a difference.
- Clearly, β depends on the **effect size (δ)**, difference between point estimate and null value.


### Agreement of CI and HT
- A **two sided** hypothesis with threshold of α is equivalent to a confidenceinterval with **CL = 1 − α.**
- A **one sided** hypothesis with threshold of α is equivalent to a confidence interval with **CL = 1 − (2 x α).**
- If **H0 is rejected**, a confidence interval that agrees with the result of the hypothesis test should **not include** the null value.
- If H0 is **failed to be rejected**, a confidence interval that agrees with the result of the hypothesis test should **include** the null value.

### Statistical vs. Practical Significance
Bigger sample size - Smaller SE - Bigger Z - Smaller p-value 
Very **large samples** will result in statistical significance even for **tiny** differences between the 
sample mean and the null value (**effect size**), even when the difference is not practically significant.
