# Reinforcement-Learning---Lunar-Lander

In this lab we will solve a classical problem in optimal control theory: the lunar lander. The
environment is implemented in the OpenGym library3. The goal will be to train a network to make a successful landing on the
moon.\\
Consider figure 1: the goal is to manoeuvre the space ship so that it lands between the two flags.
The landing pad is always at coordinates (0, 0). The coordinates are the first two numbers in the
state vector. Reward for moving from the top of the screen to the landing pad and zero speed
is about 100 ∼ 140 points. If the lander moves away from the landing pad it loses reward. The
episode finishes if the lander crashes or comes to rest, receiving an additional −100 or +100 points.
Each leg with ground contact is +10 points. Firing the main engine is −0.3 points each frame.
Firing the side engine is −0.03 points each frame. To consider the problem solved your policy
should achieve 200 points. Landing outside the landing pad is possible. Fuel is infinite, so an agent
can learn to fly and then land on its first attempt (in reality there is a limit of 1000 steps in each
episode, in order to limit simulation time).
The OpenGym library takes care of handling the environment and the reward signal for you (check
the code we provided for more details), as well as providing the initial state of the environment
(which is random).

![plot](./lunar_lander.png)
