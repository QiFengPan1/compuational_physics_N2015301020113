# 计算物理第三次作业
## 题目描述
Use the Euler method to calculate cannonshell
## 代码实现
```
import matplotlib.pyplot as plt
import math

Y1=[0 for x in range(0,14001)]
X1=[0 for x in range(0,14001)]
VX1=[0 for x in range(0,14001)]
VY1=[0 for x in range(0,14001)]

Y2=[0 for x in range(0,14001)]
X2=[0 for x in range(0,14001)]
VX2=[0 for x in range(0,14001)]
VY2=[0 for x in range(0,14001)]

Y3=[0 for x in range(0,14001)]
X3=[0 for x in range(0,14001)]
VX3=[0 for x in range(0,14001)]
VY3=[0 for x in range(0,14001)]

Y4=[0 for x in range(0,14001)]
X4=[0 for x in range(0,14001)]
VX4=[0 for x in range(0,14001)]
VY4=[0 for x in range(0,14001)]

Y5=[0 for x in range(0,14001)]
X5=[0 for x in range(0,14001)]
VX5=[0 for x in range(0,14001)]
VY5=[0 for x in range(0,14001)]

Y6=[0 for x in range(0,14001)]
X6=[0 for x in range(0,14001)]
VX6=[0 for x in range(0,14001)]
VY6=[0 for x in range(0,14001)]

t=[0 for x in range(0,14001)]

X1[0]=0
Y1[0]=0
VX1[0]=0.7*math.cos(math.pi/4)
VY1[0]=0.7*math.sin(math.pi/4)

X2[0]=0
Y2[0]=0
VX2[0]=0.7*math.cos(math.pi/3)
VY2[0]=0.7*math.sin(math.pi/3)

X3[0]=0
Y3[0]=0
VX3[0]=0.7*math.cos(math.pi/6)
VY3[0]=0.7*math.sin(math.pi/6)

X4[0]=0
Y4[0]=0
VX4[0]=0.7*math.cos(math.pi/5)
VY4[0]=0.7*math.sin(math.pi/5)

X5[0]=0
Y5[0]=0
VX5[0]=0.7*math.cos(math.pi/4.5)
VY5[0]=0.7*math.sin(math.pi/4.5)

X6[0]=0
Y6[0]=0
VX6[0]=0.7*math.cos(math.pi/3.5)
VY6[0]=0.7*math.sin(math.pi/3.5)

T=0.01
t[0]=0


for i in range(1,14001):
    VX1[i]=VX1[i-1]
    VY1[i]=VY1[i-1]-0.0098*T
    X1[i]=X1[i-1]+VX1[i-1]*T
    Y1[i]=Y1[i-1]+VY1[i-1]*T
    VX2[i]=VX2[i-1]
    VY2[i]=VY2[i-1]-0.0098*T
    X2[i]=X2[i-1]+VX2[i-1]*T
    Y2[i]=Y2[i-1]+VY2[i-1]*T
    VX3[i]=VX3[i-1]
    VY3[i]=VY3[i-1]-0.0098*T
    X3[i]=X3[i-1]+VX3[i-1]*T
    Y3[i]=Y3[i-1]+VY3[i-1]*T
    VX4[i]=VX4[i-1]
    VY4[i]=VY4[i-1]-0.0098*T
    X4[i]=X4[i-1]+VX4[i-1]*T
    Y4[i]=Y4[i-1]+VY4[i-1]*T
    VX5[i]=VX5[i-1]
    VY5[i]=VY5[i-1]-0.0098*T
    X5[i]=X5[i-1]+VX5[i-1]*T
    Y5[i]=Y5[i-1]+VY5[i-1]*T
    VX6[i]=VX6[i-1]
    VY6[i]=VY6[i-1]-0.0098*T
    X6[i]=X6[i-1]+VX6[i-1]*T
    Y6[i]=Y6[i-1]+VY6[i-1]*T
    
    t[i]=i*T

plt.axis([0,55,0,20]) 
plt.title('Trajectory of cannon shell')
plt.xlabel('x/km')
plt.ylabel('y/km')
P1=plt.plot(X1,Y1)
P2=plt.plot(X2,Y2)
P3=plt.plot(X3,Y3)
P4=plt.plot(X4,Y4)
P5=plt.plot(X5,Y5)
P6=plt.plot(X6,Y6)

plt.show()
```
## 结果展示
![](https://github.com/QiFengPan1/compuational_physics_N2015301020113/blob/master/Figure_1.png)
