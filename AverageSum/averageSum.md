## Average sum
The purpose of the task is to consecutively implement three functions to run a simulation.

### Step 0: Project Setup
Create a file named `TestAssignment`. <br>
This file should contain three public static methods: `matrixGeneration`, `averageSum` and `simulation`. <br>
The file should **not** contain a main() function.

[Here](TestAssignment.java) you'll find a file with predefined functions.

You'll need only basic Java features, **do not import** any libraries (except java.lang.*) and don't wrap the file in package.

Add a file TestAssignment.java to a .zip archive named NameSurname.zip. For example: `JaneDoe.zip`

**Print Statements** <br>
Only simulation() method must have print statement. **Do not use print statements** in your other methods.

**Mathematics notation** <br>
*Intervals*. Here we are using [the international standard](https://en.wikipedia.org/wiki/Interval_(mathematics)#Notations_for_intervals) to define intervals. Please have it in mind while making boundaries check.

*Probability*. To complete a task you have to calculate the probability of an event. The probability of an event here is defined as follows:<br>
P(event) = number of favorable outcomes / total number of outcomes

### Step 1: Matrix generation
Write a program `matrixGeneration(int n)` that takes an integer `n` and creates an `n x n matrix` filled in with random numbers from 1 to 100 in random order.

**Requirements**:
- the function accepts a single parameter `n`
- `int n` is an integer number from the interval (0, 10000)
- if the parameter is not a valid number the function throws `IllegalArgumentException` exception
- the function returns a two dimensional integer array
- an element in array is an integer number from the interval [0, 100) (means including 0 and excluding 100).

Here is an example of matrices for various values of `n`. *Please note that your results may differ from provided since matrices are filled with random numbers.*:

    > matrixGeneration(3)
    {{70, 67, 4}, {49, 63, 90}, {77, 7, 93}}
    
    > matrixGeneration(5)
    {{97, 75, 19, 5, 22}, {56, 67, 33, 7, 96}, {39, 15, 57, 22, 10}, {81, 69, 95, 19, 60}, {32, 70, 56, 34, 1}}

### Step 2: Find average sum
Implement a function `averageSum(int n, int m)`. The function takes two arguments: integer `n` and integer `m` and returns the average sum of all submatrices of a given size.

This function should:
1. generate an `n x n matrix N` using `matrixGeneration(int n)` function
2. find a sum of elements in each `m x m submatrix` in `matrix M`
3. compute and return the `average` submatrix sum

**Requirements**:
- the function accepts two parameters: `m` and `n` <br>
- parameters should meet the following requirements: <br>
`int n` - an integer number from the interval (0, 10000) <br>
`int m` - an integer number from the interval (0, n] <br>
- if any of parameters is not a valid number the function throws `IllegalArgumentException` exception <br>
- the function returns a double number <br>
- the function must call `matrixGeneration(int n)` function

Here is an example of various outputs. *Please note that your results may differ from provided since matrices are filled with random numbers.*:

    > averageSum(5, 2)
    31.0
    
    > averageSum(12, 5)
    62.76

### Step 3: Running a simulation
Implement a function `simulation(int n, int m, double q, int trials)`, which in each of `trials` independent experiments runs `averageSum(int n, int m)`.
Find the probability `P` that the average sum is less than `q`.

Here probability P of an event is specified by: <br>
`P(event) = number of favorable outcomes / total number of outcomes`

Here is an example of various outputs. *Please note that your results may differ from provided since matrices are filled with random numbers.*:

    > simulation(10, 3, 400.0, 100000)
    P = 0.08
    
    > simulation(16, 5, 1200.0, 10000)
    P = 0.19

**Requirements**:
- the function accepts four parameters
- parameters meet the following requirements: <br>
`int n` - an integer number from the interval (0, 10000),<br>
`int m` - an integer number from the interval (0, n], <br>
`double q` - a double number, <br>
`int trials` - an integer number from the interval `[100, 1000000]`<br>
- if any of parameters is not a valid number the function throws `IllegalArgumentException` exception
- the function returns nothing
- the function must print the result as stated in examples

## Submitting
Submit a zip file named NameSurname.zip that contains the file TestAssignment.java.

## Assessment
We will run a pack of tests and review your work manually to check that your programs meet the specifications. Our decision will be based on the number of tests you pass and on the code and solution quality.