# ErdosQuantum_FirstProject
Miniproject 1 from Erdos Quantum Computing Boot Camp, Summer 2025.
This project is still in progress. The partial notebook has been added to the repo.

## Sudoku Solver
We use Qiskit to build a quantum circuit that returns the solution to a 4x4 sudoku puzzle. This solution is presented as the jupyter notebook, Sudoku_Solver.ipnyb and includes one test examples. Necessary packages include numpy and qiskit.

### Some notes on complexity
Focusing on the 4x4 puzzle, we construct a quantum circuit with 2 qubits per empty cell (as the digits are 1-4), 12 qubits to record area conflicts in one of 12 areas (4 each row, column and square) and 9 ancillary bits for calculation and bookkeeping. We chose to roughly double the complexity (with double the number of Toffoli gates) in order to reduce the number of ancillary qubits needed for the calculation. All of the calculation bits are cleaned after each area is evaluated, and the result (no conflicts = 1 or conflict = 0) is recorded on the dedicated wire.

###Questions for instructor.
What is the correct way to report complexity of this function? If I am reporting based on the number of Toffoli gates, what is the contribution of a multicontrolled gate?

## Multi-controlled U gate and other upcoming stories
I intend to continue to solve some of the other problems posed in this homework set. Each solution will be included in this repository as a separate notebook. This will be returned to after completing the other mini-projects for the course. I need to catch up!
