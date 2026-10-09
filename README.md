# MexEE 402: Data Preprocessing Case Study

MexEE Elective 2: Data Science and Machine Learning
Batangas State University, Alangilan Campus
1st Semester, AY 2026-2027

## Members

| Name | Student Number | Section |
|---|---|---|
| Javier, Kim Ivan | 22-03673 | MEXE - 4103 |
| Delgado, Clifford Rhey | 22-05989 | MEXE - 4103 |

## Notebook links

| Chapter | Javier, Kim Ivan | Delgado, Clifford Rhey |
|---|---|---|
| Ch1_2_3 | [link]() | [Ch1_2_3_Javier_Delgado](https://colab.research.google.com/drive/14aqgsxow75-BFjWPJoF8NABdo5TlXAjP?usp=drive_link#scrollTo=0XpkrsEz8gCQ) |
| Ch4 | [link]() | [Ch4_Javier_Delgado](https://colab.research.google.com/drive/1-MZKjrRcKHC4EKrwICXZTHo51luPhzfK?usp=drive_link) |
| Ch5 | [link]() | [Ch5_Javier_Delgado](https://colab.research.google.com/drive/1z4X_GhpbFY4Yq5Ab3GbbA5XKKNvD3ln4?usp=drive_link) |
| Ch6 | [Ch6_Javier_Delgado](https://colab.research.google.com/drive/19CsWIEosqFsNR1mbMvHjfhE49Ku3z3h8?usp=sharing) | [link]() |
| Ch7 | [Ch7_Javier_Delgado](https://colab.research.google.com/drive/19NtSVNxichdyE5jYDYOYamNVKmzeFr_k?usp=sharing) | [link]() |
| Ch8 | [Ch8_Javier_Delgado](https://colab.research.google.com/drive/1hLlKJ2xjxH5CCNC5InxjSGGaAikmvqdT?usp=sharing) | [link]() |
| Ch9 | [Ch9_Javier_Delgado](https://colab.research.google.com/drive/18X9cI27vnHStvXqV9T0l-PMHOomjrEny?usp=sharing) | [link]() |

## What we learned

#### CHAPTER 1_2_3

This chapter taught me that raw data is almost never ready to use. I finally understood that cleaning is not just “fixing mistakes” but deciding what information is actually useful. What surprised me was how much a single column like Rank could quietly mess things up even though it looked important at first.

#### CHAPTER 4

I learned that creating new features can reveal relationships that the original columns hide. The idea of combining variables to make something more meaningful finally clicked. What surprised me was how something as simple as dividing two numbers could give a clearer story than looking at the raw values alone

#### CHAPTER 5

This chapter showed me that numbers can lie just by being bigger. I understood that models don’t automatically know which features matter more, they just react to the size of the numbers. What surprised me was realizing that without scaling, a model could completely ignore an important variable simply because its values were smaller.

#### CHAPTER 6

This chapter “Dealing with Outliers” taught me that outliers are data points that are very different from most of the values and can affect the results of data analysis. I learned how the Z-score and IQR methods can be used to identify these unusual values and why they need to be checked before analyzing or building a model. What surprised me was that even one extreme value can skew the results and lead to incorrect interpretations, so handling outliers is important for getting more reliable results.

#### CHAPTER 7

This chapter “Feature Selection” taught me that correlation helps determine how variables are related and can help identify which features are useful for analysis or prediction. I learned that correlation can be positive, negative, or zero, with values ranging from -1 to 1. What surprised me was that a high correlation shows that two variables move together, but it does not necessarily mean that one variable causes the other.

#### CHAPTER 8

This chapter “Constructing a Preprocessing Pipeline” taught me that a pipeline organizes different data preprocessing steps into one automatic and sequential process. I understood that it can make data preparation more efficient, consistent, and less prone to errors, especially when working with datasets like Titanic. What surprised me was how a pipeline can handle several preprocessing tasks together instead of doing each step manually.

#### CHAPTER 9

This chapter “Real-World Application: Data Preprocessing” taught me how to apply different preprocessing techniques to a real dataset like the Titanic dataset. I learned that data needs to be cleaned, transformed, reduced, discretized, and encoded before it can be properly used for analysis or machine learning. What surprised me was that preprocessing is not always a one-time process because some steps may need to be revisited and adjusted depending on the data.



## Errors we found


#### CHAPTER 1_2_3: DATA IMPUTATION

MISTAKE: A value is trying to be set on a copy of a DataFrame or Series through chained assignment using an inplace method.
The behavior will change in pandas 3.0. 

ORIGINAL CODE:
<img width="1738" height="266" alt="Screenshot 2026-10-09 134745" src="https://github.com/user-attachments/assets/bbe8a9b5-6ee9-498c-b7db-723f74943485" />


CORRECT VERSION:

<img width="677" height="67" alt="Screenshot 2026-10-09 141909" src="https://github.com/user-attachments/assets/68da9e12-263e-4758-93a1-1a5598a16329" />


#### CHAPTER 6: DEALING WITH OUTLIERS
MISTAKE:The original notebook states that 100 is a clear outlier using the Z-score method.

CORRECT VERSION:

The Z-score of 100 is approximately 2.61501265, which is within the ±3 cutoff. Therefore, 100 is not classified as an outlier using the Z-score method. However, the IQR method identifies 100 as an outlier. This shows that the classification depends on the method used.

#### CHAPTER 7: FEATURE SELECTION

MISTAKE:The main issue is that five-fold cross-validation creates validation folds with fewer than two samples, making the R^2
score undefined. Reducing the number of folds or using a suitable scoring metric can help address the issue.

ORIGINAL CODE:
<img width="1565" height="262" alt="Screenshot 2026-10-09 145600" src="https://github.com/user-attachments/assets/69eef75a-1aae-4b03-bd24-7654402874a4" />


CORRECT VERSION:
<img width="937" height="362" alt="Screenshot 2026-10-09 152742" src="https://github.com/user-attachments/assets/bb043a0c-e529-41cc-80bf-7fb27ce0cdab" />


## Note on AI tools

Say whether you used an AI tool, and what for. This is not a penalty.
Hiding it is.


## References

McKinney, W. (2021). Python for Data Analysis, 3rd ed. O'Reilly.
VanderPlas, J. Python Data Science Handbook.
Any other page or article you used.
