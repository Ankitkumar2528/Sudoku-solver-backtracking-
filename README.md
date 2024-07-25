# Sudoku-solver-backtracking-
Certainly! The project is a Sudoku solver implemented in Java. Sudoku is a popular logic-based number-placement puzzle. The objective of the puzzle is to fill a 9x9 grid with digits so that each column, each row, and each of the nine 3x3 subgrids contain all of the digits from 1 to 9 exactly once. The given code is designed to solve such puzzles using a backtracking algorithm.

Overview of the Code

1. **`public class SudokuSolver`**:
   - This is the main class that contains the logic for solving the Sudoku puzzle.

2. **`public static void main(String[] args)`**:
   - This is the entry point of the program. It initializes a Sudoku board with some pre-filled values (the board) and then attempts to solve it using the `solveSudoku` method. If a solution is found, it prints the solved board; otherwise, it prints a message indicating that no solution exists.

3. **`public static void printBoard(int[][] board)`**:
   - This method prints the Sudoku board to the console. It iterates through each row and column of the board and prints the values in a readable format.

4. **`public static boolean isValid(int[][] board, int row, int col, int num)`**:
   - This method checks whether placing a given number (`num`) in a specific cell (`row`, `col`) is valid according to Sudoku rules. It verifies that the number does not already exist in the same row, column, or 3x3 subgrid.

5. **`public static boolean solveSudoku(int[][] board)`**:
   - This is the core method that solves the Sudoku puzzle using a backtracking approach. It:
     - Finds an empty cell in the board using `findEmptyLocation`.
     - Attempts to place numbers from 1 to 9 in the empty cell.
     - Recursively calls itself to solve the rest of the board with the newly placed number.
     - If placing a number leads to a solution, it returns true.
     - If none of the numbers work, it backtracks by resetting the cell to 0 and trying the next number.

6. **`public static int[] findEmptyLocation(int[][] board)`**:
   - This method searches the board for the first empty cell (denoted by 0). It returns the position of this cell as an array of two integers [row, col]. If no empty cells are found, it returns `null`, indicating that the board is fully filled and possibly solved.

### Summary

The SudokuSolver class implements a complete Sudoku solver using the backtracking algorithm. The approach involves:
- Finding an empty cell.
- Trying all possible numbers in that cell.
- Recursively solving the resulting board.
- Backtracking if a number does not lead to a solution.

This solution assumes that the input board is a valid Sudoku puzzle with a unique solution. It is a straightforward and effective approach to solving Sudoku puzzles, suitable for small-scale problems typically encountered in Sudoku challenges.      
          
