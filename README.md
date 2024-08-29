# Current calculator I am working on
PROPORTIONS codes
n1= 1
d1=2
n2=0
d2=16

if n2==0:
    answer=n1*d2/d1
    print("n2= ",answer)
  

    EXTRA PROBLEMS FOR SOLVING FOR X
    # converts string input (even fractions) to float
def string_frac(in_string):
    if "/" in in_string:
        nd = in_string.split("/")
        n = float(nd[0])
        d = float(nd[1])
        ans = n/d
        return ans
    else:
        ans = float(in_string)
        return ans


# Simplest one-step addition
def one_step_add():
    import random
    # Display problem
    a = random.randint(-4,10)
    b = random.randint(2,24)
    print("x + ", a, " = ", b)
    ans = float(input("x = "))
    answer = b-a
    # Test input
    if ans==answer:
        print("Correct! \n")
    else:
        print("Try again")
        print("The correct answer is ", answer, "\n")


# One-step additon with negaive numbers
def one_step_subtract():
    import random
    a = random.randint(-19,-1)
    b = random.randint(2,24)
    print(a, " + x = ", b)
    ans = float(input("x = "))
    # test
    answer = b-a
    if ans==answer:
        print("Correct! \n")
    else:
        print("Try again")
        print("The correct answer is ", answer, "\n")

# One-step multiply
def one_step_mult():
    # Uses string_frac(<input string>)
    import random
    a = random.randint(1,11)
    b = random.randint(2,24)
    print(a, "x = ", b)
    print("Round your answer to two decimal places.")
    ans_in = (input("x = "))
    answer = round(b/a,2)
    # test
    if string_frac(ans_in)==answer:
        print("Correct! \n")
    else:
        print("Try again")
        print("The correct answer is ", answer, "\n")


# One-step divide
def one_step_div():
    import random
    a = random.randint(1,11)
    b = random.randint(2,24)
    print("x/", a, " = ", b)
    ans = float(input("x = "))
    answer = b*a
    # test
    if ans==answer:
        print("Correct! \n")
    else:
        print("Try again")
        print("The correct answer is ", answer, "\n")


# Two-step problems
def two_step():
    import random
    # Uses string_frac()
    a = random.randint(1,11)
    b = random.randint(-7,12)
    c = random.randint(2,36)
    print(a, "x + ", b, " = ", c)
    print("Round answer to two decimal places")
    ans_in = input("x = ")
    answer = (c-b)/a
    # test
    if round(string_frac(ans_in),2)==round(answer,2):
        print("Correct! \n")
    else:
        print("Try again")
        print("The correct answer is ", answer, "\n")


# test loop
for a in range(2):
    one_step_add()
    one_step_subtract()
    one_step_mult()
    one_step_div()
    two_step()
    print(" ")

two_step()
two_step()
Solving for x
import sympy
from sympy import symbols
from sympy.solvers import solve

x=symbols('x')

#put the equation here
eq= 4*x**2 + 4
print("x= ", solve(eq, x))

FACTORIZATION
import sympy
from sympy import symbols
x= symbols('x')
y= symbols('y')


eq = x**3 - 2*x**2 -5*x + 6

sympy.factor(eq)

import sympy
from sympy import symbols
from sympy.solvers import solve

x=symbols('x')

eq= 3*x - 12
solution = solve(eq,x)
for s in solution:
    print("x = ", s)

    import sympy
from sympy import symbols
from sympy.solvers import solve

example = 3*x - 12
equation = Eq(example,0)
solution = solve(equation,x)
print(solution)


#decimal to fraction
digits = input('Enter the decimal number to be converted')
exponent = int(len(digits))-1
n = float(digits)
numerator = int(n*10**exponent)
denominator = 10**exponent
percent = n*100
print("the fraction = ", numerator, "/" , denominator)
print("the percentage is = ", percent, "%")


#solving quadratic equations
import sympy
from sympy import symbols
from sympy.solvers import solve

x = symbols('x')
a= symbols('a')
b= symbols('b')
c= symbols('c')

form = a*x**2 + b*x + c
Left = 0
Right = a*x**2 + b*x + c
eq= 2*x**2 -4*x - 5
solution = solve(eq,x)
for s in solution:
    print("x = ", s)


    #Graphing functions
    import matplotlib.pyplot as plt
