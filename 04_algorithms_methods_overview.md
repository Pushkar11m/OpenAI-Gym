Uninformed searches 
Dfs : Depth-first search (DFS) is an algorithm for traversing or searching tree or graph data structures. 
        The algorithm starts at the root node (selecting some arbitrary node as the root node in the case of a graph) and 
        explores as far as possible along each branch before backtracking.

Bfs: This algorithm works to find the shortest path to an item, location, or goal state. It does so my searching breadth wise, exploring all neighbor nodes before searching deeper. We used this in our Pacman AI algorithm for eating all the pellets in a maze.

Ucs:
Similar to Dijkstras algorithm, but with the difference that we do have a goal state, and not all the nodes in the graph need to be explored, just the ones that lead to the goal. The algorithm starts at the root node,and it explores nodes in order of the minimum cost back to the root. In other words, it explores the minimum cost  vertices to the root vertex. UCS is complete and optimal, but it explores options in every “direction” and has no information about the goal location

Informed search
Heuristic: Problem specific knowledge that (tries to) lead the search algorithm faster towards a goal state based on how close to goal we are. Often implemented via heuristic function h(n).
       

Dijkstra's algorithm 
It is very similar to Prim’s algorithm for minimum spanning tree. We maintain two sets, one set contains vertices included in shortest path tree, other set includes vertices not yet included in shortest path tree. At every step of the algorithm, we find a vertex which is in the other set and has a minimum distance from the source.

A*search :
Like Dijkstra, A* works by making a lowest-cost path tree from the start node to the target node. What makes A* different and better for many searches is that for each node, A* uses a function that gives an estimate of the total cost of a path using that node.

Adversarial search :
Minimax : Minimax is a kind of backtracking algorithm that is used in decision making and game theory to find the optimal move for a player, 
          assuming that your opponent also plays optimally.
          In Minimax the two players are called maximizer and minimizer. 
          The maximizer tries to get the highest score possible while the minimizer tries to do the opposite and get the lowest score possible.

Expectimax:In addition to "min" and "max" nodes of the traditional minimax tree, this variant has "chance" ("move by nature") nodes, 
           which take the expected value of a random event occurring.
           Instead of taking the max or min of the utility values of their children, chance nodes take a weighted average, 
           with the weight being the probability that child is reached.

Alpha-beta pruning: 
                 Seeks to decrease the number of nodes that are evaluated by the minimax algorithm in its search tree. It basically avoids expanding nodes
        that wont be played because they will be ignored by the min/max agent(s). 

Markov decision process:

Value iteration:
Value iteration is a method of computing an optimal MDP policy and its value.
Value iteration starts at the "end" and then works backward, refining an estimate of either Q* or V*. There is really no end, so it uses an arbitrary end point.

policy iteration: 
Policy iteration starts with a policy and iteratively improves it. 
It starts with an arbitrary policy π0 (an approximation to the optimal policy works best) and carries out the following steps 
starting from i=0.

Q-learning :
This algorithm is used to find a policy that will indicate which action to take under different circumstances. It takes into account the old Q value, the learning rate, and the learned value which is composed of the reward, discount factor, and estimate of the next optimal Q value. The end result allows an agent to take the best possible action given a specific state.

Cross-Entropy
Cross-Entropy is a term used in machine learning. A set of inputs gets linked to a set of outputs. The desired outputs are given and each iteration the network updates itself so that a set of inputs will predict into the correct outputs.

Epsilon Greedy
Epsilon greedy involves keeping track of probabilites to go down certain paths. When certain paths give good rewards, the probability to go down that path increases. This continues until the good and bad paths are largely taken or avoided.

Reinforcement Learning :
It teaches agents ought to take actions in an environment so as to maximize some notion of cumulative reward. All learning is based on observed samples of outcomes and the agent’s utility is defined by the reward function. RL methods can be classified according to: Model-free or model-based; Value-based or policy-based; On-policy or off-policy.
