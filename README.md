# Ramanujan pi_formula implement on python 
This is ramanujan_PI formula using python 

First found by Mr Ramanujan. This formula used to calculate numerical approximation of pi.

please refer the python code below.

{\frac {1}{\pi }}={\frac {2{\sqrt {2}}}{99^{2}}}\sum _{k=0}^{\infty }{\frac {(4k)!}{k!^{4}}}{\frac {26390k+1103}{396^{4k}}}
Python Code :

import math

#finds factorial for given number
def factorial(x):
if x==0:
return 1
else:
r=x*factorial(x-1)
return r

#computes pi value by Ramanujan formula
#https://www.maa.org/sites/default/files/pdf/upload_library/22/Chauvenet/BorweinBorweinBailey.pdf
def pi_formula():
sum = 0
n = 0
i = (math.sqrt(8))/9801

while True:
tmp = i*(factorial(4*n)/pow(factorial(n),4))*((26390*n+1103)/pow(396,4*n))
sum +=tmp

if(abs(tmp) < 1e-15):
break
n += 1

return(1/sum)

print(“Pi value using Ramanujan Formula : “,pi_formula())





# The formula of Pi can be expressed as,
Circumference / Diameter = π = 3.14159… or 22/7.
Circumference of Circle = 2πr. Area of circle = πr2 Surface Area of Circle = 4πr2 Volume of a sphere = 4/3 πr3
Given: The perimeter of a circular pipe = 84 inches. By Using pi formula, We have , Pi(π) = (Circumference / Diameter)
