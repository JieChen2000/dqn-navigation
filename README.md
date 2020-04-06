[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"

# DQN Navigation Example

### Introduction

For this project, you will train an agent to navigate (and collect bananas!) in a large, square world.  

![Trained Agent][image1]

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.  

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, the agent must get an average score of +13 over 100 consecutive episodes.

### Enviroment Setup

The code is written in PyTorch and Python 3.

1. Clone this repo by
* git clone https://github.com/JieChen2000/dqn-navigation.git

2. Current code is tested with the Unity Machine Learning Agents (ML-Agents) environment on windows 64-bit operating system, download the enviroment
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

3. Place the file in the this GitHub repository, and unzip (or decompress) the file.

4. Install openai gym, which is required by ML-Agents.
* `git clone https://github.com/openai/gym.git`
* `cd gym`
* `pip install -e . `

### Running Instructions
* `pip install -r requirement.txt` //this install the required pytorch, numpy etc.
* `python train_agent.py`  //this will call the DQN algorithm implementated in dqn_agent.py and model.py. The agent will solve the problem once it gets rewards of +15. The model weight wil be saved to a checkpoint.pth.

### Demo and Algorithm Description

The report `report.ipynb` describes the learning algorithm, along with the chosen hyperparameters. It also describes the model architectures for any neural networks. A plot of rewards per episode is included to illustrate that the agent is able to receive an average reward (~ 600 episodes) of at least +15.