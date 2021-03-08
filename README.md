# Project3
People who exercise for at least 3 hours a week have a lower risk of CVD than sedentary people. 
#generating a p-value from data
import numpy as np
from scipy.stats import ttest_ind
#higher numbers will be given to people at risk for CVD from 1-10)
n = 38
PA = [1, 1, 1, 1, 1, 1, 1, 1, 1, 2, 2, 2, 2, 2, 2, 2, 2 ,2 ,2 ,2 ,2, 2, 2, 3, 3, 3, 3, 3, 3, 3, 3, 3, 3, 4, 4, 4, 4, 4]
no_PA = [6, 6, 6, 6, 6, 6, 6, 6, 7, 7, 7, 7, 7, 7, 7, 9, 9, 9, 9, 9, 9, 9, 9, 9, 9, 9, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10]
hours_PA = 

#create arrays
PA1 = np.array(PA)
PA0 = np.array(no_PA)
#alternate hypothesis: People who exercise for 3 or more hours a week have a low risk of CVD.
#null hypothesis: People who do not exercise have a high risk of CVD. 
print(PA1)
print("PA0 data ::-\n")

#calculate the mean of data sets
PA1_mean = np.mean(PA1)
PA0_mean = np.mean(PA0)

print("PA1 mean value:",PA1_mean)
print("PA0 mean value:",PA0_mean)

#calculate the standard deviation
PA1_std = np.std(PA1)
PA0_std = np.std(PA0)

print("PA1 std value:",PA1_std)
print("PA0 std value:", PA0_std)

#perform a ttest between the data sets
ttest,pval = ttest_ind(PA1, PA0)
print("p-value",pval)

if pval <0.05:
    print("we reject null hypothesis")
else:
    print("we accept null hypothesis")
