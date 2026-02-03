# PDF_Estimation
Probability Density Function Learning using Nonlinear Transformation
1. Methodology

The project follows these sequential steps:
Data Collection → Data Preprocessing → Feature Transformation → Probability Density Function Modeling → Parameter Estimation (MLE) → Result Analysis → Parameter Submission

2. Description

Dataset used:
India Air Quality Dataset (Kaggle)
https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data

Feature considered:
NO2 concentration as input variable (x)

Nature of data:
Continuous environmental air quality measurements with real-world noise and variability.

The dataset is first cleaned by handling missing values and outliers.
A nonlinear transformation is applied to the NO2 feature using a roll-number-dependent function:

z=x+a_r*sin(b_r*x)
where:
𝑎_r​=0.05(rmod7)
b_r=0.3((rmod5)+1)
r = University Roll Number
This transformation ensures that each student works with a unique modified dataset.
After transformation, a probability density function is learned:
𝑝^(z)=ce^(−λ(z−μ))^2
The parameters 𝜆, μ, and 𝑐 are estimated using Maximum Likelihood Estimation (MLE) to best fit the transformed data.

3. Input / Output
Input:
NO2 concentration values from the air quality dataset
University Roll Number (for transformation parameters)

Output:
Estimated parameters of the probability density function:
Lambda (λ)
Mu (μ)
Normalization constant (c)
Visualizations of original and transformed data distributions
Probability density curve fitted to transformed data

4. Results and Analysis

The nonlinear transformation changes the distribution of NO2 values, introducing controlled variability.
The transformed variable (z) approximately follows a Gaussian-like distribution.
Maximum Likelihood Estimation provides stable and mathematically sound parameter estimates.
The learned PDF effectively models the probability distribution of the transformed data.
Visualization confirms good agreement between empirical histogram and fitted density function.
The results demonstrate that nonlinear feature transformation combined with probabilistic modeling can effectively capture real-world data behavior.

5. Conclusion

This project demonstrates the application of nonlinear feature transformation and probability density estimation on real environmental data.
The use of Maximum Likelihood Estimation ensures statistically reliable learning of distribution parameters.
The approach highlights the importance of preprocessing and transformation in probabilistic machine learning tasks.

Overall, the project successfully models the probability density of transformed NO2 values and provides meaningful parameter estimates for further analysis.

6. GitHub Link

Project Repository:
👉 https:https://github.com/KunalGupta28/PDF_Estimation.git
