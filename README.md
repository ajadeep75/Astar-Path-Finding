# Astar-Path-Finding
Data Structures

A-star path finding can be used to find a way to go from one spot to another around barriers. This example just draws the path, based on the coordinates returned.
Make sure to install pygame and tkinter before running the code!!

# Why A* Algorithm?
Informally speaking, A* Search algorithms, unlike other traversal techniques, it has “brains”. What it means is that it is really a smart algorithm which separates it from the other conventional algorithms. This fact is cleared in detail in below sections and it is also worth mentioning that many games and web-based maps use this algorithm to find the shortest path very efficiently (approximation). 

# Working Methodology
F = G + H
One important aspect of A* is f = g + h. The f, g, and h variables are in our Node class and get calculated every time we create a new node.
F is the total cost of the node.
G is the distance between the current node and the start node.
H is the heuristic — estimated distance from the current node to the end node.

# Approach
1. Add the starting square (or node) to the open list.

2. Repeat the following:

A) Look for the lowest F cost square on the open list. We refer to this as the current square.

B). Switch it to the closed list.

C) For each of the 8 squares adjacent to this current square …

If it is not walkable or if it is on the closed list, ignore it. Otherwise do the following.

If it isn’t on the open list, add it to the open list. Make the current square the parent of this square. Record the F, G, and H costs of the square.

If it is on the open list already, check to see if this path to that square is better, using G cost as the measure. A lower G cost means that this is a better path. If so, change the parent of the square to the current square, and recalculate the G and F scores of the square. If you are keeping your open list sorted by F score, you may need to resort the list to account for the change.

D) Stop when you:
Add the target square to the closed list, in which case the path has been found, or Fail to find the target square, and the open list is empty. In this case, there is no path.

3. Save the path. Working backwards from the target square, go from each square to its parent square until you reach the starting square. That is your path.
