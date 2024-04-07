# Solving-Maze-Problems
# Overview
We aim to efficiently navigate through mazes, unraveling their intricate pathways and finding optimal solutions using Depth-First Search (DFS) and Breadth-First Search (BFS) algorithms.
Through this exploration, we seek to deepen our understanding of algorithmic problem-solving and its practical applications in maze traversal and beyond.

## Introduction
The problem of maze-solving is a prevalent challenge in artificial intelligence and
robotics. It involves navigating an agent through a maze from a specified start state to a goal
state while avoiding obstacles or walls. Maze-solving algorithms play a crucial role in various
real-world applications, including robotics, pathfinding, and game development.

In this report, our objective is to implement and compare the performance of two well-known
search algorithms, Depth-First Search (DFS), and Breadth-First Search (BFS), in solving maze
problems. To analyze and discuss the effectiveness of these algorithms in finding optimal paths
within a 20x20 grid maze.

In the following sections, we will provide a background on DFS and BFS algorithms, outline
the formal analysis, which includes PEAS representation, describes the maze environment,
present the implementation and discuss the results.

## Background

### Maze-Solving in Artificial Intelligence
Maze-solving is a fundamental problem in artificial intelligence, often used as a
benchmark for evaluating search and pathfinding algorithms. The goal is to determine the
optimal or shortest path from the starting point to the destination while avoiding obstacles.

### Depth-First Search (DFS) and Breadth-First Search (BFS)
DFS and BFS are two widely used graph traversal algorithms. They are commonly employed
in solving maze problems and pathfinding tasks.

* **Depth-First Search (DFS)**: DFS explores as far as possible along a branch before backtracking. It
uses a stack data structure to manage the exploration order.

* **Breadth-First Search (BFS)**: BFS explores all the nodes at the current depth before moving on to
the next level. It uses a queue data structure to manage the exploration order.

These algorithms have distinct characteristics and are suited for different scenarios.

## Formal Analysis

### PEAS Description
PEAS descriptions are used to define the scope and objectives of an AI system or agent, This
helps in designing, developing, and evaluating intelligent systems effectively. For our maze
problem, we represented the PEAS description as follows:

* **Performance Measure**: The performance measure for our agent is its capability to find
the shortest path from the start state to the goal state within the maze while avoiding
collisions with walls.

* **Environment**: The walls and the available routes.
  
* **Actuators**: Motors for movement control (Forward, Backward, Left, Right).
  
* **Sensors**: Our agent uses sensors to avoid crashing into a wall and to keep track of the
path.

### Environment type
Regarding the environment type, there are several key features within our maze
environment.

To begin with, we classify it as **fully observable** because the agent within the maze possesses
unrestricted access to all pertinent information about its surroundings. This characteristic also
designates it as a **deterministic** environment since all actions taken by the agent yield entirely
predictable outcomes.

Moreover, it qualifies as a **sequential** environment, given that each action influences
subsequent actions. It is **static**, as the environment remains unchanged while the agent
interacts with it. Additionally, it can be described as **discrete** since we have a finite number of
well-defined states. Lastly, it is a **single-agent** environment, consisting of only one agent.

### Formulation Of the Search Problem
For every problem, the world has a formulation, and it can be formulated by the initial
state, goal state, state space, operators, and assumptions if we have it in the problem,
Figure 1.0 shows the problem, or in other words, the maze we’re dealing with. So, for the maze
the problem we have:

#### States
We have two main states, the initial and goal states.

The **Initial State** is the point colored green, the starting point for the maze.

The **Goal State** is the red point, or the exit that we want to go for to solve the
maze.

The state space covers all possible cells within the maze as each state aligns with a
specific locator cell within the labyrinth in the maze scenario.

#### Operators
The operators are the actions that agents take to move around the maze.
For our agent, the actions are:

  **Move Forward**: Go one cell forward your current position (if there's no wall).

  **Move Backward**: Go one cell behind your current position (if there's no wall).

  **Move Left**: Go one cell to your left (if there's no wall).

  **Move Right**: Go one cell to your right (if there's no wall).

#### Assumptions
For the maze problem, our solution goes accordingly with a few assumptions we made:

* The maze is like a grid with walls and open paths.
  
* You start at a well-known spot in the maze.
  
* You can't walk through walls; you can only move to open cells.
  
* We assume there's at least one way to get from the starting point to the exit;
otherwise, it's an unsolvable problem.

## Figure 1: A 19x19 maze
![](https://github.com/Raiyan-S/Solving-Maze-Problems/blob/main/Maze.png)

### Final Path BFS
![](https://github.com/Raiyan-S/Solving-Maze-Problems/blob/main/Final%20Path%20BFS.png)

#### Here's an animation on how it works:
![](https://github.com/Raiyan-S/Solving-Maze-Problems/blob/main/BFS.gif)

### Final Path DFS
![](https://github.com/Raiyan-S/Solving-Maze-Problems/blob/main/Final%20Path%20DFS.png)

## Conclusion
In conclusion, the choice between DFS and BFS in solving maze problems depends on the
specified constraints and requirements, while DFS is efficient in terms of memory usage. It doesn’t
necessarily find the shortest path, we just happened to use a test case where DFS found a shorter path.
As for BFS, it might find the shortest path, but it uses more memory than DFS. This has
provided valuable insights into applying these two algorithms to a maze problem.

As we are diving into the field of artificial intelligence, the knowledge gained from this study
can contribute to making more sophisticated algorithms and agents for the navigation of complex
environments, and later on use it in an even broader project, such as game development.

## References
* [Audaris Blades. (2020, March 08). Solving mazes with Depth-First Search.](https://medium.com/swlh/solving-mazes-with-depth-first-search-e315771317ae)

* [Panigrahi, Kiran Kumar. (2023, Feb 20). tutorialspoint: difference-between-bfs-and-dfs.](https://www.tutorialspoint.com/difference-between-bfs-and-dfs)

* Stuart Jonathan Russell, Peter Norvig. (2010). Artificial Intelligence.

* [Timur Bakibayev. ( 2020, June 2). solve a maze with python.](https://levelup.gitconnected.com/solve-a-maze-with-python-e9f0580979a)
