# Navigation_Udacity_DRLND_P1

Project 2: done as part of the [Udacity Deep Reinforcement Learning Nanodegree](https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893). The objective of this project is to create a Deep Deterministic Policy Gradient Learning agent that is able to maximize the reward in the [Unity ML-Agents](https://github.com/Unity-Technologies/ml-agents) based [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) continuous environment.

## Game Environment Details

![Game Environment](https://video.udacity-data.com/topher/2018/June/5b1ea778_reacher/reacher.gif)

The environment has an Agent with a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of the agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

The environment is considered to be solved when the Agent gets an average score of +30 over 100 consecutive episodes.

**Note:** This project uses a simulator provided by Udacity which is similar but not identical to the `Reacher` environment on the [Unity ML-Agents GitHub page](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher).

## Getting Started

1. Install project dependencies by following the instructions mentioned in the [Installation_Guide.md](Installation_Guide.md).

2. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
   
   1. Version 1: One (1) Agent:
       - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
       - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
       - Windows (32-bit): [click here](hhttps://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
       - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)
     
  
   2. Version 2: Twenty (20) Agents: (**Note that the project has been implemented using Version 1**)
       - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
       - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
       - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
       - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)

    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (For AWS) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux_NoVis.zip) (version 1) or [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux_NoVis.zip) (version 2) to obtain the "headless" version of the environment. You will not be able to watch the agent without enabling a virtual screen, but you will be able to train the agent. (To watch the agent, you should follow the instructions to [enable a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md), and then download the environment for the Linux operating system above.)

3. Place the file in `/data` directory, and unzip the file.

## Instructions

Following are the steps to train your agent:

1. Clone this github repository:
   ```bash
    git clone https://github.com/anubhavshrimal/Continuous_Control_Udacity_DRLND_P2.git
    cd Continuous_Control_Udacity_DRLND_P2/
   ```
2. Activate the conda environment where you installed the dependencies and open jupyter notebooks. 
   ```bash
    conda activate drlnd
    jupyter notebook
   ```
3. Open `Continuous_Control.ipynb` on your browser and run all the cells of the notebook.

## Files

* `checkpoint_actor.pth` and `checkpoint_critic.pth` are the pre-trained model weights for the Agent, which can be used to further train the Agent or to see how the trained agent performs over the environment
* `Continuous_Control.ipynb` is the ipython notebook which trains the Agent in the reacher environment
* `ddpg` folder contains the implementation for the `Agent` and the `actor`, `critic` models.

## Algorithm

The algorithm and hyper-parameter details are mentioned in [Report.md](./Report.md).