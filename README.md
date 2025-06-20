# Quantum_Sudoku
We treat a Sudoku puzzle as an unstructured search problem and build a quantum circuit to find the solution.

## Sudoku Solver
We use Qiskit to build a quantum circuit that returns the solution to a 4x4 sudoku puzzle by first constructing an oracle to mark the solution state and then applying Grover's search using that oracle. This solution is presented as the jupyter notebook, Sudoku_Solver.ipnyb and includes one test examples. Necessary packages include numpy and qiskit.

### Some notes on complexity
Focusing on the 4x4 puzzle, we construct a quantum circuit with 2 qubits per empty cell (as the digits are 1-4), 12 qubits to record area conflicts in one of 12 areas (4 each row, column and square) and 9 ancillary bits for calculation and bookkeeping. We chose to roughly double the complexity (with double the number of Toffoli gates) in order to reduce the number of ancillary qubits needed for the calculation. All of the calculation bits are cleaned after each area is evaluated, and the result (no conflicts = 1 or conflict = 0) is recorded on the dedicated wire.

