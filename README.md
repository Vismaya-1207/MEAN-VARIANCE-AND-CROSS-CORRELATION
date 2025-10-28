# MEAN-VARIANCE-AND-CROSS-CORRELATION

## Aim
To write a program for mean, variance, and cross-correlation in Scilab and verify the output.

## Equipment Needed
1.Computer with i3 Processor
2.Scilab Software
## Algorithm
1.Define the Function: Specify the function you want to simulate. For example, f(x) = sin(x) or any other function.
2.Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
3.Evaluate the Function: Compute the function values at each of these sample points.
4.Compute Mean, Variance, and Cross-Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
5.Display Results: Output the computed mean, variance, and cross-correlation.
## Procedure
1.Refer to the algorithm and write code for the experiment.
2.Open Scilab on your system.
Type your code in a new editor.
3.Save the file.
4.Execute the code.
5.If any errors occur, correct the code and execute again.
6.Verify the generated results.
## Program
```
clear;
clc;
clear;
function z = f(x)
    z = (4-x)^2 
endfunction
a = 0;
b = 1;
EX = intg(a, b, f); 
function z = c(y)
    z = (3-x)^2; 
endfunction

EY = intg(a, b, c); 

disp(EX, "i) Mean of X =");
disp(EY, "Mean of Y =");

function z = g(x)
    z = (4-x)^2 
endfunction

EX2 = intg(a, b, g); // E[X^2]

function z = h(y)
    z = 3*(1-y)^3 * y^2; // Y^2 * PDF
endfunction

EY2 = intg(a, b, h); // E[Y^2]

vX2 = EX2 - (EX)^2; // Variance of X
vY2 = EY2 - (EY)^2; // Variance of Y

disp(vX2, "ii) Variance of X");
disp(vY2, "Variance of Y");

// Cross-Correlation
x = input("Type in the reference sequence = ");
y = input("Type in the second sequence = ");
n1 = max(size(y)) - 1;
n2 = max(size(x)) - 1;
r = corr(x, y, n1);
plot2d3('gnn', r);
```
Output

Mean Values

Mean of X = 0.3011687

Mean of Y = 0.25

Variance Values

Variance of X = 0.0092974

Variance of Y = 0.0375000

Cross-Correlation Input Example

Reference sequence: [1, 2, 3, 4, 5, 6, 7, 8]

Second sequence: [2 , 4 , 7 , 8 , 9 , 1 , 3 , 6]

MANUAL CALCULATION:


RESULT:
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.
