# Description

The idea of pure Monte Carlo Tree Search (pMCTS) is as follows:
When it’s the computers turn to make a move, it makes a list of all legals moves. 
Then for each of these moves it does some number of random playouts. 
A random playout is when the computer simulates playing the game — using randomly chosen moves — until it is over, i.e. a win, loss, or draw is reached.
It records the result (a win, loss, or draw), and then does some more random playouts. 
It does random playouts for every possible move, and when they’re done it choses the move that resulted in the least number of losses, if there are more than one move with the same number, then the numbers of wins and draws are compared accordingly. 
With enough random playouts, this approach will play essentially perfectly.

