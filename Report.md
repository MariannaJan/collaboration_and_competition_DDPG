# Report


## Learning Algorithm


The collaboration and competition problem was framed as a multi agent reinforcement learning task. To solve it the Deep Deterministic Gradient Policy was chosen.

The basis for the implementation was the research paper [*'Human-level control through deep reinforcement
learning'*](https://storage.googleapis.com/deepmind-media/dqn/DQNNaturePaper.pdf).

The DDPG algorithm is an actor critic algorithm, that uses two separate neural networks. The actor network is used to find a deterministic policy and choose the best action. The critic network uses this action to count the action-value and provide feedback for the actor network. As the algorithm needs to run on a continous action space, the exploration is a challange. To provide means of exploration for the actor network, a noise is added to the weights. To maximze the use of already examined experience tuples a so called Experience Replay mechanism is used. It basically puts the experience tuples in a fixed size pool, from which they are sampled randomly. This also helps to avoid any unwanted correlation between chronologically adjacent actions. Both actor and critic networks have their weights optimised on the basis of temporal difference. Each network respectively has a local and target copy. The target copy is what we use as a target for the weights optimisation of the local network. When the new valu for the local weights is established, the previous value of the local weights is used to update the target. However the target weights are not updated all at once, but so called 'soft updates' are used, that are a way of gradually making the target weights closer to the local weights (the process is controlled by the factor TAU).

The actor network consists of three fully connected laers, out of which first two use ReLu activation functions, and the last one uses TanH activation function, to keep the output values in the range between -1 and 1. 

The critic network differs from the actor network only in this, that the last fully connected layer has no activation function. The definitions of both networks can be found in the model.py file.

In the used Unity environment thee are two agents, tasked with playing tennis. The fact that both agents in fact do exactly same things, as their goal is identical, was used to train them both with the same brain.


### Hyperparameter values

## Plot of Rewards

## Ideas for Future Work

Further hyperparameter tuning and longer training, with a goal set to a higher value (like 0.7), to make the agent get better results.
