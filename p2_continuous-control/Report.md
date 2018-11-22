# Project 2 Report

## Learning Algorithm

We use the Deep Deterministic Policy Gradients ([DDPG](https://arxiv.org/abs/1509.02971)) learning algorithm in this project. DDPG is an off-policy model-free algorithm that uses neural networks to learn policies, even in high-dimensional and continuous action spaces. The implementation is a DDPG agent with three fully connected layers: hidden layers of 500 and then 375 units, each with ReLU activation, and an output layer of 4 units with tanh applied in order to bound the output between -1 and 1. That was the actor network specifically. The critic network is similar, except that tanh is not applied to the output layer and the action vector is included between the first and second hidden layers. The hyperparameters are as follows:

| Hyperparameter | Value |
| ------------- | ------------- |
| first hidden layer units | 500 |
| second hidden layer units | 375 |
| replay buffer size | 1e5 |
| batch size | 128 |
| discount factor (gamma) | 0.99 |
| tau* | 1e-3 |
| actor learning rate | 1e-4 |
| critic learning rate | 1e-3 |
| number of episodes | 1000 |
| max time steps per episode | 1000 |
| L2 weight decay | 0 |

*Tau is the percentage of weights from the local model to carry over to the target model during the soft update of target parameters; meanwhile, `1 - tau` is the percentage of target model weights to carry over.

## Plot of Rewards

The plot below shows that, after 164 episodes, the agent is able to receive an average reward of 30 over the last 100 consecutive episodes.

![final_model_rewards_plot](./final_model_rewards_plot.png)

## Ideas for Future Work

Ideas for improving the agent's performance are as follows:
- Attempt prioritized experience replay, TRPO, TNPG, PPO, or D4PG.
- Solve the environment in fewer than 150 episodes.
- See how large the rewards can get before the environment is solved (do not stop at 30).
