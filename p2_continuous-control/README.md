[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/43851024-320ba930-9aff-11e8-8493-ee547c6af349.gif "Trained Agent"

# Project 2: Continuous Control

### Introduction

For this project, we worked with the [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environment.

![Trained Agent][image1]

In this environment, a double-jointed arm can move to target locations.
- **Reward:** +0.1 for each step that the agent's hand is in the goal location.
- **Goal:** Agent should maintain its hand position at the target location for as many timesteps as possible.
- **Observation Space:** 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm.
- **Action Space:** Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

#### Solving the Environment

There are two separate versions of the Unity environment:
- The first version contains a single agent.
    - Environment Solved: Agent must get an average score of +30 over 100 consecutive episodes.
- The second version contains 20 identical agents, each with its own copy of the environment.
    - Environment Solved: Agents must get an average score of +30 (over 100 consecutive episodes, and over all agents).
    
For this project, we have solved the second version.

### Getting Started

1. Download and install Anaconda or Miniconda: https://conda.io/docs/user-guide/install/download.html.
1. In the terminal, create and activate a new environment with Python 3.6.
    - __Linux__ or __Mac__: 
    ```bash
    conda create --name control python=3.6
    source activate control
    ```
    - __Windows__: 
    ```bash
    conda create --name control python=3.6 
    activate control
    ```
1. Navigate to the `python/` folder of this repository and install several dependencies by running `pip install .`.
1. Run `python -m ipykernel install --user --name control --display-name "control"`.

1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:

    - **_Version 1: One (1) Agent_**
        - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
        - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
        - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
        - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)

    - **_Version 2: Twenty (20) Agents_**
        - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
        - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
        - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
        - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux_NoVis.zip) (version 1) or [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux_NoVis.zip) (version 2) to obtain the "headless" version of the environment.  You will **not** be able to watch the agent without enabling a virtual screen, but you will be able to train the agent.  (_To watch the agent, you should follow the instructions to [enable a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md), and then download the environment for the **Linux** operating system above._)

1. Place the file in this repository's `p2_continuous-control/` folder, and unzip (or decompress) the file.
1. In the terminal, run `jupyter notebook` and open the `Continuous_Control.ipynb` file.
1. Select `Kernel > Change kernel > control` to change the kernel.

### Instructions

Run or view the output of each cell in `Continuous_Control.ipynb`. You would have to modify the files in `model.py` and `ddpg_agent.py` to get similar results (based on the comments for each trial in part 4 of the notebook). I have left `model.py` and `ddpg_agent.py` to their optimal settings after all the trials I've run.
