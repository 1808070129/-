import numpy as np
import matplotlib.pyplot as plt
data=[(3,2.014,400),(3,1.600,330),(3,2.400,369),(2,1.416,232)]
theta0=0
theta1=0
theta2=0
m=len(data)
alpha=0.001
for i in range(10000):
    h_theta=0
    diff=0
    for point in data:
        x_i_1=point[0]
        x_i_2=point[1]
        y_i=point[2]
        h_theta=theta1*x_i_1+theta2*x_i_2+theta0
        diff=diff+h_theta-y_i
        
        
    theta0=theta0-alpha/m*diff
    theta1=theta1-alpha/m*diff*x_i_1
    theta2=theta2-alpha/m*diff*x_i_2
print(theta0,theta1,theta2)
