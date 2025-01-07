 REPRESENTING THE BOARD AS DATA 
First, you must figure out how to represent the board as data in a variable. On paper, the Tic Tac Toe board is drawn as a pair of horizontal lines and a pair of vertical lines, with either an X, O, or empty space in each of the nine spaces.
In the program, the Tic Tac Toe board is represented as a list of strings. Each string will represent one of the nine spaces on the board. To make it easier to remember which index in the list is for which space, they will mirror the numbers on a keyboard’s number keypad, as shown in Figure 10-2.
The strings will either be 'X' for the X player, 'O' for the O player, or a single space ' ' for a blank space.
So if a list with ten strings was stored in a variable named board, then board[7] would be the top-left space on the board. board[5] would be the center. board[4] would be the left side space, and so on. The program will ignore the string at index 0 in the list. The player will enter a number from 1 to 9 to tell the game which space they want to move on.
The AI needs to be able to look at a board and decide which types of spaces it will move on. To be clear, we will label three types of spaces on the Tic Tac Toe board: corners, sides, and the center. Figure 10-3 is a chart of what each space is.

 

 
 ALGORITHM 
The AI’s smarts for playing Tic Tac Toe will follow a simple algorithm. An algorithm is a finite series of instructions to compute a result. A single program can make use of several different algorithms. An algorithm can be represented with a flow chart. The Tic Tac Toe AI’s algorithm will compute the best move to make.
The AI’s algorithm will have the following steps:
1.      First, see if there’s a move the computer can make that will win the game. If there is, take that move. Otherwise, go to step 2.
2.      See if there’s a move the player can make that will cause the computer to lose the game. If there is, move there to block the player. Otherwise, go to step 3.
3.      Check if any of the corner spaces (spaces 1, 3, 7, or 9) are free. If so, move there. If no corner piece is free, then go to step 4.
4.      Check if the center is free. If so, move there. If it isn’t, then go to step 5.
5.      Move on any of the side pieces (spaces 2, 4, 6, or 8). There are no more steps, because if the execution reaches step 5 the side spaces are the only spaces left.
This all takes place in the “Get computer's move.” box on the flow chart in Figure 10-1. You could add this information to the flow chart with the boxes in Figure 10-4.
 

