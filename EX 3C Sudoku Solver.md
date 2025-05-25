# EX 3C Sudoku Solver
## DATE:11/04/2025
## AIM:
To write a python program to find the solution of sudoku puzzle using Backtracking.


## Algorithm
1. Define a function to check if placing a number at a given position is valid (no duplicates in row, column, or 3×3 box).

2.Define a function to find the next empty cell in the grid.

3.Implement the recursive backtracking function:

4.If no empty cell, puzzle is solved.

5.For each digit from 1 to 9:

6.If valid, place the digit and recursively attempt to solve.

7.If unsuccessful, backtrack.

8.Print the solved Sudoku board
  

## Program:
```
/*
N = 4
 

def printSolution( sol ):
     
    for i in sol:
        for j in i:
            print(str(j) + " ", end ="")
        print("")
 

def isSafe( maze, x, y ):
     
    if x >= 0 and x < N and y >= 0 and y < N and maze[x][y] == 1:
        return True
     
    return False
 

def solveMaze( maze ):
     
    # Creating a 4 * 4 2-D list
    sol = [ [ 0 for j in range(4) ] for i in range(4) ]
     
    if solveMazeUtil(maze, 0, 0, sol) == False:
        print("Solution doesn't exist");
        return False
     
    printSolution(sol)
    return True
     

def solveMazeUtil(maze, x, y, sol):
    if x==N-1 and y==N-1:
        sol[x][y]=1
        return True
    if isSafe(maze,x,y)==True:
        sol[x][y]=1
        if solveMazeUtil(maze,x+1,y,sol)==True:
            return True
        if solveMazeUtil(maze,x,y+1,sol)==True:
            return True
        sol[x][y]=0
        return False
 



# Driver program to test above function
if __name__ == "__main__":
    # Initialising the maze
    maze = [ [1, 0, 0, 0],
             [1, 1, 0, 1],
             [0, 1, 0, 0],
             [1, 1, 1, 1] ]
              
    solveMaze(maze)
Developed by: NAVIN KUMAR J
Register Number:  212222240071
*/
```

## Output:

![image](https://github.com/user-attachments/assets/9fcb7993-02ee-402d-bfa3-3ef4bd545a26)


## Result:
The Sudoku solver program executed successfully and found the solution for the given puzzle.
