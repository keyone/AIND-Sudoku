# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: First, we find potential candidates, boxes with two digits and match them in pairs.
Then, we delete the digits of the naked twin pair from the other boxes in the unit.
We repeat these two steps through constraint propagation until we get a solution.
To reduce the Sudoku, we now have three strategies: elimination, only choice, and naked twins.
These strategies or constraints (eliminate -> only_choice -> naked_twins) are applied repeatly until we get a solution or not.
This technique is called constraint propagation.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal Sudoku problem?
A: We create two additional units that represent the diagonals of the grid.
These diagonals units are constraints that are enforced throughout the resolution of the sudoku.
We need to set this local rule during the initialization of our solution. Then, this rule will be propagated to resolve the Sudoku.

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solutions.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Data

The data consists of a text file of diagonal sudokus for you to solve.