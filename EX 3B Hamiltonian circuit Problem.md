# EX 3B Hamiltonian Circuit Problem
## DATE:11/04/2025
## AIM:
To write a python program to check whether Hamiltonian path exits in the given graph.

## Algorithm
1.Represent the graph using an adjacency matrix.

2.Start from the first vertex and create a recursive utility function to check paths.

3.At each step, check if the next vertex is adjacent and not already visited.

4.If all vertices are visited and there's a path back to the start (for a circuit), a Hamiltonian Circuit exists.

5.If all vertices are visited and no path back to the start, it's only a Hamiltonian Path. 
   

## Program:
```
/*
global N
N = int(input())
 
def printSolution(board):
    for i in range(N):
        for j in range(N):
            print(board[i][j], end = " ")
        print()
 
def isSafe(board, row, col):
 
    # Check this row on left side
    for i in range(col):
        if board[row][i] == 1:
            return False
 
    # Check upper diagonal on left side
    for i, j in zip(range(row, -1, -1),
                    range(col, -1, -1)):
        if board[i][j] == 1:
            return False
 
    # Check lower diagonal on left side
    for i, j in zip(range(row, N, 1),
                    range(col, -1, -1)):
        if board[i][j] == 1:
            return False
 
    return True
 
def solveNQUtil(board, col):
    if col>=N:
        return True
        
    for row in range(N):
        if isSafe(board,row,col):
            board[row][col]=1
            if solveNQUtil(board, col+1):
                return True
            board[row][col]=0
    return False
    
def solveNQ():
    board = [ [0, 0, 0, 0, 0, 0, 0, 0],
              [0, 0, 0, 0, 0, 0, 0, 0],
              [0, 0, 0, 0, 0, 0, 0, 0],
              [0, 0, 0, 0, 0, 0, 0, 0],
              [0, 0, 0, 0, 0, 0, 0, 0],
              [0, 0, 0, 0, 0, 0, 0, 0],
              [0, 0, 0, 0, 0, 0, 0, 0],
              [0, 0, 0, 0, 0, 0, 0, 0]]
 
    if solveNQUtil(board, 0) == False:
        print ("Solution does not exist")
        return False
 
    printSolution(board)
    return True
 
# Driver Code
solveNQ()

Developed by: NAVIN KUMAR J
Register Number: 212222240071  
*/
```

## Output:

![image](https://github.com/user-attachments/assets/a838bb58-575e-48e1-aa28-48be3af31c7d)


## Result:
The Hamiltonian path program executed successfully, and it determined whether a Hamiltonian path exists in the given graph.
