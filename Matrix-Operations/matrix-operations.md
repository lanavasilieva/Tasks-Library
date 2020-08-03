## Working with matrices
### Project Setup
- Create a file named `TestAssignment.java`. <br>
- You'll need only basic Java features, **do not import** any libraries (except java.lang.*) and don't wrap the file in package. <br>
- Add a file TestAssignment.java to a .zip archive named NameSurname.zip. For example: `JaneDoe.zip`<br>
- We `WILL NOT` grade an assignment submitted omitting these rules.

### Matrix Jugglery
The purpose of the task is to implement basic matrix operations: addition, subtraction and multiplication. <br>


Program run example: <br>
```
> java TestAssignment < data01.txt > result01.txt
> cat result01.txt
[5 1 1; 9 0 0]
```


Each matrix is given in the following way: `name=[x11 x12 ... x1n; x21 x22 ... x2n;...,xm1 xm2 ... xmm]` <br>
Matrix operations expression follows matrix definitions.


**Example 01 with comments:** <br>
```
A=[1 2 2; 0 3 1; -1 2 -4]   <- first matrix definition, matrix A is 3x3
B=[2 1 0; -2 -1 -1; 1 1 2]  <- second matrix definition, matrix B is 3x3
                            <- new line
A+B                         <- matrix operation (addition)
```

**Example 02 with comments:** <br>
```
M=[1 2 2; 0 3 1; -1 2 -4]   <- first matrix definition, matrix M is 3x3
N=[2 1 0; -2 -1 -1; 1 1 2]  <- second matrix definition, matrix N is 3x3
K=[2 3; 5 0; 3 1]           <- third matrix definition, matrix K is 3x2
                            <- new line
M+K+N+N*N+M+N               <- matrix operations (5 additions and 1 multiplication)
```

### Requirements
- Name of the matrix has to be an uppercase letter. <br>
- Input should always follow the same pattern: matrix definitions - new line - matrix operations. <br>
- Each matrix is defined on a separate line. <br>
- Elements are separated by whitespace, rows are separated by semicolon. <br>
- Elements are wrapped in square brackets. <br>
- Operations are separated from matrix definition with exactly one new line. <br>
- Operations may contain arbitrary number of operators and operands. <br>
- There are only three operators: `+`, `-` and `*`. <br>
- Operators have the following priority: multiplication, addition and subtraction. <br>
- Operations are evaluated from left to right. <br>
You can read `A+B*C+D*E-F` as `((A+(B*C))+(D*E))-F` <br>
- Output of the program is the result of defined operations. <br>
- Number of matrices are limited by the number of letters in English alphabet, length of operation expression is not limited. <br>
- Every element in matrix is an integer number.<br>
- If any of requirements described above are failing, exception should be thrown and a message should appear in stderr.
- Error messages should be formed in the following way: <br>
`Exception caught: $exceptionName. Can't $do_something.`

### More Examples

Example 03: <br>
stdin: <br>
```
S=[1]
P=[1]

S+P
```
stdout: <br>
`[2]`<br>
stderr: <br>

Example 04: <br>
stdin: <br>
```
B=[5 2 4; 0 2 -1; 3 -5 -4]
E=[-6 -5 -8; -1 -1 -10; 10 0 -7]
R=[-1 -7 6; -2 9 -4; 6 -10 2]

R+E+B
```

stdout: <br>
`[-2 -10 2; -3 10 -15; 19 -15 -9]`<br>
stderr: <br>


Example 05: <br>
stdin: <br>
```
K=[-10 0 2; -6 10 -6; -9 2 0]
D=[0 6 7]
M=[10 -5 -4]

D*K+M
```
stdout: <br>
`[-89 69 -40]` <br>
stderr: <br>


Example 06: <br>
stdin: <br>
```
R=[6 9; -3 9; -9 10]
K=[2 -8 8; -1 2 -4]

K+K*R*K
```
stdout: <br>
`[-96 332 -384; 78 -252 312]`<br>
stderr: <br>


Example 07: <br>
stdin: <br>
```
M=[-9 5 9; -7 8 7; 10 -3 3]

M*M+M-M
```
stdout: <br>
`[136 -32 -19; 77 8 14; -39 17 78]`<br>
stderr: <br>


Example 08: <br>
stdin: <br>
```
M=[-9 5 9; -7 8x 7; 10 -3 3]`

M*M
```

stdout: <br>

stderr: <br>
`Exception caught: IllegalArgumentException. Can't read matrix.`


Example 09: <br>
stdin: <br>
```
P=[6 0 9; -3 1 9; -9 2 10]
Q=[2 -8 8 0; -1 2 -4 2]

P+Q*P+Q
```
stdout: <br>

stderr: <br>
`Exception caught: IllegalArgumentException. Can't perform multiplication.`


You can use [our test data](data) to test your solution.


**We use the following definitions:** <br>
Matrix https://mathworld.wolfram.com/Matrix.html <br>
Matrix multiplication https://mathworld.wolfram.com/MatrixMultiplication.html <br>
Matrix addition https://mathworld.wolfram.com/MatrixAddition.html

### Non-functional Requirements
Your solution `MUST` have a Javadoc <br>
You code `MUST` be readable and follow any of known code conventions <br>
You `MUST` cover at least 25% of your code with unit tests <br>