import numpy as np
xmin = -10
xmax = 10
ymin = -10
ymax = 10
points = 2*(xmax-xmin)
x = np.linspace(xmin, xmax, points)
fig, ax = plt.subplots()
plt.plot([xmin,xmax],[0,0], 'r')
plt.plot([0,0],[ymin,ymax], 'r')


y = 2*x + 1
plt.plot(x,y,'r')

plt.show()


import matplotlib.pyplot as plt
import numpy as np
xmin = -10
xmax = 10
ymin = -10
ymax = 10
points = 2*(xmax-xmin)
x = np.linspace(xmin, xmax, points)


fig, ax = plt.subplots()
plt.axis([xmin,xmax,ymin,ymax])
plt.plot([xmin,xmax],[0,0], 'r')
plt.plot([0,0],[ymin,ymax], 'r')

ax.set_xlabel("x values")
ax.set_ylabel("y values")
ax.set_title("Some Graph")
ax.grid(True)

ax.set_xticks(np.arange(xmin,xmax,2))
ax.set_yticks(np.arange(ymin,ymax,2))


y = x**3 - 6*x**2 +11*x -6
plt.plot(x,y,'r')






plt.show()



FINDING SLOPE
x1= 2
y1= 3
x2= 5
y2= 7

slope = (y2-y1)/(x2-x1)
print("slope = ", slope)


SLOPE INTERCEPT EQUATION
x1= 1
y1= 7
x2= 2
y2= 10

m = (y2-y1)/(x2-x1)
b = y1 - m*x1
#y = m*x + b
print("y = ", m , "x + ", b)

import matplotlib.pyplot as plt
import numpy as np
xmin = -10
xmax = 10
ymin = -10
ymax = 10

y3 = m*xmin + b
y4= m*xmax + b


fig, ax = plt.subplots()
plt.axis([xmin,xmax,ymin,ymax])
plt.plot([xmin,xmax],[0,0], 'r')
plt.plot([0,0],[ymin,ymax], 'r')

plt.plot([xmin,xmax],[y3,y4], 'b')

ax.set_xlabel("x values")
ax.set_ylabel("y values")
ax.set_title("Some Graph")
ax.grid(True)

ax.set_xticks(np.arange(xmin,xmax,2))
ax.set_yticks(np.arange(ymin,ymax,2))


x1= 0
y1= 17
x2= 8
y2= 25

m = (y2-y1)/(x2-x1)
b = y1 - m*x1
#y = m*x + b
print("y = ", m , "x + ", b)

import matplotlib.pyplot as plt
import numpy as np
xmin = 0
xmax = 10
ymin = 0
ymax = 150

y3 = m*xmin + b
y4= m*xmax + b


fig, ax = plt.subplots()
plt.axis([xmin,xmax,ymin,ymax])
plt.plot([xmin,xmax],[0,0], 'r')
plt.plot([0,0],[ymin,ymax], 'r')

plt.plot([xmin,xmax],[y3,y4], 'b')

ax.set_xlabel("x values")
ax.set_ylabel("y values")
ax.set_title("Some Graph")
ax.grid(True)

ax.set_xticks(np.arange(xmin,xmax,2))
ax.set_yticks(np.arange(ymin,ymax,20))

plt.show()

USING MODULE % TO FIND FACTORS



number = 12
# find the factors
for test_factor in range(1,number+1):
    if number%test_factor == 0:
        print(test_factor)

        REDUCING FRACTIONS TO THEIR LOWEST TERMS
        numerator = 11
denominator = 33
factor = 1

#find the greatest commom factors
for test_factor in range(1,denominator+1):
    if numerator%test_factor==0 and denominator%test_factor==0:
        factor = test_factor

#find the greatest commom factors
n= int(numerator/factor)
d=int(denominator/factor)

print('original: ', numerator, "/" ,denominator)
print('reduced: ', n, "/" ,d)

digits=input('Enter the decimal number you want to convert: ')
exponent=int(len(digits)-1)
n=float(digits)
numerator=int(n*10**exponent)
denominator=int(10**exponent)



factor = 1

#find the greatest commom factors
for test_factor in range(1,denominator+1):
    if numerator%test_factor==0 and denominator%test_factor==0:
        factor = test_factor

#find the greatest commom factors
num= int(numerator/factor)
den=int(denominator/factor)
print('the decimal is ', n)
print('the fraction is ', num, "/", den)
