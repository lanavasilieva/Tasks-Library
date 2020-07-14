## Coordinates
The purpose of the task is to consecutively implement three functions to run a simulation.

### Step 0: Project Setup
Create a file named `TestAssignment`. <br>
This file should contain three public static methods: `matrixGeneration`, `findCoordinates` and `simulation`. <br>
The file should **not** contain a main() function.

[Here](TestAssignment.java) you'll find a file with predefined functions.

You'll need only basic Java features, **do not import** any libraries (except java.lang.*) and don't wrap the file in package.

Add a file TestAssignment.java to a .zip archive named NameSurname.zip. For example: `JaneDoe.zip`

**Mathematics notation** <br>
*Intervals*. Here we are using [the international standard](https://en.wikipedia.org/wiki/Interval_(mathematics)#Notations_for_intervals) to define intervals. Please have it in mind while making boundaries check.

*Probability*. To complete a task you have to calculate the probability of an event. The probability of an event here is defined as follows:<br>
P(event) = number of favorable outcomes / total number of outcomes

### Step 1: Matrix generation
Write a program `matrixGeneration(int n)` that takes an integer `n` and creates an `n x n matrix` filled in with random numbers from 1 to 100 in random order.

**Requirements**:
- the function accepts a single parameter `n`
- `int n` is an integer number from the interval (0, 10000)
- if the parameter is not a valid integer number the function throws `IllegalArgumentException` exception
- the function returns a two dimensional integer array
- an element in array is an integer number from the interval [0, 100) (means including 0 and excluding 100).

Here is an example of matrices for various values of `n`. *Please note that your results may differ from provided since matrices are filled with random numbers.*:

    matrixGeneration(3)
    {{70, 67, 4}, {49, 63, 90}, {77, 7, 93}}
    
    matrixGeneration(5)
    {{97, 75, 19, 5, 22}, {56, 67, 33, 7, 96}, {39, 15, 57, 22, 10}, {81, 69, 95, 19, 60}, {32, 70, 56, 34, 1}}

### Step 2: Find coordinates
Implement a function `findCoordinates(int n)`. The function takes one argument: integer `n` and returns `coordinates of the biggest element` in the n x n matrix.

This function should:
1. generate an `n x n matrix N` using `matrixGeneration(int n)` function
2. find coordinates x and y of the biggest element in the matrix N
3. return an integer array `int[] coordinates` with x and y in this order: `x, y` and `coordinates.length` = 2.

**Requirements**:
- the function accepts a single parameter `n`  <br>
- `int n` is an integer number from the interval (0, 10000)  <br>
- if the parameter is not a valid integer number the function throws `IllegalArgumentException` exception  <br>
- the function returns an integer array   <br>
- the function must call `matrixGeneration(int n)` function  <br>

Here is an example of various outputs. *Please note that your results may differ from provided since matrices are filled with random numbers.*:

    findCoordinates(12)
    [5, 3]
    
    findCoordinates(5)
    [1, 4]

### Step 3: Running a simulation
Implement a function `simulation(int n, int[] coordinates, int trials)`, which in each of `trials` independent experiments runs `findCoordinates(int n)`.
Find the probability `P` that the largest element is on `x0, y0` position. Coordinates x0 and y0 are given in `int[] coordinates` array.

Here probability P of an event is specified by: <br>
`P(event) = number of favorable outcomes / total number of outcomes`

Here is an example of various outputs. *Please note that your results may differ from provided since matrices are filled with random numbers.*:

    simulation(12, [2, 10], 1000000)
    P = 0.03
    
    simulation(5, [1, 1], 100000)
    P = 0.12

**Requirements**:
- the function accepts three parameters  <br>
- parameters meet the following requirements: <br>
`int n` - an integer number from the interval (0, 10000),<br>
`int[] coordinates` - an integer array with `coordinates.length` = 2 <br>
`int trials` - an integer number from the interval `[100, 1000000]`<br>
- if any of parameters is not a valid number the function throws `IllegalArgumentException` exception <br>
- the function returns nothing <br>
- the function must print the result as stated in examples <br>

## Submitting
Submit a zip file named NameSurname.zip that contains the file TestAssignment.java.

## Assessment
We will run a pack of tests and review your work manually to check that your programs meet the specifications. Our decision will be based on the number of tests you pass and on the code and solution quality.


