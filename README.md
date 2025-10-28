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
function X = f(x)
    z = (4 - x).^2;
    X = x .* z;
endfunction
a = 0; b = 1;
EX = intg(a, b, f);
function Y = c(y)
    z = (3 - y).^2;
    Y = y .* z;
endfunction
EY = intg(a, b, c);
function X2 = g(x)
    z = (4 - x).^2;
    X2 = (x.^2) .* z;
endfunction
EX2 = intg(a, b, g);
function Y2 = h(y)
    z = (3 - y).^2;
    Y2 = (y.^2) .* z;
    endfunction
EY2 = intg(a, b, h);
vX2 = EX2 - (EX)^2;
vY2 = EY2 - (EY)^2;
disp(EX, "i) Mean of X =");
disp(EY, "   Mean of Y =");
disp(vX2, "ii) Variance of X =");
disp(vY2, "   Variance of Y =");
x= input("type in the reference sequence="); 
y= input("type in the second sequence="); 
n1=max(size(y))-1;
n2=max(size(x))-1;
r=corr(x,y,n1);
plot2d3('gnn',r);

```

### Output

<img width="685" height="544" alt="Screenshot 2025-10-28 213317" src="https://github.com/user-attachments/assets/4cac2c3a-c1d7-4c99-8326-7f3374860f5d" />

<img width="739" height="707" alt="Screenshot 2025-10-28 213326" src="https://github.com/user-attachments/assets/086e9d70-6d83-4777-bd6c-bfb39c6db1e4" />

### Tabular Column:


![WhatsApp Image 2025-10-28 at 21 37 52_83386e34](https://github.com/user-attachments/assets/18e10e7b-7774-4088-a8d5-be929c936572)

### MANUAL CALCULATION:


![WhatsApp Image 2025-10-28 at 21 38 15_34d3807f](https://github.com/user-attachments/assets/e87e2e9f-a33d-4e70-87a1-95e0774d2f63)

![WhatsApp Image 2025-10-28 at 21 38 23_0e763135](https://github.com/user-attachments/assets/f93da123-eae1-43fa-8eca-29b2c3982918)



### RESULT:
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.
