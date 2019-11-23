# Purpose
The purpose of this project is to design an AI program plays the game against dumb to smart players by adopting pure Monte Carlo Tree search algorithm.
# Process
## Step 1: The Language of Choice

Python has a great community support for Artificial Intelligence libraries and many other benefits Artificial Intelligence development such as:
  - consistency and simple syntax
  - extensive selection of libraries and frameworks
  - Platform independence
  - Great community and popularity

With these benefits in mind, I chose python3 for this project.

## Step 2: The Understanding of Algorithm

Before implementing algorithm, I needed to understand the logic of pure Monte Carlo Tree Search. The pMCTS basically says, for each move, all feasible moves are determined: k random games are played out to the very end, and the scores are recorded. The move leading to the best score is chosen. Ties are broken by fair coin flips.

The challenging part is to find the minimum number of play-outs that guarantees 100% win rate or draw, but no loss, against a smart player.

## Step 3: The Implementation

Coding was fairly straight-forward although time complexity and data structures needed to be carefully chosen.

Based on the understanding of the algorithm, I found that there always has to be a new move recorded in the gameboard and checked before either a human player or computer decides the next move. Therefore, python dictionary met this need and the algorithm was designed in O(N^2) because each column of rows or row of columns needs to be checked every time a new move is made.

## Step 4: Final Result & Reflection

As a result, my AI program guarantees 100% win rate or draw if the number of playouts (simulates games itself given a move) exceeds to 300 playouts which takes about maximum 5 seconds to decide a move.

From this project, I learned that algorithm design with respect to time complexity is crucial for real-time applications and it was fun to learn a basic AI algorithm for the first time!
