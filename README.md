# Tic-Tac-Toe Using Reinforcement Learning

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Table of Contents
- [Overview](#overview)
- [Author](#author)
- [Reinforcement Learning Approach](#reinforcement-learning-approach)
- [Key Features](#key-features)
- [Repository Structure](#repository-structure)
- [Implementation Details](#implementation-details)
  - [Deep Q-Network Architecture](#deep-q-network-architecture)
  - [Training Process](#training-process)
  - [Evaluation Metrics](#evaluation-metrics)
- [Sample Outputs](#sample-outputs)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)
- [Future Work](#future-work)
- [License](#license)

## Overview
This repository contains an implementation of a Tic-Tac-Toe agent using Deep Q-Networks (DQN), a reinforcement learning technique. The agent learns to play the game by interacting with the environment and optimizing its strategy based on rewards received after each action.

## Author
- Sashwat Desai (desai.sas@northeastern.edu)
  - MS, Applied Mathematics
  - Northeastern University, Boston

## Reinforcement Learning Approach
The implementation uses a Deep Q-Network (DQN) approach, where:
- The agent learns a Q-function that estimates the expected future rewards for each action in a given state
- Neural networks are used to approximate the Q-function, enabling the agent to generalize across states
- Experience replay is employed to improve learning stability and efficiency
- The agent balances exploration and exploitation using an epsilon-greedy strategy

## Key Features
- Complete Tic-Tac-Toe environment implementation
- Deep Q-Network agent with experience replay
- Visualization of the learning process
- Documentation of the algorithm through pseudocode
- Sample outputs showing the agent's performance
- Support for both agent vs. agent and human vs. agent gameplay

## Repository Structure
- **code/** - Implementation code
  - **dqn_final.ipynb** - Main Jupyter notebook containing the full implementation
  - **placeholder.md** - Placeholder file
- **pseudocode/** - Documentation of the algorithm
  - **Pseudocode for 3x3 Tic - Tac - Toe Using Deep Q - Networks.pdf** - Detailed algorithm explanation
  - **placeholder.md** - Placeholder file
- **sample-outputs/** - Example outputs and visualizations
  - **agent-drawing/** - Examples of games ending in draws
    - **draw 1.png** - First draw example
    - **draw 2.png** - Second draw example
    - **placeholder.md** - Placeholder file
  - **agent-winning/** - Examples of agent winning games
    - **agent winning 1.png** - First win example
    - **agent winning 2.png** - Second win example
    - **agent winning 3.png** - Third win example
    - **agent winning 4.png** - Fourth win example
    - **placeholder.md** - Placeholder file
  - **placeholder.md** - Placeholder file
- **LICENSE** - MIT License
- **README.md** - Project documentation
- **requirements.txt** - Python package dependencies

## Implementation Details

### Deep Q-Network Architecture
The implementation uses a neural network architecture consisting of:
- Input layer representing the game state (9 positions on the Tic-Tac-Toe board)
- Hidden layers with ReLU activation functions
- Output layer representing Q-values for each possible action (9 positions)

### Training Process
The agent is trained through the following steps:
1. Initialize the Q-network with random weights
2. For each episode:
   - Reset the environment to the initial state
   - For each step in the episode:
     - Select an action using epsilon-greedy policy
     - Execute the action and observe reward and next state
     - Store experience in replay memory
     - Sample a batch from replay memory
     - Update Q-network weights using gradient descent
   - Decrease exploration rate (epsilon)

### Evaluation Metrics
The agent's performance is evaluated based on:
- Win rate against a random player
- Win rate against a minimax player
- Number of draws vs. losses
- Average number of moves to win

## Sample Outputs
The repository includes sample outputs showing:
- The agent successfully winning games
- Games ending in draws
- Visualization of the agent's decision-making process

## Setup and Installation
```bash
# Clone this repository
git clone https://github.com/desai-sashwat/tic-tac-toe-RL.git
cd tic-tac-toe-RL

# Install required packages from requirements.txt
pip install -r requirements.txt
```

## Usage
The main implementation is in the Jupyter notebook `code/dqn_final.ipynb`. To use:

1. Open the notebook in Jupyter:
```bash
jupyter notebook code/dqn_final.ipynb
```

2. Run the cells sequentially to:
   - Define the Tic-Tac-Toe environment
   - Implement the DQN agent
   - Train the agent
   - Evaluate the agent's performance
   - Play against the trained agent

## Future Work
Potential enhancements for this project include:
- Implementing additional reinforcement learning algorithms (e.g., PPO, A3C)
- Extending to larger board sizes (4x4, 5x5)
- Developing a web-based interface for human vs. agent gameplay
- Adding support for variants of Tic-Tac-Toe (e.g., Ultimate Tic-Tac-Toe)
- Comparing performance with other machine learning approaches

## License
This project is licensed under the MIT License - see the LICENSE file for details.
