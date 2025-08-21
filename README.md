# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
import numpy as np
import matplotlib.pyplot as plt

X = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
Y = np.array([1, 3, 2, 5, 7, 8, 8, 9, 10, 12])

XMean = np.mean(X)
YMean = np.mean(Y)

num, den = 0, 0
for i in range(len(X)):
    num += (X[i] - XMean) * (Y[i] - YMean)
    den += (X[i] - XMean) ** 2

m = num / den
c = YMean - m * XMean

print(m, c)

Y_Pred = m * X + c
print(Y_Pred)

plt.scatter(X, Y)
plt.plot(X, Y_Pred, color="red")
plt.show()
```

## Output:

8,2,11,6,5,4,12,9,6,1
3,10,3,6,8,12,1,4,9,14
Register number:25018038
Name:shivaji.k
Slope: -1.1064189189189189
Y-intercept: 14.08108108108108
Predicted value: [ 5.22972973 11.86824324  1.91047297  7.44256757  8.54898649  9.65540541
  0.80405405  4.12331081  7.44256757 12.97466216]

  
<img width="543" height="413" alt="7c989425-2cdf-4d4f-8947-2dc6c0f7c77c" src="https://github.com/user-attachments/assets/4d5fd910-c90c-4396-bd9f-24391484d7de" />



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
