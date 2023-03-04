# Quantum computing and sudoku

Algorithms for constraint based quantum evaluation.

## QUBO on D-Wave annealer

[Julian towardsdatascience](https://towardsdatascience.com/solving-sudoku-with-a-quantum-power-up-5bb4f64f3944)

[Julian github notebook](https://github.com/ju2ez/quantum_annealing_sudoku/blob/main/quantum_annealing_sudoku_9x9.ipynb)

In Sudoku we have a large number of constraints/rules which determine
whether a proposed solution is valid or not. 

1. A single cell/box can only have one number

$$\sum_{k=1}^N x_{ijk} = 1, \forall i,j\in cell$$

2. Each column $j$ can not have duplicate numbers:

$$\sum_{i=1}^Nx_{ijk} = 1, \forall j\in column, \forall k\in \{1,...,N\}$$

3. Each row $i$ can not have duplicate numbers:

$$\sum_{j=1}^Nx_{ijk} = 1, \forall i\in row, \forall k\in \{1,...,N\}$$

4. Each of the nine 3x3 sub-grids can not have duplicate numbers:

$$\sum_i^2\sum_j^nx_{(i+u)(j+v)k} = 1, \forall k\in \{1,...,N\}, \forall (u, v)\in\{0, 3, 6\}$$

5. Initial numbers given as a hint cannot be changed:

$$\sum_{x_{ijk}\in hints} x_{ijk} = 1$$

...

## Graph coloring and Grover's search algorithm
[Microsoft learn](https://learn.microsoft.com/en-us/samples/microsoft/quantum/solving-sudoku-using-grovers-algorithm/)

## Duality computing

[Ankur Pal et al.](https://www.researchgate.net/profile/Bikash-Behera/publication/326978036_Solving_Sudoku_game_using_a_hybrid_classical-quantum_algorithm/links/5b6f040992851ca65055deb1/Solving-Sudoku-game-using-a-hybrid-classical-quantum-algorithm.pdf)

...

## License

All code is to be held under a general MIT license, please see [LICENSE](https://github.com/willeagren/sudoqu/blob/bebef7c975212e629044dc8b582dda54f95e0074/LICENSE) for specific information.
