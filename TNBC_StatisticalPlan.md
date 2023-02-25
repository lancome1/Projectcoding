# Statistical Analysis Plan for Triple Negative Breast Cancer Project


We will include 604 patients of 24 - 92 years of age who were diagnosed with triple negative breast cancer (TNBC) at Weill Cornell Medicine between 1998 and 2017. 

The primary endpoint for this study is the patient characteristics that manifest the racial disparity. The patient characteristics of interest include: 1) demographical variables (e.g., age at diagnosis); 2) disease history-related variables (e.g., clinical T stage, clinical N stage, index tumor status, past ipsilateral breast cancer, past contralateral breast cancer, tumor size by path or imaging, nodal metastases, histology, high grade, lymphovascular invasion, Ki67, primary laterality); 3) breast cancer management-related variables (e.g., mammographically screening detected, mammographically occult, magnetic resonance imaging screening detected, lumpectomy, mastectomy surgery, contralateral prophylactic mastectomy, sentinel lymph node biopsy, axillary lymph node dissection, neoadjuvant chemotherapy); 4) event-related variables (e.g., estrogen receptor (ER), progesterone receptor (PR), human epidermal growth factor receptor 2 (HER2), laterality for subsequent breast cancer events, overall subsequent breast cancer events, 3-year overall subsequent breast cancer events, 5-year overall subsequent breast cancer events, X-year overall subsequent breast cancer events). The secondary endpoints for this study are the factors associated with the overall subsequent breast cancer events within 5-year follow-up and X-year follow-up, respectively, and the factors associated with the survival time till the overall subsequent breast cancer events. The third endpoints for this study are 1) incidence rates of overall subsequent breast cancer events in 1, 2, 3, 5, and 10 years, respectively; 2) cumulative incidence rates of ER, PR, or HER2- specific overall subsequent breast cancer events in 1, 2, 3, 5, and 10 years, respectively.

In addition, we will estimate the median follow-up time in the entire cohort; the frequency of the overall subsequent breast cancer events; the median time to the overall subsequent breast cancer events from the initial diagnosis of TNBC; the percentage of ER-positive, PR-positive, or HER2-positive among the patients who are diagnosed with a subsequent breast cancer event.

We will check the accuracies of the following date columns in the electronic medical records:  Date Last Follow-up, Date Subsequent BC, and Date Death. We will recode the variable Ki67 in two fashions: 1. use the mid-point method to interpolate the value originally expressed in the range. For example, if the original Ki67 value is 5-10%, the corresponding interpolated value would be 7.5% ((0.05+0.1)/2). The newly constructed variable will be continuous and renamed as Ki.67.2. 2. refer the Updated Recommendations From the International Ki67 in Breast Cancer Working Group (https://academic.oup.com/jnci/article/113/7/808/6053794) to group Ki.67 into three levels: <= 5%, > 5% and <30%, >= 30%.

We will group patients by the following variables: 1) 5 categories of race/ethnicity (i.e., WA, AA, Asian, Hisp/Latina, Other); 2) 4 categories of race/ethnicity (i.e., WA, AA, Asian, Hisp/Latina); 3) 2 categories of race/ethnicity (i.e., WA, Other); 4) 2 categories of subsequent breast cancer events (i.e., Yes, No); 5) 2 categories of 5-year subsequent breast cancer events (i.e., 1 = Yes, 0 = No). Descriptive statistics including mean, standard deviation, median, interquartile range will be calculated to summarize continuous patient characteristics grouped by race/ethnicity or grouped by subsequent breast cancer events. The frequency and percent will be calculated to summarize categorical patient characteristics grouped by race/ethnicity or grouped by subsequent breast cancer events.

We will use the Fisher’s exact test to compare the 1) proportion of certain patient characteristics among the WA, AA, Asian, Hisp/Latina, and Other groups; 2) proportion of certain patient characteristics among the WA, AA, Asian, and Hisp/Latina groups; 3) proportion of certain patient characteristics between the WA and Other groups; 4) proportion of certain patient characteristics between the patients who experience the subsequent breast cancer events, and the patients who do not experience the subsequent breast cancer events; 5) proportion of certain patient characteristics between the patients who experience the 5-year subsequent breast cancer events, and the patients who do not experience the 5-year subsequent breast cancer events, respectively. 

We will use the nonparametric Wilcoxon rank sum test (for two groups comparison) or Kruskal Wallis rank sum test (for more than two groups comparison), as appropriate, to compare the medians in certain patient characteristics among the WA, AA, Asian, Hisp/Latina, and Other groups; among the WA, AA, Asian, and Hisp/Latina groups; between the WA and Other groups; between the patients who experience the subsequent breast cancer events, and the patients who do not experience the subsequent breast cancer events; between the patients who experience the 5-year subsequent breast cancer events, and the patients who do not experience the 5-year subsequent breast cancer events, respectively.

Multivariable logistic regression models will be explored to evaluate the independent effects of patient characteristics of interest on the 5-year/X-year overall subsequent breast cancer events. 
These patient characteristics are the ones that show statistical significance in the associations  with the 5-year/X-year overall subsequent breast cancer events in the Fisher’s exact tests or Wilcoxon rank sum tests.

We will also use univariable cox proportional hazards regression models to examine the crude effects of patient characteristics excluding the event-related variables on the survival time till the overall subsequent breast cancer events. Specifically, multivariable cox proportional hazards regression models will be explored to evaluate the independent effects of patient characteristics of interest, which show statistical significance in univariable cox proportional hazards regression models, on the survival time till the overall subsequent breast cancer events. 

Collinearity between covariates in the regression models will be evaluated prior to the formulation of the final multivariable models. Adjusted regression coefficients and 95% confidence intervals for patient characteristics of interest will be estimated from the multivariable logistic and cox proportional hazards regression models. All adjusted regression coefficient estimates from the multivariable models will serve as preliminary data (i.e., hypothesis-generating) for future studies. 

We will use the Kaplan-Meier estimator to estimate the survival probabilities of the overall subsequent breast cancer events in 1, 2, 3, 5, and 10 years, respectively, then use the formula 1 - survival probability to derive the incidence rates of the overall subsequent breast cancer events in 1, 2, 3, 5, and 10 years, respectively. We will use the cumulative incidence function, which accounts for the competing risk between the positive marker and the negative marker (i.e., ER positive vs ER negative, PR positive vs PR negative, HER2 positive vs HER2 negative), to estimate the cumulative incidence rates of the ER, PR, or HER2- specific overall subsequent breast cancer events in 1, 2, 3, 5, and 10 years, respectively.

All p-values will be two-sided with statistical significance evaluated at the 0.05 alpha level. All analyses will be performed in R Version 4.2.2 (R Foundation for Statistical Computing, Vienna, Austria).