# CPSC_481_Final_Project

## Problem

I wanted to use reinforcement learning, to create an AI that can increasingly get better at beating the classic Snake Game.

## Approach

I used reinforcment learning, along with deep reinfocement learning, to create an AI that can help impove its score for the Snake Game.

In Reinforcement learning, there are two main components, the environment (the snake game) and the agent (the snake / deep neural network that controls the snake's action).

I created three modules for this project, the environment (snake game), the model (reinforcement model for move prediction), and the agent (the connector between the environment and model)

So, every time the agent performs an action, the environment gives a reward to the agent, which can be positive (snake eats the food) or negative (snake hits a wall and loses).

Deep reinforcement learning combines the ideas of reinformcent learning with deep neural networks.
The Neural network learns the “Q Function”, which takes an input the current environment state and outputs a vector contain the expected rewards for each possible action. 

The agent can then pick the action that maximizes the Q function. So based on this action the game then updates the environment to a new state, and assigns a reward (for example: +10 for eating the food, -10 for hitting a wall)

There are going to be 11 values for the state. (Boolean)

[Danger straight, danger right, danger left,
Direction left, direction right, direction up, direction down,
Food left, food right, food up, food down]

After getting the states, the agent would pass this to the model and get the next move to perform
After executing the next state, calculate the reward, which are: eat food +10, game over -10, else 0.
Then we update the Q value and train the model.

I used a deep neural network layer with an input layer size of 11 and one dense layer with 256 neurons and an output of 3 neurons.
How the model works:

The game starts, and the q-value is randomly initialized.
The system gets the current state.
Based on the state, it executes an action, randomly based on its neural network. During the beginning, the system will choose random actions, but as it learns, it will rely more on the neural network. [you will see in demo]
When the ai chooses and performs the action, the environment gives a reward, then the agent reaches the new state and updates its q-value.

## Results

<p align="center">
<img src="https://github.com/le11evan/CPSC_481_Final_Project/blob/main/graph results.png" width="250" height="250" />
 </p>
 
<p align="center">
<img src="https://github.com/le11evan/CPSC_481_Final_Project/blob/main/results.png" width="250" height="250" />
 </p>

<p>
<img src="https://github.com/vedantgoswami/SnakeGameAI/blob/main/Images/new.gif" width=380px height=250px align='left'>
<img src="https://github.com/vedantgoswami/SnakeGameAI/blob/main/Images/Animation.gif" width=380px height=250px align='right'>
<br><br><br><br><br><br><br><br><br><br><br>
<p style="font-size:25px">
<pre>              <b> Intial Results</b>                                                <b>After about 80<sup>th</sup> Games</b></pre>
</p>
