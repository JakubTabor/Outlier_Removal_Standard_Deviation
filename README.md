# Outlier_Removal_Standard_Deviation
# In this "csv" the price column interes me the most
# I plot histogram to look at my price cloumn
# I am gonna remove outliers using percentile technique """df.price.quantile([0.001, 0.999])""" and assign it into "lower_limit, upper_limit"
# Now i have my outliers """outliers = df[(df.price > upper_limit) | (df.price < lower_limit)]""" i take 10 samples of my outliers "outliers.sample(10)"
