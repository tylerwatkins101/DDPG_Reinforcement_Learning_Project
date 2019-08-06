## Project Details

In this project I train a DDPG Reinforcement Learning Agent to improve it's performance in the Reacher environment provided by Unity.

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

This project uses a Unity environment with a single agent. The task is episodic, and in order to solve the environment, your agent must get an average score of +30 over 100 consecutive episodes.

## Software Dependencies

The project was done using python 3 and has the following library dependencies that can be installed using pip:

- unityagents
- numpy
- torch
- matplotlib

## File Descriptions

- Continuous_Control.ipynb - jupyter notebook used to open environment, instantiate and train agent, and save trained model parameters.
- model.py - python module containing Actor-Network and Critic-Network architecture classes.
- ddpg_agent.py - python module containing DDPG Agent, Replay Buffer, and OU Noise classes.
- checkpoint_actor.pth - saved trained actor model parameters.
- checkpoint_critic.pth - saved trained critic model parameters
- Report.md - explains the model parameters, training, and potential future improvements.

## Instructions

To run the code and train the model yourself you'll need to download the Unity environment as well Continuous_Control.ipynb, model.py, and ddpg_agent.py from this repository.

Open the Continuous_Control.ipynb jupyter notebook in your browser and run the code cells from top to bottom. In the notebook you'll see a visualization of the agent learning the task and after the agent has scored an average of at least +30 over 100 consecutive episodes the agent's model parameters will be saved to a .pth file.
