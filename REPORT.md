### Instructions

Follow the instructions in `Continuous_Control.ipynb` to get started with training your own agent!

## Algorithm

**Deep Deterministic Policy Gradient** (DDPG) is a model-free policy based learning algorithm in which the agent will learn directly from the un-processed observation spaces without knowing the domain dynamic information. That means the same algorithm can be applied across domains which is a huge step forward comparing with the traditional planning algorithm

- This project repository uses **DDPG** algorithm to solve Unity's Reacher environment.

- The network architectures used (2 neural networks) is a simple, fully-connected neural network with 2 hidden layers of sizes, 400 and 300 units. Model definition can be found in `model.py` file.

- Hyperparameter values chosen are as follows :

| Hyperparameter | Value |
| -------------- | ------ |
| GAMMA | 0.99 |
| BUFFER_SIZE | 9e5 |
| BATCH_SIZE | 2048 |
| TAU | 1e-3 |
| LR_ACTOR | 1e-3 |
| LR_CRITIC | 1e-3 |
| WEIGHT_DECAY | 0 |
| HIDDEN_LAYERS | [64, 128] |
| DEVICE | GPU |

## Rewards Plot

Rewards obtained by agent plotted as function of episodes of training is shown below :

![rewards_plot](https://raw.githubusercontent.com/akshaydp1995/Reacher_Environment/master/rewards.png)

Orange line represents a rolling mean of rewards for latest 100 episodes.
