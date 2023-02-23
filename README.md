# Predicting-Abalone-Age-using-ANN-to-Obtain-Measurements 

For this project, we use a real data on abalone fishing in Australia (taken from http://archive.ics.uci.edu/ml
/machine-learning-databases/abalone). Abalone is a rich nutritious food resource in the many parts of the
world. The economic value of abalone is positively correlated with its age. The age of abalone is determined
by cutting the shell through the cone, staining it, and counting the number of rings through a microscope – a
boring and time-consuming task. Other measurements, which are easier to obtain, are used to predict the
age.

From the original data examples with missing values were removed (the majority having the predicted value
missing), and the ranges of the continuous values have been scaled for use with an ANN (by dividing by 200).
The provided dataset has 4177 rows and 9 columns. Each row corresponds to a particular caught abalone,
and the columns correspond to the following attributes: 

Name / Data Type / Measurement Unit / Description

Sex / nominal / – / M, F, and I (infant)

Length / continuous / mm / Longest shell measurement

Diameter / continuous / mm / perpendicular to length

Height / continuous / mm / with meat in shell

Whole weight / continuous / grams / whole abalone

Shucked weight / continuous / grams / weight of meat

Viscera weight / continuous / grams / gut weight (after bleeding)

Shell weight / continuous / grams / after being dried

Rings / integer / – / +1.5 gives the age in years

By checking the correlation matrix of all of the numeric measurements, or based on common sense, these
measurements are highly correlated. I fit the linear regression including all features, and made the diagnosis
plots and found a couple of outliers and abnormality. Hence I removed these outliers and transformed rings
to be log2(rings). The diagnosis plots improved a little bit. All the following is based on the transformed
data.
