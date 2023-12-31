Grid world is one of the basic environment models known in reinforcement learning.

Grid_World_MDP.ipynb defines the environment as follows:
- States: The grid has 3x4 = 12 distinct states. The start state is cell (2,0) at the bottom left corner and the terminal state is either at cell (0,3) or at cell (1,3). The grey cell represents a wall and can not be moved to.
- Actions: The agent is allowed to choose one of 4 actions which are: Up, Down, Left, and Right with equal probability.
- Environment Dynamics: The environment is deterministic, where a given state and action always lead to the same new state.
- Rewards: The agent gets a reward of +1 when it gets to state (0,3) and a -1 reward when reaching state (1,3); other than that it gets 0.

This is a finite Markov decision process (MDP) in which the goal is to find the agent policy which maximizes its future discounted reward. The code also solves it using a system of linear equations

Dynamic programming is implemented in Grid_World_Policy_Iteration.ipynb and finds the optimal policy for the agent using policy iteration technique with:
- Discount factor of 0.9.
- Acceptable Tolerance of 0.05 or less.

Feel free to change the the starting state of the agent and other paremeters such as discount factor and tolerance to see how it affects policy iteration.