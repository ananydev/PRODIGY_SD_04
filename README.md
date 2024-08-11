SUDOKU SOLVER :

This project is a simple Sudoku Solver implemented in Java using the backtracking algorithm. It takes a partially filled 9x9 Sudoku board as input and solves it by filling in the empty cells while adhering to the rules of Sudoku.




FEATURES :
1. Backtracking Algorithm: The solver uses a backtracking approach to try placing numbers in the empty cells. If a number placement doesn't lead to a solution, it backtracks and tries a different number.

2. Input Board Flexibility: The solver can handle any valid partially filled 9x9 Sudoku board. Cells that are not filled should be represented by 0.

3. Validation of Moves: The isSafe method ensures that the number placed in any cell does not violate the Sudoku rules, checking the row, column, and 3x3 subgrid.

4. Efficient Search: The solver moves sequentially through the board, placing numbers and recursively attempting to solve the board. It stops as soon as a solution is found.

5. Complete Board Printout: Upon solving the board, the program prints the entire solved Sudoku grid to the console.



WORKING :

1. Checking if a Number is Safe :     This function checks if it's safe to place a given number (num) in a specific cell at position (row, col) on the board. It does so by ensuring that:
                                      Row Check: The number does not already exist in the current row.
                                      Column Check: The number does not already exist in the current column.
                                      Subgrid Check: The number does not already exist in the 3x3 subgrid containing the cell.
                                      If all three checks pass, the function returns true; otherwise, it returns false.

2. Solving the Sudoku Puzzle :        This is the main function that attempts to solve the Sudoku puzzle using backtracking. The algorithm works as follows:
                                      Base Case: If the solver reaches the last cell (i.e., row == 8 and col == 9), the puzzle is solved, and the function returns true.  
                                      Recursive Case:
                                                      If the current cell is already filled (not 0), move to the next cell.
                                                      If the current cell is empty (0), try placing numbers 1 to 9 in it.
                                                      For each number, check if it's safe to place using the isSafe() function.
                                                      If it's safe, place the number and recursively try to solve the rest of the board.
                                                      If placing the number doesn't lead to a solution, backtrack by resetting the cell to 0.
                                                      If no number can be placed in the current cell, return false.


3. Printing the Sudoku Board :       This function prints the Sudoku board in a readable format. It iterates over each row and column of the board, printing the numbers with a space between them. It also adds a new line after each row.
