# Monte Carlo Minimization - Parallelized Search Algorithm

## Introduction
This repository contains a Java implementation of a serial and parallelized search algorithim which makes use of the Monte Carlo method to locate a minimum in a function. Parallelization was used to speed up the process for varying sizes of the input parameters (more below).

## Instructions

## Run the code
There are 2 ways to run the code:
- Single serial run
- Single parallel run

To run them, ensure you are on a Unix machine or just make sure that `make` is available to use from the command line. The commands are:
```sh
make run-serial
```
```sh
make run-par
```
Note that if you want to edit the input parameters, you must do so manually in the Makefile.

### Make run information
In the Makefile you must input 7 space-seperated values after `-cp bin MonteCarloMini.MonteCarloMinimization` or `-cp bin MonteCarloMini.MonteCarloMinimizationParallel`, depending on which program you want to run.
1. Rows (int): Number of rows in the grid.
2. Columns (int): Number of columns in the grid.
3. xmin (double): Minimum x-coordinate of the terrain.
4. xmax (double): Maximum x-coordinate of the terrain.
5. ymin (double): Minimum y-coordinate of the terrain.
6. ymax (double): Maximum y-coordinate of the terrain.
7. Search Density (double): The number of searches applied to each grid position.

For example:
```
100 100 -100.0 100.0 -100.0 100.0 0.5
```

## Output
The program will output the results of the Monte Carlo searches to the CLI with information regarding the execution time, grid sizes, x and y values, number of searches performed, percentage of grid points visited and evaluated, and the global minimum with its correlating x and y coordinates.

## Important Notes
- Do not edit the source code if you want to change the parameters of the test. Do this strictly in the Makefile.
- Ensure that you have Java installed and have access to the `javac`,`java` and `make` commands.

## Conclusion
By reading this readme file, you should have a good enough overview of the project to be able to run tests with different parameters and observe the results.