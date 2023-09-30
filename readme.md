## Application of Reinforcement Learning in Bitcoin Trading
The model being used is a combination of the Proximal Policy Optimization (PPO) algorithm and the Advantage Actor-Critic (A2C) policy network. 

In this model, we state the RL problem as predicting optimal actions (buy, hold, or sell) to optimize portfolio value based on the input states, which consist of price and technical indicators. The price represents the current market price of a financial asset, while the technical indicators provide additional information about the asset's past performance and market trends.

To process the input states and make predictions, different neural network architectures were experimented with in the A2C network, including Long Short-Term Memory (LSTM) networks, Convolutional Neural Networks (CNN), and dense networks. Among these architectures, the dense network architecture performed the best.

## MDP formation
![mdp](https://github.com/ALEXdotR/Application-of-Reinforcement-Learning-in-Bitcoin-Trading/assets/72406898/c789fd59-d6df-4c97-b71d-caebd92078f7)

States - Set of states which includes the price and technical indicators

Actions - Set of actions which includes {buy, hold, sell}

Reward - the growth of portfolio value


## Architecture

The proximal policy optimization (PPO) is used as an implementation of the reinforcement learning.

<img width="739" alt="PPO structure" src="https://github.com/ALEXdotR/Application-of-Reinforcement-Learning-in-Bitcoin-Trading/assets/72406898/511407e5-d513-496d-8ed5-9c029b700555">

*Structure of the PPO strategy*

An action-to-critic (a2c) model is used as the policy network in PPO, the following is its structure. Note that in our implementation, we have also tried using LSTM and CNN to replace the shared model layer.

<img width="522" alt="a2c structure" src="https://github.com/ALEXdotR/Application-of-Reinforcement-Learning-in-Bitcoin-Trading/assets/72406898/eabb67b8-e4f9-4de8-8d4b-50be1f21bfd7">

*Structure of a2c policy network*

## Result

<img width="500" alt="different model in a2c" src="https://github.com/ALEXdotR/Application-of-Reinforcement-Learning-in-Bitcoin-Trading/assets/72406898/b886caa8-a860-47ff-a75c-0cdf0e52c10e">

*The result of using different models in the a2c model*

<img width="666" alt="distribution of return" src="https://github.com/ALEXdotR/Application-of-Reinforcement-Learning-in-Bitcoin-Trading/assets/72406898/022caecb-9d43-40f7-825a-93669f021ae7">

*Distribution of return under different training episodes, with the red line being the median return*

<img width="479" alt="earn ratio by episode" src="https://github.com/ALEXdotR/Application-of-Reinforcement-Learning-in-Bitcoin-Trading/assets/72406898/ed93f297-e999-4ef5-89ea-2ba5d5175a99">

*Earn ratio to episodes*

