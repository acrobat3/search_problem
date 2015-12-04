# search_problem

Finding Paths
_______________________________

It can run on your terminal with command in following.

** DFS Finding Paths **

python pacman.py -l tinyMaze -p SearchAgent  ---- This command use tinyMaze as the map for searching.

python pacman.py -l mediumMaze -p SearchAgent ---- This use mediumMaze.

python pacman.py -l bigMaze -z .5 -p SearchAgent ---- This is for bigMaze.

_____________________________________________________

** BFS Finding Paths **

python pacman.py -l mediumMaze -p SearchAgent -a fn=bfs ----- This command use mediumMaze as the map for searching

python pacman.py -l bigMaze -p SearchAgent -a fn=bfs -z .5 ----- This use bigMaze

If Pacman moves too slowly for you, try the option --frameTime 0 after any command.

_____________________________________________________

** UniformCostSearch Finding Paths **

python pacman.py -l mediumMaze -p SearchAgent -a fn=ucs ----- This command use mediumMaze as the map

python pacman.py -l mediumDottedMaze -p StayEastSearchAgent ----- This map make the right zone lesser cost than left zone by put foods there

python pacman.py -l mediumScaryMaze -p StayWestSearchAgent ----- This map make the right zone more cost than left zone by put enemies there

________________________________________________________

** A star Search Finding Paths **

python pacman.py -l bigMaze -z .5 -p SearchAgent -a fn=astar,heuristic=manhattanHeuristic ----- This use bigMaze as the map and use A* to search paths 

________________________________________________________

** Solved food on four corner problem **

python pacman.py -l tinyCorners -p SearchAgent -a fn=bfs,prob=CornersProblem

python pacman.py -l mediumCorners -p SearchAgent -a fn=bfs,prob=CornersProblem

This's like above command but change problem to solve

_______________________________________________________

** Solved anywhere food problem **

python pacman.py -l testSearch -p AStarFoodSearchAgent

Note: AStarFoodSearchAgent is a shortcut for -p SearchAgent -a fn=astar,prob=FoodSearchProblem,heuristic=foodHeuristic.

__________________________________________________________


The Pacman board will show an overlay of the states explored, 
and the order in which they were explored (brighter red means earlier exploration).


You can find code of search algorithm in search.py
and conner problem solver "searchAgent" in searchAgents.py 
