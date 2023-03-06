# Mario-AI

Creating an AI that plays mario.<br>
Training 2 agents with 2 different RL algorithms (PPO, DQN) doing 2,000,000 timesteps with each algorithm and comparing the results (can be seen in the word file "Mario AI Project").

## Description

* This project was made on the first semester of the degree's third year.

* This page contains a brief explanation, for a full exlanation about the project (explanation about the libraries in use and the algorithms with comparison data) can be viewed in the file "Mario AI Project".

This project is using jpyter notebook, gym-super-mario-bros, nes-py, pytorch, and 2 stable baselines3 RL algorithms called PPO and DQN in order to set up an environment for training the 2 agents to play mario.<br>

In order to improve the learning process the images of the Mario game are proccessedas gray images using gym.wrappers.GrayScaleObservation because color is a redundant parameter for the purpose of the learning.<br>

In order to for the agent to gain context and "memory" using a frame stack of size 4.<br>

By default gym_super_mario_bros environment use actions space of 256 discrete actions which takes a lot of time for an AI model to learn and a lot of space so we used the SIMPLE_MOVEMENT actions list that contains 7 actions: [ [‘NOOP’], [‘right’], [‘right’, A], [‘right’, B], [‘right’, A, B], [A], [‘left’] ] <br>


## Usage

Open a jupyter notebook environment and copy the cotent in the "Untitled.ipynb" file.<br>

Run all the pip install commands first.<br>

### Train the PPO Model

Trains a model using a PPO algorithm for 1,000,000 timesteps, saves the model every 50,000 in a directory named "ppo_train" and the log in a directory named "ppo_logs" wich can be viewed using tesrorboard. 

### Retrain the model

Loads the last saved model of the PPO and trains it for another 1,000,000 timesteps, saves the model every 50,000 in a directory named "ppo_train2" and the log in a directory named "ppo_logs" wich can be viewed using tesrorboard.

### Test it out

Loads the last saved PPO model (2,000,000 timesteps) and lets it play Mario so the user can watch the results.

### Train a new model using DQN

Trains a model using a DQN algorithm for 1,000,000 timesteps, saves the model every 50,000 in a directory named "dqn_train" and the log in a directory named "dqn_logs" wich can be viewed using tesrorboard. 

### Retrain the model

Loads the last saved model of the DQN and trains it for another 1,000,000 timesteps, saves the model every 50,000 in a directory named "dqn_train2" and the log in a directory named "dqn_logs" wich can be viewed using tesrorboard.

### Test it out

Loads the last saved DQN model (2,000,000 timesteps) and lets it play Mario so the user can watch the results.

## Tools in use

* gym_super_mario_bros - OpenAI Gym environment for Super Mario Bros. & Super Mario Bros 2.
* nes_py - provides the option to play the game using python.
* stable-baselines3 - for the PPO and DQN reinforcement learning algorithms.
* Jupyter Notebook - for writing the code and running the program.



