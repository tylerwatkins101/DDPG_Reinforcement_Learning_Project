## Project Details

In this project I train a DDPG Reinforcement Learning Agent to improve it's performance in the Reacher environment provided by Unity.

![Reacher](photos/reacher.gif)

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

This project runs locally on Windows 10 environment. Here are the steps to setup the environment:
1. Create (and activate) a new environment with Python 3.6.
	```
	- __Windows__: 
	```bash
	conda create --name drlnd python=3.6 
	activate drlnd
	```

2. Install these dependencies in the environment on windows 10
	- __Install Unity ML-Agents__
	```bash
	pip3 install --user mlagents
	```	
	- __Install Unity Agents__
	```bash
	pip install unityagents
	```	
	- __Install Pytorch__
	```bash
	conda install pytorch torchvision cudatoolkit=9.0 -c pytorch
	```
3. Download the `Reacher` environment from one of the links below and select the environment that matches your Windows operating system:
    - **_Version 1: One (1) Agent_**
        - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
        - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)
 
4. Place the file in the `continuous_control/` folder, and unzip (or decompress) the file.

5. Open the Continuous_Control.ipynb jupyter notebook in your browser and run the code cells from top to bottom. In the notebook you'll see a visualization of the agent learning the task and after the agent has scored an average of at least +30 over 100 consecutive episodes the agent's model parameters will be saved to a .pth file.
