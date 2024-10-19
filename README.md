# Sudoku Solver with Computer Vision

## Sudoku Solver Project Overview

This project utilizes computer vision techniques to solve Sudoku puzzles from natural images. The process involves capturing an image of a Sudoku puzzle, extracting the puzzle grid, identifying and classifying digits within each cell, solving the puzzle using a recursive backtracking algorithm, and finally overlaying the solution onto the original image. OpenCV is employed for image processing tasks.

## Implementation Details

Image processing begins with applying an adaptive threshold to obtain a binary image. Contours are then computed from the binary image to locate the main puzzle grid. A perspective transform is applied to achieve a bird's eye view of the puzzle grid. Subsequently, contours within the transformed grid are computed to identify individual cells. We ascertain which cells contain digits and store relevant information about each cell to reconstruct the Sudoku grid. Upon solving the puzzle, the solution numbers are integrated into the grid cells, and the inverse perspective transform is applied to place the solution back onto the original image.

For the purpose of solving puzzles, a two-dimensional array representing the puzzle grid is provided to an instance of the `SudokuSolver` class. A recursive backtracking algorithm is employed to solve the sudoku puzzle. It's important to note that the solver only returns a single solution, even in cases where multiple solutions may exist.