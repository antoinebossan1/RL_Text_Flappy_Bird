# Comparison of Lambda SARSA and Monte Carlo Q (MCQ) Learning Algorithms

## Overview

This project is dedicated to comparing two reinforcement learning algorithms, Lambda SARSA and Monte Carlo Q (MCQ), using the Text Flappy Bird environment from OpenAI Gym. The aim is to evaluate the performance of these algorithms in learning optimal policies for playing Text Flappy Bird, a terminal-based version of the popular game.

## Installation

First, install the Text Flappy Bird gym environment using the following command:

```shell
!pip install git+https://gitlab-research.centralesupelec.fr/stergios.christodoulidis/text-flappy-bird-gym.git
```


## Algorithm Implementation

Two agent classes are implemented: `MC_Q_Agent` for Monte Carlo Control with Epsilon-Greedy Policy, and `Lambda_SARSA_Agent` for the Lambda SARSA algorithm. Both algorithms are evaluated over a series of episodes to compare their effectiveness in navigating the game.

### MC_Q_Agent

Implements the Monte Carlo Q-learning algorithm, utilizing an epsilon-greedy policy for action selection and learning the state-action values.

### Lambda_SARSA_Agent

Implements the Lambda SARSA learning algorithm, incorporating eligibility traces to efficiently update state-action values and employing an epsilon-greedy policy for action selection.

## Experiments

The experiments are divided into two main parts:

1. **Parameter Sweeping**: To identify the best hyperparameters for each algorithm.
2. **Performance Comparison**: To evaluate and compare the performance of Lambda SARSA and MCQ agents using the optimal parameters found in the previous step.

### Parameter Sweeping

For each algorithm, a range of parameters for epsilon (exploration rate), discount factor, and, for Lambda SARSA, the lambda parameter and step size are swept to find the combination that yields the best performance in terms of game score.

### Performance Comparison

Using the best parameters identified, both algorithms are then compared based on the average rewards and scores obtained over a number of episodes. 

## Results Visualization

Plots are generated to visualize the parameter sweeping results, performance comparison in terms of average rewards and scores, and state-value function plots to illustrate the learned values across different game states.
