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
SE **ONLY** represent variability in point estimates/**sampling distribution** from different samples of the same size and from the same population.

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
**Q: Probability that mean/sum is at least xxx**
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
Approximate 95% CI: x bar ± **2SE**

### Confidence Level
The **percentage of random samples** which  yield confidence intervals that capture the true population parameter. 

Commonly used confidence levels in practice are 90%, 95%, 98%, and 99%.

### Accuracy VS Precision
Confidence Level+  CI Width+  Accuracy+  Precision-

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
