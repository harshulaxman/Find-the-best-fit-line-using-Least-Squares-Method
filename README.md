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
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: HARSSHITHA LAKSHMANAN
RegisterNumber: 212223230075
import numpy as np
import matplotlib.pyplot as plt
#preprocessing data input

x=np.array(eval(input()))
y=np.array(eval(input()))
xmean=np.mean(x)
ymean=np.mean(y)
nume=0    #for slope
denom=0   #for slope

#to dind sum of(xi-x')&(yi-y')&(xi-x')^2
for i in range(len(x)):
    nume+=(x[i]-xmean)*(y[i]-ymean)
    denom+=(x[i]-xmean)**2

    #calculate slope
    m=nume/denom

    #calculate intercept
    b=ymean-m*xmean
    print(m,b)
    #line equation
    ypredicted=m*x+b
    print(ypredicted)

    #to plot graph
    plt.scatter(x,y)
    plt.plot(x,ypredicted,color='red')
    plt.show()


```

## Output:
![image](https://github.com/harshulaxman/Find-the-best-fit-line-using-Least-Squares-Method/assets/145686689/df73a649-b987-4c0f-8d21-52b315cacddb)




## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
