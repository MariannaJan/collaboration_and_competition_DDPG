# Collaboration and competition

Multi agent reinforcement learning problem in a Unity environment solved with Deep Deterministic Policy Gradient

![tenni](/tennis.gif)

*Source: https://github.com/udacity/deep-reinforcement-learning/tree/master/p3_collab-compet*

## Project Details

In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

The task is episodic, and in order to solve the environment, your agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,

After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores. This yields a single score for each episode.

The environment is considered solved, when the average (over 100 episodes) of those scores is at least +0.5.

## Getting Started

To run this repo on your local machine, first clone this repository https://github.com/udacity/deep-reinforcement-learning

Follow the instruction in the README file in the root of the folder to install the Python environment needed to run the whole project.

Follow the instructions in the README of p3_collab-compet (https://github.com/udacity/deep-reinforcement-learning/tree/master/p3_collab-compet) to install the correct environment for Your operating system. You don't need to install Unity separately, as Unity Agents are already configured in the environment.

Finally place the files from this repo into the p1_navigation folder of the deep-reinforcement-learning repository and run the Jupyter Notebook Tennis.ipynb. Make sure the name of the environment you downloaded matches the one specified in the code env = UnityEnvironment(file_name="/data/Tennis_Linux_NoVis/Tennis")

## Instructions

To run the code, simply open the Tennis.ipynb notebook.
To train the agent from scratch just run the ddpg function.
