[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"

# Project 1: Navigation

### Project Details

For this project, the agent is trained to navigate (and collect bananas!) in a large, square world.  

![Trained Agent][image1]

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of the agent is to collect as many yellow bananas as possible while avoiding blue bananas.  

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction.  Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, the agent must get an average score of +13 over 100 consecutive episodes.

### Getting Started

1. Download and install Anaconda or Miniconda: https://conda.io/docs/user-guide/install/download.html.
1. In the terminal, create and activate a new environment with Python 3.6.
	- __Linux__ or __Mac__: 
	```bash
	conda create --name navigation python=3.6
	source activate navigation
	```
	- __Windows__: 
	```bash
	conda create --name navigation python=3.6 
	activate navigation
	```
1. Install Unity ML-Agents by following the instructions [here](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Installation.md).
    - After following the instructions, check to make sure that `from unityagents import UnityEnvironment` in the Python REPL works without error.
    - If it throws an error, you will need to run `pip install unityagents` in the terminal.
1. Run `pip install -r requirements.txt`.
1. Run `python -m ipykernel install --user --name navigation --display-name "navigation"`.

1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux_NoVis.zip) to obtain the environment.

1. Place the file in this repository's `p1_navigation/` folder, and unzip (or decompress) the file.
1. In the terminal, run `jupyter notebook` and open the `Navigation.ipynb` file.
1. Select `Kernel > Change kernel > navigation` to change the kernel.

### Instructions

Run or view the output of each cell in `Navigation.ipynb`. You would have to modify the files in `model.py` and `dqn_agent.py` to get similar results (based on the comments for each trial in part 4 of the notebook). I have left `model.py` and `dqn_agent.py` to their optimal settings after all the trials I've run.
