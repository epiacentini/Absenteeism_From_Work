# Absenteeism_From_Work

Provided with a data set ~1000 entries related to reasons why people miss time from work and then more specific details about those people.
This includes their age, distance to work, travel expenses, why they have children and ultimately what was their primary reason for being absent.

The data had to be worked on a bit to be fully calibrated for the predictory model (Logistic Regression). This includes feature engineering certain columns such as only utilizing the month values out of the original date column. Addtional examples are condensing the reasons for absence which was initially 29 separate values into only 4 categories making it easier to gain insight and value.

A lot of categorical data had to be converted into dummies in order to be able to be useful to our model such as Education and Reasons for Absence. The data had to be scaled to give more perspective on the values. However, using StandardScaler wouldn't exactly cut it because it interferes with our dummy variables. So ultimately a CustomerScaler was created that would effectively do the same job but only columns of our choosing.
