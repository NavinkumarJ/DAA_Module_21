# EX 3A Knight Tour & Count Path
## DATE:11/04/2025
## AIM:
To write a python program to find minimum steps to reach to specific cell in minimum moves by knight


## Algorithm
1. Define the possible 8 knight moves.

2. Use Breadth-First Search (BFS) to explore all possible moves level by level.

3. Keep track of visited cells to avoid cycles.

4. For each move, check if the position is valid and not yet visited.

5. Stop when the target cell is reached and return the move count.


   

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
    for i in range(N):
        if isSafe(board,i,col)==True:
            board[i][col]=1
            if solveNQUtil(board,col+1)==True:
                return True
            board[i][col]=0
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

![image](https://github.com/user-attachments/assets/90fe5211-ec5b-43e3-b232-81de13d2297c)


## Result:
The program executed successfully, and the minimum number of steps for the knight to reach the target was calculated.
