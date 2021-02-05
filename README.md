
# Overview

This repository contains my "Project 2" submission for Udacity's nanodegree program, 
"Deep Reinforcement Learning" started in late 2020.

It provides an implementation of a learning agent that solves the "Reacher" environment:
[click here](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher)

# Project Details

In the "Reacher" environment, an agent is a double-jointed arm that tries to position the aim at the 
goal location as long as possible. 
The state space has 33 dimensions, containing the arm's position, rotation, velocity, and angular velocities.
With this state information, the agent has to maximize total reward by selecting actions for the joints of the arm.
At each time step, the 4 available actions correspond to torques associated with the 2 joints of the agent's arm.
Each torque action is associated with a value in range [-1, 1].

The task is episodic, meaning it has clear beginning and an end, and everything gets reset at the start of each episode.
In terms of rewards, +0.1 is provided each time step when the arm is at the goal location.
The environment is considered "solved" when the agent has +30 average score during past 100 consecutive episodes.


There are two different ways to solve the Reacher environment: 1) single agent vs 2) multiple agents.
In the case of the single agent version, the agent must get an average score of +30 over 100 consecutive episodes.
In the case of the multiple agents version, scores across all agents are averaged, and average of this average score overe 100 consecutive episodes is taken. If the double average score of +30 reached over 100 consecutive episodes, then the environment is solved.

Note that to run this Reacher enviroment, the user has to use the provided Unity environment file, and *not* use the environment on the ML-agents GitHub page.


# Getting Started

## Installation
The following instructions have been tested on the linux ubuntu (18.04) environment.

### Python virtual environment
1. Create a python version 3.6 virtual environment. You can use `conda` or `pyenv`.
2. Once you `activate` into the environment, issue the following statements to install required dependencies:

Here is the command:

    pip install numpy matplotlib jupyter torch unityagents

If using `conda`, one can isssue the following command:

    conda create -n myenv python=3.6 numpy matplotlib jupyter torch
    conda activate myenv
    pip install unityagents

Note that I could not install `unityagents` in python3.7, but was able to in python3.6. Hence python version 3.6 is required.

### Unity Environment

#### 1. Download the Unity Environment

To run the notebook, you need to download one of the prepared Unity environment files matching your setup:

##### Version 1: One (1) Agent
- Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
- Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
- Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
- Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)

##### Version 2: Twenty (20) Agents
- Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
- Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
- Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
- Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)


The zip file needs to be placed in the same folder as the training notebook, and uncompressed.

#### 2. Explore the Environment

If the Unity environment has been set up correctly, then the notebook should 
run like the one shown below in the video: [click here](https://www.youtube.com/watch?v=ltz2GhFv04A)

## Instructions

To train an agent for the Reacher environment, you can run the jupyter 
notebook `training_code_reacher.ipynb` in the python environment that you created above.


