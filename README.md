# Hippo_VBM
This repository contains the results of a study analyzing volumetric variables derived from VolBrain data of healthy subjects' hippocampi. The study focuses on examining the effects and interactions of sex and age on hippocampal volumes

## Volume Loss
The findings highlight significant sex differences in the volumetric changes of hippocampal subfields with age. Males generally exhibit greater volume loss in several regions, particularly the CA2_3 subfield, and show increases in certain asymmetries. Conversely, females show either stable volumes or less pronounced changes. These differences underscore the importance of considering sex as a factor in studies of hippocampal aging and its implications for cognitive health.

Hippocampus Total Volume:

Males show a significant decline in hippocampal total volume with age (slope = -0.0137, p = 0.003), while females do not exhibit a significant change (slope = 0.0026, p = 0.673).
CA1 Total Volume Percent:

A notable difference is observed in the CA1 total volume percent between sexes. Males have a positive slope (0.5243, p = 0.038), indicating an increase, whereas females have a slight negative slope (-0.0730, p = 0.616). This difference is statistically significant, as shown by the U-test results (u-statistic = 0.87, p-value = 0.021), indicating a greater increase in CA1 volume percent with age in males compared to females.
CA2_3 Total Volume:

Both males and females experience a decline in CA2_3 total volume with age, but the rate of decline is more pronounced in males (slope = -0.0033, p = 0.000006) compared to females (slope = -0.0014, p = 0.106).
Asymmetry:

In terms of asymmetry, males show an increase in asymmetry for several subfields, while females exhibit a decrease or less pronounced changes. For example, males show an increase in CA4/DG asymmetry (slope = 0.080, p = 0.134), while females show a decrease (-0.018, p = 0.672).

Key Volumetric Variables:

Hippocampus Total Volume:
The significant volume loss in males (p = 0.003) compared to the non-significant change in females suggests that aging may have a more pronounced impact on hippocampal atrophy in males.

CA1 Total Volume Percent:
The increase in CA1 volume percent in males (p = 0.038) versus a decrease in females indicates potential sex-specific differences in how this subfield responds to aging. This could reflect differential vulnerability or compensatory mechanisms between sexes.

CA2_3 Total Volume:
The steeper decline in CA2_3 volume in males highlights a potential area of concern, suggesting that this subfield may be more susceptible to age-related atrophy in males.

