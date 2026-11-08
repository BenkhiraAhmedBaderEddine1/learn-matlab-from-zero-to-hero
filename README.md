



# learn-matlab-from-zero-to-hero

-------------------------------------------------------------------------------------------------------------------------------------------------


The Learn MATLAB from ZERO to HERO course



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

------------------------------------------------------------------------------------------------------
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

----------------------------------------------------------------------------------------------------
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

----------------------------------------------------------------------------------------------------------------

MATLAB Zero to Hero ⭐
Lesson 3 — Vectors & Matrices
Beginner → Intermediate
 Core MATLAB Skill


Today we're learning one of the most important concepts in MATLAB: Matrices and Vectors.

MATLAB was originally designed around matrix mathematics. Almost everything in engineering, AI, robotics, and signal processing uses these concepts.
1. What is a vector?
A vector is a collection of numbers.

There are two main types:

A. Row vector
A = [10 20 30 40 50];


ROW VECTOR — 1 × 5
10

20

30

40

50



B. Column vector
B = [10; 20; 30; 40; 50];


COLUMN VECTOR — 5 × 1
10

20

30

40

50



Important:
- Spaces separate elements in a row vector.
- Semicolons separate rows.

  2. Creating vectors automatically
MATLAB provides several useful functions.
A = 1:10;
B = 1:2:10;
C = linspace(0,100,6);


Results:
A = 1 2 3 4 5 6 7 8 9 10

B = 1 3 5 7 9

C = 0 20 40 60 80 100


Understand the syntax:

start:step:end

linspace(start,end,number_of_elements)
3. What is a matrix?
A matrix is a rectangular arrangement of numbers in rows and columns.

Example: a 3 × 3 matrix.


A = [1 2 3;
     4 5 6;
     7 8 9];


Matrix A
1


2


3


4


5


6


7


8


9



3 rows × 3 columns

You can create other matrices:
A = zeros(3,3);  % All zeros
B = ones(3,3);   % All ones
C = eye(3);      % Identity matrix
D = rand(3,3);   % Random values


4. Matrix indexing
This is extremely important.

Consider:


A = [10 20 30;
     40 50 60;
     70 80 90];


To access individual elements:
A(1,1)  % 10
A(2,3)  % 60
A(3,2)  % 80


Syntax:
A(row,column)


To access a complete row:
A(2,:)


To access a complete column:
A(:,2)


To access all elements:
A(:)


Remember: MATLAB indexing starts at 1, not 0.
5. Matrix operations
Suppose:
A = [1 2; 3 4];
B = [5 6; 7 8];


Addition
C = A + B;


Result:
6  8
10 12


Subtraction
C = A - B;


Matrix multiplication
C = A * B;


Element-by-element multiplication
C = A .* B;


Important difference:
Operator	Meaning
*	Matrix multiplication
.*	Element-wise multiplication
/	Matrix right division
./	Element-wise division
^	Matrix power
.^	Element-wise power

This distinction is essential for scientific computing.
6. Matrix mathematics
Let's explore three important operations.
A = [1 2; 3 4];

T = A';       % Transpose
D = det(A);   % Determinant
I = inv(A);   % Inverse


Transpose:
\[
A^T =
\begin{bmatrix}
1 & 3\\
2 & 4
\end{bmatrix}
\]

Determinant:
\[
\det(A)=1(4)-2(3)=-2
\]

The inverse exists because the determinant is not zero.

For solving linear systems, MATLAB's backslash operator is generally preferable to explicitly calculating an inverse:
A = [2 1; 1 3];
b = [5; 7];

x = A\b;


This solves:
\[
Ax=b
\]

7. Engineering application — Electrical circuits
Imagine a simple circuit system described by two simultaneous equations:
\[
2I_1+I_2=5
\]

\[
I_1+3I_2=7
\]

We can solve it using MATLAB:
A = [2 1;
     1 3];

B = [5;
     7];

I = A\B;

fprintf('I1 = %.4f A\n',I(1));
fprintf('I2 = %.4f A\n',I(2));


Expected result
I1 = 1.6000 A
I2 = 1.8000 A


This is a practical application of linear algebra in electrical engineering


MATLAB Zero to Hero ⭐
Lesson 4 — Indexing, Arrays & Advanced Matrix Operations
Beginner → Intermediate
 Practical Programming


Welcome back! Today we're going deeper into MATLAB arrays. These concepts are essential for handling large datasets, AI, signal processing, and engineering simulations.
1. Understanding array indexing
Consider this matrix:

A = [10 20 30 40;
     50 60 70 80;
     90 100 110 120];

     Its dimensions are 3 × 4.
Visual representation
10
(1,1)

20
(1,2)

30
(1,3)

40
(1,4)

50
(2,1)

60
(2,2)

70
(2,3)

80
(2,4)

90
(3,1)

100
(3,2)

110
(3,3)

120
(3,4)



Selected element A(2,3) = 70

Access individual elements:
A(1,1)   % 10
A(2,3)   % 70
A(3,4)   % 120


Remember:
A(row,column)


2. Extracting rows and columns
The colon operator : is extremely useful.
A = [10 20 30 40;
     50 60 70 80;
     90 100 110 120];

row = A(2,:);
column = A(:,3);


Results:
row = 50 60 70 80

column =
30
70
110


Other useful examples:
A(1:2,1:3)  % First two rows, first three columns

A(:,2:4)    % All rows, columns 2 to 4

A(2:end,:)  % Rows 2 to the last row

3. Modifying matrix elements
You can change elements without recreating the matrix.
A = [1 2 3;
     4 5 6;
     7 8 9];

A(2,2) = 100;


You can also replace an entire row:
A(1,:) = [10 20 30];


Or an entire column:
A(:,3) = [300;600;900];


4. Reshaping arrays
The reshape() function changes the dimensions of an array without changing its elements or their column-wise order.
A = 1:12;

B = reshape(A,3,4);


Result:
1   4   7   10
2   5   8   11
3   6   9   12


Other useful functions:
