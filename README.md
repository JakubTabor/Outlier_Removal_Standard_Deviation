# Outlier_Removal_Standard_Deviation
# In this "csv" the price column interes me the most
# I plot histogram to look at my price cloumn
# I am gonna remove outliers using percentile technique """df.price.quantile([0.001, 0.999])""" and assign it into "lower_limit, upper_limit"
# Now i have my outliers """outliers = df[(df.price > upper_limit) | (df.price < lower_limit)]""" i take 10 samples of my outliers "outliers.sample(10)"
# I take all of them """df2 = df[(df.price<upper_limit) & (df.price>lower_limit)]""" and assign it into new df2.
# And i look how many outliers i remove """df.shape[0] - df2.shape[0]""" from my df.
# When i get my new df2. i can remove outliers with 4 std. and get my "max_limit" """df2.price.mean() + 4*df2.price.std()""" 
# And "min_limit" """df2.price.mean() - 4*df2.price.std()"""
# I can take my outliers """df2[(df2.price>max_limit) | (df2.price < min_limit)].sample(10)""" a see 10 samples of them
# Now i get my new df3. with outliers """df3 = df2[(df2.price>min_limit) & (df2.price < max_limit)]"""
# And remove them from my df. """df2.shape[0]-df3.shape[0]"""
# Then i plot my new data on histogram using "norm" from "scipy.stats"