![volume loss](https://github.com/Sebarz98/Hippo_VBM/assets/70062910/0379a1de-7f38-4648-8302-0b72e6536268)

The attached plot visually represents these findings, showing the slope of volume loss with age for various hippocampal subfields. Positive slopes indicate volume increases with age, while negative slopes indicate volume loss. The differing slopes between males (blue) and females (orange) across variables illustrate the sex-specific patterns of hippocampal aging, with significant differences noted in key subfields such as CA1 total percent and CA2_3 total volume.

 ## Mixed Model
 In this study, a linear mixed-effects model was employed to analyze the volumetric variables of the hippocampus derived from VolBrain data. The model incorporated both fixed effects (age group, sex, and their interaction) and random effects (subject-specific variations) to account for the hierarchical structure of the data. Specifically, the formula used was {var} ~ Age_Group * Sex, with Patient_ID as the grouping variable for random effects. 
 The comparison age group is the 40-49. 

For hippocampal asymmetry, significant interactions between sex and age groups were observed. Males generally exhibited higher asymmetry than females, but this effect varied across age groups. Specifically, negative coefficients for interaction terms (e.g., Age_Group[T.50-59], Age_Group[T.60-69]) indicate that the degree of asymmetry differed between sexes more prominently in these age groups. For instance, the coefficient for Age_Group[T.60-69] is -13.433 (p = 0.002), suggesting that within this age group, the difference in hippocampal asymmetry between males and females is significantly pronounced​​.

In terms of total hippocampal volume, sex also showed a significant main effect and interaction with age groups. For example, the interaction term Age_Group[T.70-79] had a positive coefficient of 1.102 (p = 0.009), indicating that the difference in hippocampal volume between males and females in this age group is substantial. This suggests that as age increases, the volumetric differences between sexes become more evident. 

The mixed linear model for CA1 total volume revealed a significant effect of the interaction between age group and sex. Specifically, the interaction term for the 60-69 age group and sex was significant, with a coefficient of -255.467 (p = 0.002), indicating that the difference in CA1 total volume between males and females is substantial in this age group. The main effect of the 60-69 age group was also significant (coef = 510.940, p < 0.001), suggesting a notable increase in CA1 volume for this age group compared to the reference group.

Analysis of CA1 right volume indicated a significant interaction between the 70-79 age group and sex, with a positive coefficient of 0.473 (p = 0.005). This result suggests that, within this age group, males and females show significant differences in CA1 right volume. Additionally, the main effect of sex was significant (coef = -0.218, p = 0.024), with males generally having smaller CA1 right volumes than females.

For CA1 left volume, the interaction between the 70-79 age group and sex was significant (coef = 0.551, p = 0.001), indicating a pronounced difference in CA1 left volume between males and females in this age group. The main effect of sex was also significant (coef = -0.285, p < 0.001), showing that males tend to have smaller CA1 left volumes compared to females.

Males generally exhibited higher CA1 Hippocampal asymmetry than females (β = 4.141, p < 0.001).
Significant interactions between sex and age groups were observed.
Age_Group[T.50-59](β = -4.256, p = 0.030), Age_Group[T.60-69](β = -5.860, p = 0.022), and Age_Group[T.80-89](β = -5.602, p = 0.020) showed notable differences in asymmetry between sexes across different age groups.

CA2/3 Total Volume:
Significant main effect of sex (β = -0.063, p < 0.001), indicating lower total volume in males. Interaction term Age_Group[T.70-79](β = 0.118, p = 0.021) highlighted increased volumetric differences between males and females in the 70-79 age group.

CA2/3 Right Hemisphere Volume:
Main effect of sex (β = -15.889, p = 0.112) with indications of larger volumetric differences in the 60-69 age group (β = -12.416, p = 0.102), though not statistically significant.

CA2/3 Left Hemisphere Volume:
No significant main effect of sex (β = -0.039, p = 0.996). Interactions with age group, such as Age_Group[T.50-59] (β = -13.928, p = 0.223), did not reach statistical significance.

CA2/3 Total Percent Volume:
No significant main effect of sex (β = 0.001, p = 0.612) on percentage volume.Age_Group[T.70-79](β = 0.009, p = 0.038) indicated increasing sex differences in volume percentage in the 70-79 age group.

CA2_3_Asymmetry:
No significant main effect of sex (β = 4.307, p = 0.331) on CA2/3 asymmetry.
Significant main effect of age group (Age_Group[T.100+]: β = -147.431, p < 0.001), indicating higher asymmetry in the oldest age group.
Age_Group[T.50-59](β = -11.314, p = 0.084) and Age_Group[T.60-69] (β = -8.690, p = 0.118) showed trends towards interaction, suggesting potential sex differences in asymmetry across these age groups.

CA4_DG_Total_cm3:
Significant main effect of age group (Age_Group[T.60-69]: β = 225.063, p < 0.001), indicating significantly larger total volume in the 60-69 age group.
No significant main effect of sex (β = -0.232, p = 0.991) on total volume.
Age_Group[T.60-69](β = -112.499, p < 0.001) showed a significant interaction, suggesting sex-specific differences in total volume particularly in the 60-69 age group.

CA4_DG_Right_cm3:
Significant main effect of age group (Age_Group[T.80-89]: β = 102.941, p = 0.007), indicating larger right hemisphere volume in the 80-89 age group.
No significant main effect of sex (β = -0.097, p = 0.993) on right hemisphere volume. 
Age_Group[T.80-89](β = -51.477, p = 0.022) showed a significant interaction, suggesting sex-specific differences in right hemisphere volume in the 80-89 age group.

CA4_DG_Left_cm3:
Significant main effect of sex (β = 22.528, p = 0.001), indicating larger left hemisphere volume in males.
No significant main effect of age group on left hemisphere volume.
Age_Group[T.50-59](β = -22.602, p = 0.052) showed a trend towards interaction, suggesting potential sex-specific differences in left hemisphere volume in the 50-59 age group.

## Multivariate Analysis of Covariance (MANCOVA)

The multivariate analysis of covariance (MANCOVA) was conducted to assess the effect of Age Group, Sex, and their interaction on the dependent variables. The MANCOVA revealed significant multivariate effects for the intercept, Age Group, and Sex, but not for the interaction between Sex and Age Group.

Multivariate Tests
Intercept: The results for the intercept indicated a highly significant multivariate effect across all test statistics, including Wilks' lambda (Λ = 0.0062, F(26, 258) = 1598.4961, p < 0.0001), Pillai's trace (V = 0.9938, F(26, 258) = 1598.5534, p < 0.0001), Hotelling-Lawley trace (T = 161.0887, F(26, 258) = 1598.4958, p < 0.0001), and Roy's greatest root (Θ = 161.0887, F(26, 258) = 1598.4958, p < 0.0001).

Age Group: The effect of Age Group showed significant results on several multivariate tests, with Wilks' lambda (Λ = 0.4542, F(182, 1761.5761) = 1.1946, p = 0.0462), and Hotelling-Lawley trace (T = 0.8620, F(182, 1355.3897) = 1.2143, p = 0.0351) being significant. However, Pillai's trace (V = 0.7259, F(182, 1848) = 1.1748, p = 0.0632) approached significance, while Roy's greatest root (Θ = 0.3040, F(26, 264) = 3.0866, p < 0.0001) indicated a strong effect.

Sex: There was a significant multivariate effect of Sex across all tests: Wilks' lambda (Λ = 0.7954, F(26, 258) = 2.5519, p < 0.0001), Pillai's trace (V = 0.2046, F(26, 258) = 2.5519, p < 0.0001), Hotelling-Lawley trace (T = 0.2572, F(26, 258) = 2.5519, p < 0.0001), and Roy's greatest root (Θ = 0.2572, F(26, 258) = 2.5519, p < 0.0001).

Sex by Age Group Interaction: The interaction between Sex and Age Group did not show a significant multivariate effect based on Wilks' lambda (Λ = 0.4944, F(182, 1761.5761) = 1.0593, p = 0.2887), Pillai's trace (V = 0.6582, F(182, 1848) = 1.0539, p = 0.3046), and Hotelling-Lawley trace (T = 0.7557, F(182, 1355.3897) = 1.0645, p = 0.2768). However, Roy's greatest root (Θ = 0.2154, F(26, 264) = 2.1875, p = 0.0011) indicated a significant interaction.

These results suggest that while both Age Group and Sex individually have significant effects on the dependent variables, their interaction does not contribute significantly to the model, except as indicated by Roy's greatest root.

## Principal Component Analysis (PCA)
The PCA results reveal that the primary sources of variability in hippocampal volumetric measures are differentially influenced by sex and age. Specifically, age is a significant factor for the total volume of the hippocampus (PC1), while sex significantly influences the percentage volumes (PC4 and PC5). These findings underscore the importance of considering both sex and age when studying hippocampal structure and its changes over time.

![pca](https://github.com/Sebarz98/Hippo_VBM/assets/70062910/9fe7df1b-2530-4c0b-9350-dbec3cf06e19)

Explained Variance:

The first principal component (PC1) accounts for the largest proportion of variance in the data, capturing approximately 20% of the total variance. This component is predominantly associated with the total volume of the hippocampus.
The first five principal components (PC1 to PC5) cumulatively explain around 50% of the variance, with the variance contribution gradually decreasing for subsequent components.
The cumulative variance explained by the first 28 principal components reaches close to 90%, indicating that these components capture most of the variability in the dataset.
ANOVA Results:

PC1 (Hippocampus_Total_cm3):
The analysis of variance (ANOVA) results for PC1 show that sex is not a significant factor (F = 0.6127, p = 0.4344). However, age group is a significant factor (F = 2.5889, p = 0.0133), suggesting that variations in hippocampal total volume are significantly associated with age but not sex.
PC2 (Hippocampus_Right_cm3):
For PC2, neither sex (F = 1.9250, p = 0.1664) nor age group (F = 0.8314, p = 0.5619) are significant factors, indicating that the variance captured by this component is not strongly influenced by these variables.
PC3 (Hippocampus_Left_cm3):
The results for PC3 indicate that sex is not a significant factor (F = 0.2103, p = 0.6468), and age group is marginally non-significant (F = 2.0174, p = 0.0529). This suggests a weak influence of age on the variance captured by this component.
PC4 (Hippocampus_Total_percent):
For PC4, sex is a highly significant factor (F = 17.1580, p = 0.000045), indicating that the variance in hippocampal total percent volume is strongly associated with sex. Age group is not a significant factor (F = 1.1530, p = 0.3300) for this component.
PC5 (Hippocampus_Right_percent):
The ANOVA results for PC5 show that sex is a significant factor (F = 6.8466, p = 0.0093), whereas age group is not significant (F = 0.7843, p = 0.6009), indicating that this component's variance is significantly influenced by sex but not by age.

## K-means Clustering 
The K-means clustering results are visualized in the attached plot, which displays the distribution of clusters based on the first two principal components derived from PCA. The features contributing the most to these principal components were identified and used as labels for the axes.

![cluster](https://github.com/Sebarz98/Hippo_VBM/assets/70062910/d5f14aa2-b101-4d2b-87bc-02e4555ba7a7)


PCA and Feature Contribution:
Principal Component 1 (PC1):
The top contributing features for PC1 are Sex, ICV_cm3, and CA1_Right_percent. These features combined capture the most variance in the data along the first principal component.
Principal Component 2 (PC2):
The top contributing features for PC2 are CA2_3_Right_percent, Hippocampus_Right_percent, and Age. These features are the primary drivers of variance along the second principal component.

Cluster Analysis:
The plot shows the clusters in a 2-dimensional PCA space, with the x-axis representing the combination of Sex + ICV_cm3 + CA1_Right_percent and the y-axis representing CA2_3_Right_percent + Hippocampus_Right_percent + Age.
Different symbols and colors represent different clusters, with the legend indicating sex (1.0 for male, 2.0 for female) and various age groups (0 through 9).
Interpretation:

The majority of the data points are concentrated near the origin, indicating that most subjects have similar values for the combined features.
A few outliers are spread out along the x-axis and y-axis, suggesting some variation in the dataset that might be due to the combined effects of sex, intracranial volume (ICV), hippocampal subfield volumes, and age.
The clustering reveals distinct groups in the data, although there is some overlap between clusters, particularly near the origin. This overlap might suggest subtle differences in the features that contribute to the variance captured by PC1 and PC2.
