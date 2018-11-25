[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135623-e770e354-7d12-11e8-998d-29fc74429ca2.gif "Trained Agent"

# Project 3: Collaboration and Competition

In this environment, a double-jointed arm can move to target locations.
- **Reward:** +0.1 for each step that the agent's hand is in the goal location.
- **Goal:** Agent should maintain its hand position at the target location for as many timesteps as possible.
- **Observation Space:** 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm.
- **Action Space:** Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

### Introduction

For this project, we worked with the [Tennis](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#tennis) environment. View the full report [here](https://github.com/mrbarbasa/drlnd-projects/blob/master/p3_collab-compet/Report.md).

![Trained Agent][image1]

In this environment, two agents control rackets to bounce a ball over a net.
- **Positive Rewards:** +0.1 if an agent hits the ball over the net.
- **Negative Rewards:** -0.01 if an agent lets a ball hit the ground or hits the ball out of bounds.
- **Goal:** Each agent should keep the ball in play for as long as possible.
- **Observation Space:** 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation.
- **Action Space:** Two continuous actions are available: 1) movement toward (or away from) the net, and 2) jumping. 

#### Solving the Environment

An episode ends when the ball is out of play (when it's hit out of bounds or within bounds into the ground). Agents must get an average score of +0.5 over 100 consecutive episodes. This is done by summing up the rewards that each agent received per timestep, yielding two separate sums at the end of each episode; the maximum of these two scores is the score for the episode.

The environment is considered solved when the average over 100 episodes of these scores is at least +0.5.

### Getting Started

1. Download and install Anaconda or Miniconda: https://conda.io/docs/user-guide/install/download.html.
1. In the terminal, create and activate a new environment with Python 3.6.
    - __Linux__ or __Mac__: 
    ```bash
    conda create --name compete python=3.6
    source activate compete
    ```
    - __Windows__: 
    ```bash
    conda create --name compete python=3.6 
    activate compete
    ```
1. Navigate to the `python/` folder of this repository and install several dependencies by running `pip install .`.
1. Run `python -m ipykernel install --user --name compete --display-name "compete"`.

1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux_NoVis.zip) to obtain the "headless" version of the environment.  You will **not** be able to watch the agent without enabling a virtual screen, but you will be able to train the agent.  (_To watch the agent, you should follow the instructions to [enable a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md), and then download the environment for the **Linux** operating system above._)

1. Place the file in this repository's `p3_collab-compet/` folder, and unzip (or decompress) the file.
1. In the terminal, run `jupyter notebook` and open the `Tennis.ipynb` file.
1. Select `Kernel > Change kernel > compete` to change the kernel.

### Instructions

Run or view the output of each cell in `Tennis.ipynb`. You would have to modify the file `ddpg_agent.py` to get similar results (based on the comments for each trial in part 4 of the notebook). I have left `model.py` and `ddpg_agent.py` to their optimal settings after all the trials I've run.
