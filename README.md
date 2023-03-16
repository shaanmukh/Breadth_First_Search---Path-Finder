# Maze Solver

This program solves a maze using breadth-first search algorithm and visualizes the path on a console window using the curses library in Python.

## How to Use

1. Make sure you have Python 3 and the curses library installed.
2. Open a terminal window and navigate to the directory containing the code.
3. Run the command python maze_solver.py to start the program.
4. The program will show the maze and the path it found from the starting point "O" to the ending point "X".
5. Press any key to exit the program.

## How it Works

The program represents the maze as a 2D list of characters, where "#" represents a wall and " " represents a free space. The starting point is denoted by "O" and the ending point by "X".

The *find_path* function uses breadth-first search to find the shortest path from the starting point to the ending point. It starts at the starting point and explores all neighboring cells, marking each cell as visited to avoid revisiting it. If a neighboring cell is the ending point, the function returns the path to that cell. If no path is found, the function returns *None*.

The *print_maze* function uses the curses library to display the maze and the path found. The function takes a 2D list representing the maze, a curses window object, and an optional path as input. The function iterates through each cell in the maze and displays it on the curses window. If a cell is in the path, it is displayed in red. Otherwise, it is displayed in blue.

The *main* function initializes the curses library and calls *find_path* and *print_maze* to find and display the path.

The *wrapper* function from curses is used to handle the initialization and cleanup of the curses library.

The *find_neighbors* function returns a list of neighboring cells for a given cell. It checks the cells above, below, to the left, and to the right of the given cell, and adds them to the list if they are not walls and are within the bounds of the maze.

The program uses a queue to keep track of the cells to explore in the breadth-first search algorithm. The *visited* set is used to keep track of which cells have already been explored to avoid revisiting them.

Finally, the program waits for the user to press a key before exiting.


## Limitations

- The program assumes that the maze is rectangular and that the starting and ending points are present in the maze. It may not work correctly with irregularly shaped mazes or mazes with multiple starting or ending points.

- The program also assumes that the maze can be displayed within the console window. If the maze is too large, it may not be possible to display it within the console window.

## Conclusion

The Maze Solver program demonstrates how breadth-first search can be used to solve a maze and how the curses library can be used to visualize the path found. The program can be used as a starting point for more complex maze solving algorithms or for visualizing other types of graph traversal algorithms.
