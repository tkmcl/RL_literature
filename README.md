# RL_literature

## Approaches

#### Policy Gradient
1. Pong from Pixels http://karpathy.github.io/2016/05/31/rl/  



## Applications

1. Resources Management in Computer Clusters (use RL to automatically learn to allocate and schedule computer resources to waiting jobs, with the objective to minimize the average job slowdown.)  https://people.csail.mit.edu/alizadeh/papers/deeprm-hotnets16.pdf

2. Traffic Light Control (a traffic light controller to solve the congestion problem.) http://web.eecs.utk.edu/~itamar/Papers/IET_ITS_2010.pdf

3. Chemistry (Combined with LSTM to model the policy function, the RL agent optimized the chemical reaction with the Markov decision process (MDP) characterized by {S, A, P, R}, where S was the set of experimental conditions (like temperature, pH, etc), A was the set all possible actions that can change the experimental conditions, P was the transition probability from current experiment condition to the next condition, and R was the reward which is a function of the state. https://github.com/lightingghost/chemopt

## What do you need to know before applying RL to your problem

Deep Reinforcement Learning Doesn't Work Yet
https://www.alexirpan.com/2018/02/14/rl-hard.html

There are several things needed before RL can be applied:

* Understanding your problem: You do not necessarily need to use RL in your problem and sometimes you just cannot use RL. You may want to check if your problem has some of the following characteristics before deciding to use RL: a) trial-and-error (can be learned to do better by receiving feedback from the environment); b)delayed rewards; c)can be modeled as MDP; d)your problem is a control problem.
* A simulated environment: Lots of iterations are needed before a RL algorithm to work. I am sure that you don’t want to see a RL agent trying different things in a self-driving car on a highway, right? Therefore, a simulated environment that can correctly reflect the real world is needed.
* MDP: You world need to formulate your problem into a MDP. You need to design the state space, action space, reward function and so on. Your agent will do what it is rewarded to do under the constraints. You may not get the results you want if you design the things differently.
* Algorithms: There are different RL algorithms you can choose and questions to ask yourself. You want to directly find out the policy or you want to learn the value function? You want to go model-free or model-based? Do you need to combine other kinds of deep neural network or methods to solve your problems?
