# learn-matlab-from-zero-to-hero
The Learn MATLAB from ZERO to HERO course
1. Your complete MATLAB roadmap
Level	Topics


1	MATLAB installation and interface

2	Variables, data types and operators

3	Vectors and matrices

4	Indexing and matrix operations

5	Conditions and logical operators

6	Loops: for, while

7	Scripts and functions

8	Plotting and visualization

9	Data analysis and statistics

10	Numerical methods and calculus

11	Differential equations and ode45

12	Linear algebra and optimization

13	Signal processing

14	Control systems

15	Artificial intelligence and machine learning

16	Deep learning

17	Robotics and automation

18	Simulink

19	Advanced engineering simulations

20	Professional portfolio projects


What is MATLAB?

MATLAB stands for MATrix LABoratory.

It is a programming and numerical computing environment used for:
- Mathematical calculations.
- Electrical circuit simulation.
- Robotics and automation.
- Artificial intelligence.
- Signal and image processing.
- Control systems.
- Scientific research and engineering.
Understanding your first MATLAB commands
Open MATLAB and enter:
clc
clear
close all

disp('Hello World!')

What does each command do?
Command	Meaning
clc	Clears Command Window
clear	Removes variables
close all	Closes open figures
disp()	Displays information

3. Variables
A variable stores information.
x = 10;
y = 20;

z = x + y;

disp(z)


Output:
30

More examples:
age = 23;
name = "Ahmed";
temperature = 36.5;
isStudent = true;


Notice that MATLAB uses = for assignment.
4. Mathematical operators
Operator	Meaning	Example
+	Addition	5+3
-	Subtraction	5-3
*	Multiplication	5*3
/	Division	10/2
^	Power	2^3
sqrt()	Square root	sqrt(25)

Try this:
a = 15;
b = 5;

addition = a + b;
subtraction = a - b;
multiplication = a * b;
division = a / b;
power = a ^ 2;

disp(addition)
disp(subtraction)
disp(multiplication)
disp(division)
disp(power)


5. Your first engineering application
Let's calculate electrical power.

Remember:
\[
P=V\times I
\]

Where:
- P = Power (Watts)
- V = Voltage (Volts)
- I = Current (Amperes)
MATLAB code:
Voltage = 220;
Current = 5;

Power = Voltage * Current;

fprintf('Electrical Power = %.2f Watts\n', Power);


Expected result
Electrical Power = 1100.00 Watts


This is your first MATLAB engineering calculation!

MATLAB Zero to Hero ⭐
Lesson 2 — Variables, Data Types & Operators
Beginner Level
 Practical Engineering


Today, you'll learn how MATLAB stores information, handles different data types, and performs calculations.
1. Understanding variables
A variable is a named container that stores a value.
voltage = 220;
current = 5;
power = voltage * current;
Here:
- voltage stores 220.
- current stores 5.
- power stores 1100.
Display the results:
disp(voltage)
disp(current)
disp(power)

Important: MATLAB is case-sensitive.
Voltage = 220;
voltage = 110;

disp(Voltage)  % 220
disp(voltage)  % 110


These are two different variables!
2. MATLAB data types
There are several important data types.
Type	Example	Description
double	10.5	Decimal numbers
int32	int32(10)	32-bit integer
logical	true	True or false
char	'Hello'	Character array
string	"MATLAB"	Text string
single	single(2.5)	Single precision

Try this code:
a = 25.5;
b = int32(10);
c = true;
d = 'Ahmed';
e = "Engineering";

whos


whos displays information about your variables.

3. Arithmetic operators
Essential MATLAB operators
Operator	Function	Example
+	Addition	5+2
-	Subtraction	5-2
*	Multiplication	5*2
/	Division	10/2
^	Exponentiation	2^3
mod()	Remainder	mod(10,3)
sqrt()	Square root	sqrt(25)


Practice:
a = 20;
b = 6;

x1 = a + b;
x2 = a - b;
x3 = a * b;
x4 = a / b;
x5 = a ^ 2;
x6 = mod(a,b);

temperature = 40;

result1 = temperature > 30;
result2 = temperature == 40;
result3 = temperature < 20;

disp(result1)
disp(result2)
disp(result3)


Output:
1
1
0


In MATLAB, 1 represents true and 0 represents false.


4. Comparison operators
These operators compare values and return logical results.
Operator	Meaning
==	Equal
~=	Not equal
>	Greater than
<	Less than
>=	Greater than or equal
<=	Less than or equal


Example:

5. Logical operators
A = true;
B = false;

AND_result = A & B;
OR_result  = A | B;
NOT_result = ~A;


- & means AND.
- | means OR.
- ~ means NOT.
These become extremely important in automation, control systems, and AI algorithms.
6. Engineering application — Electrical calculations
Let's calculate resistance, power, and energy.

Using Ohm's law:
\[
R = \frac{V}{I}
\]

Power:
\[
P = V \times I
\]

Energy:
\[
E = P \times t
\]

MATLAB implementation:
clc;
clear;

V = 220;       % Voltage
I = 5;         % Current
t = 3;         % Time in hours

R = V / I;
P = V * I;
E = P * t;

fprintf('Resistance: %.2f Ohms\n', R);
fprintf('Power: %.2f Watts\n', P);
fprintf('Energy: %.2f Wh\n', E);


Expected output
Resistance: 44.00 Ohms
Power: 1100.00 Watts
Energy: 3300.00 Wh
