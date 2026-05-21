<h1 align="center">AMSS 2025 Module 8</h1>
<h2 align="center">Reinforcement Learning and Deep RL</h2>
<h3 align="center">Session Date: Sep 6, 2025</h3>

# Reinforcement Learning and Deep RL

## Introduction
Reinforcement Learning (RL) differs from supervised and unsupervised methods by focusing on learning through interaction. An agent explores its environment, makes decisions, receives feedback in the form of rewards or penalties, and improves its strategy over time. This process resembles how people learn tasks such as cycling or playing games. The summary introduces the core framework, major algorithms, and recent advances in deep reinforcement learning.

## Core Concepts and Framework

### Interaction Model
- **Agent and Environment**: The agent observes the state of the environment, takes an action, and receives a reward.  
- **Sequential Decisions**: Each action affects immediate outcomes and future possibilities.  
- **Markov Decision Process (MDP)** defines RL with:
  - States (S): Descriptions of the environment.  
  - Actions (A): Choices available.  
  - Transition Probabilities (P): Likelihood of moving between states.  
  - Rewards (R): Signals that guide learning.  
  - Discount Factor (γ): Weighs short-term versus long-term gains.  

### Key Differences from Supervised Learning

| Aspect | Supervised Learning | Reinforcement Learning |
|--------|---------------------|------------------------|
| Data | Labeled, fixed datasets | No initial data; collected through interaction |
| Objective | Improve prediction accuracy | Maximize long-term cumulative reward |
| Data Structure | Independent and identically distributed | Sequential, depends on past actions |
| Exploration | Not required | Essential (exploration vs exploitation) |

### Exploration vs Exploitation
- **Exploration**: Trying new actions to gain knowledge.  
- **Exploitation**: Using existing knowledge to maximize reward.  
- **Trade-off**: A balance is needed, as excessive exploitation limits discovery and excessive exploration reduces efficiency.  

## Reinforcement Learning Algorithms

### Multi-Arm Bandits (MAB)
A simple setting with no states, only actions linked to unknown reward probabilities.  
- **Goal**: Maximize cumulative rewards or minimize regret.  
- **Strategies**:  
  - Epsilon-Greedy: Random exploration with some probability.  
  - Upper Confidence Bound (UCB): Chooses actions with high estimated value and uncertainty.  
  - Thompson Sampling: A Bayesian approach sampling from posterior distributions.  

| Algorithm | Pros | Cons |
|-----------|------|------|
| Epsilon-Greedy | Easy to use, simple | Needs careful tuning, may underexplore |
| UCB | Balances value and uncertainty | Computationally expensive |
| Thompson Sampling | Efficient, strong performance | Posterior estimation may be complex |

### Contextual Bandits
Extends MAB by adding context such as user information or product features. Examples include LinUCB and Bayesian contextual methods.

### MDP-Based Reinforcement Learning
- **Value Functions**: Estimate expected returns for states and actions.  
- **Policies**: Can be deterministic or stochastic.  
- **Bellman Equations**: Recursive relationships central to RL.  

### Model-Free Algorithms
- **Q-Learning**: Learns action-value functions without modeling transitions.  
- **Policy Gradient**: Directly optimizes policies using gradients.  
- **Deep RL**: Combines RL with neural networks.  
  - Deep Q-Networks (DQN): Neural networks approximate Q-values.  
  - Experience Replay: Stores past interactions for stable learning.  
  - Target Networks: Reduce instability during updates.  

## Applications of Deep RL

### Game Playing
- **Atari Games**: Agents trained from raw pixels achieved human-level or better performance.  
- **AlphaGo and AlphaZero**: Combined deep RL with search methods to master complex board games.  
- **StarCraft II**: RL agents reached competitive performance in large-scale strategy games.  

### Why Deep Learning Helps
- Handles raw sensory inputs such as images.  
- Learns internal feature representations automatically.  
- Generalizes across unseen states and environments.  

## Summary and Takeaways

| Aspect | Reinforcement Learning | Deep RL |
|--------|------------------------|---------|
| Data | Collected by interacting with environment | Stored in replay buffers for training |
| Function Approximation | Optional, simple methods possible | Essential, neural networks approximate functions |
| Exploration | Central challenge | Same, with added complexity |
| Applications | Robotics, operations, recommendations | Complex games, self-driving, advanced control |

>[!NOTE]
> Reinforcement Learning provides a structured way to model decision-making over time. With the integration of deep learning, RL has progressed to solving tasks once thought impossible for machines, from classic games to real-world control systems. Research continues to refine algorithms for stability, efficiency, and generalization, making RL one of the most promising areas in modern artificial intelligence.