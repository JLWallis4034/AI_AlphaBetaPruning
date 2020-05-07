AI Tutorial: Minimax and Alpha-Beta Pruning

1. Overview
"Minimax" is an AI algorithm that works in tandem with a similar AI algorithm called "Maximin." In short, Minimax works to "minimize" the loss that occurs in a "worst case" situation. Maximin works in reverse: the goal of the algorithm is to "maximize" the lowest possible gain in a situation. These algorithms have many functions, one of which involves multiplayer AI-based games.

Alpha-beta pruning is often seen as an extension of the minimax algorithm, as it seeks to reduce the amount of searching the latter has to do in order to reach its goal. Like minimax, it also shines in multiplayer games involving AI.

2. How do minimax and alpha-beta pruning work?
Minimax, in essence, works as a form of depth-first search in reverse. Suppose you create a game in which two AI play against each other. AI One will be denoted as the "maximizing player," while AI Two will be the "minimizing player." This means that AI One will attempt to reach the highest score possible, while AI Two will do the exact opposite and seek the lowest score. Beginning at the root of the tree (which is counted as layer 0) and beginning with the maximizing player, the AIs will alternate turns until you reach the second-lowest layer of the tree. For example, a tree with a depth of 4 layers means that 4 turns will be taken, beginning with the maximum player and ending 3 turns later with the minimum player.

Once the second-lowest layer of the tree is reached, you can begin working up back to the root node. For each parent node in the next-to-last layer, each of two child nodes are checked. Let's return to our assumption that the tree has 4 layers. Since the last player to move was the minimizing player, each child node is checked to determine the lowest of the two. That value is placed onto the parent node. Once each parent node in the next-to-last layer is checked, the program moves a layer up and repeats the process with the maximizing player; this means the higher values are taken and placed onto the parent nodes. This repeats until the root node is reached, in which the maximizing player chooses the highest node. From here, the path to take to reach the "optimal" solution has been found.

Alpha-beta pruning, as stated before, is able to help a minimax algorithm reach its goal much faster. Alpha-beta pruning works as follows: as the minimax algorithm works its way up a tree, each player selects the most beneficial moves to them. Working from the bottom up allows each player to make the best possible decision. However, if a player finds a move that is determined to be worse than a move that was previously examined, it isn't necessary to look further into the results of selecting that move. As such, alpha-beta pruning disregards that node and its resulting nodes entirely.

If that all sounds confusing, it kind of is. Provided within the repository is a picture and a Visual Studio solution that can hopefully shed a bit more light on both minimax and alpha-beta pruning if you still need some help understanding them.

3. What makes minimax and alpha-beta pruning useful?
Minimax is a useful algorithm in the world of AI. It has been used in many ways relating to AI decision-making, as it can help the AI to determine the best way to approach different situations. Much of this can be seen in games where AI opponents are used, such as chess. By giving values to specific pieces on the board, two AI opponents can use the algorithm to determine the best move to victoriously reach the end of the game. Alpha-beta pruning can help to enhance the speed of certain AI algorithms like this by lowering the computational time spent deciding moves.

4. Further Reading
Many sources were used in order to make this tutorial as clear-cut and (hopefully) understandable as possible. They are listed below for anyone wanting to take a deeper dive into either of these algorithms.

https://www.geeksforgeeks.org/minimax-algorithm-in-game-theory-set-4-alpha-beta-pruning/ - This website contains a code example for minimax and alpha-beta pruning. The code in the Visual Studio project is very much based on the code here, with some adjustments.

https://en.wikipedia.org/wiki/Minimax and https://en.wikipedia.org/wiki/Alpha%E2%80%93beta_pruning - Although Wikipedia is a freely editable website, these pages did seem to provide ample information regarding both minimax and alpha-beta pruning that would succeed in helping anyone who wishes to learn more.

https://www.youtube.com/watch?v=DZfv0YgLJ2Q - While not a "tutorial," this video was sort of the starting point to this project. Just a video of a guy creating a chess AI utilizing both minimax and alpha-beta pruning. He does go over the basics of each algorithm, as well as provide a nice bit of entertainment if you have some time to spare.
