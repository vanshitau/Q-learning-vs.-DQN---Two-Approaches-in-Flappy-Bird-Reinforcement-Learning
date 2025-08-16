# Overview
Flappy Bird is a game that emerged in early 2013 and gained popularity within a year. The motive of this game is to help the bird navigate through the pipes to stay alive. This report highlights how Q-Learning and DQN affect the training in terms of the rewards generated and the number of time steps required to solve the task per episode, along with the optimal performance of the agent.

### State/Observation Space: 
The state space in Flappy Bird is the variables that showcase the current situation of the bird. The state space of this project includes the last pipe’s horizontal position, the last top pipe’s vertical position, the last bottom pipe’s vertical position, the next pipe’s horizontal position, the next top pipe’s vertical position, the next bottom pipe’s vertical position, the next next pipe’s horizontal position, the next next top pipe’s vertical position and the next next bottom pipe’s vertical position, the player’s vertical position, the player’s vertical velocity and the player’s rotation. The size of the space can vary as it depends on the value that each state can take. Therefore, the state is continuous as the position and distance can take on a continuous range of values. 
### Action Space: 
The actions in this problem include two actions: “do nothing” and “flap”. The action space is discrete as the action that can be taken is distinctive. 
### Reward Scheme: 
These are the rewards given to the agent when they perform a certain action:

## Algorithm Description
### Q-Learning
The first algorithm that we chose to experiment with was Q-Learning. This is a model-free reinforcement learning algorithm that enables an agent to learn the optimal action-selection policy for any given finite Markov decision process by learning and updating estimates of the action values (Q-values). It operates through repeated interactions with the environment, updating the Q-values based on the rewards received for actions taken in various states. The updates are guided by the Bellman equation, combining immediate rewards with the discounted maximum future rewards expected according to the current policy, adjusted by a learning rate. 

### DQN
The DQN algorithm extends the classic Q-learning by using a deep neural network to approximate the Q-value function. The network predicts Q-values (expected future rewards) for each action given an input state. The primary advantages of using DQN include its ability to handle high-dimensional state spaces, which helps because the environment and state space are very dynamic and would benefit from approximation. 
