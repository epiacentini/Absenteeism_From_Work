# Absenteeism_From_Work

Provided with a data set ~1000 entries related to reasons why people miss time from work and then more specific details about those people.
This includes their age, distance to work, travel expenses, why they have children and ultimately what was their primary reason for being absent.

The data had to be worked on a bit to be fully calibrated for the predictory model (Logistic Regression). This includes feature engineering certain columns such as only utilizing the month values out of the original date column. Addtional examples are condensing the reasons for absence which was initially 29 separate values into only 4 categories making it easier to gain insight and value.

A lot of categorical data had to be converted into dummies in order to be able to be useful to our model such as Education and Reasons for Absence. The data had to be scaled to give more perspective on the values. However, using StandardScaler wouldn't exactly cut it because it interferes with our dummy variables. So ultimately a CustomerScaler was created that would effectively do the same job but only columns of our choosing.

Additionally the classifications of the reasons are listed in the files for those that want more details.

Ultimately, the model can predict with roughly 75% accuracy whether an individual will be excessivley absent and the percentage likelihood that they will be excessively absent. Based on the data provided excessive absence is defined as missing more than 2 hours of that work day. A summary table is constructed at the end and can be read as the coefficient values represent how strong of a factor in absenece. Whereas the odds-ratio column denotes the given odds someone will be excessively absent given that value (i.e. travel expense, having children) is present and cited.

Programming Languages: Python

Tools/Libraries: TensorFlow, Pandas, NumPy, Matplotlib, Seaborn, SciKit-Learn(SKLearn), Jupyter Notebook

Dataset(Kaggle): https://www.kaggle.com/chetnasureka/absenteeismatwork
