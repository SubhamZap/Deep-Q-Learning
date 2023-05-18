# Deep-Q-Learning

![cartpole](https://github.com/SubhamZap/Deep-Q-Learning/assets/96906297/4826489c-2338-43fa-b3c0-c6b9ecb4b505)

## Task
*The agent can make two actions - move the cart Left or Right, to keep the pole upright.

## Cartpole
- As the agent observes the current state of the environment, it decides an action for it.
- In response to an action, the environment transitions to a new state.
- For each action taken, the agent is rewarded that represent the consequence of the action.
- In this task, the reward is +1 for every incremental timestamp and the environment terminates, if the task is unsuccessful.

Let's understand the various terminology used:
- [`step()`](https://gymnasium.farama.org/api/env/#gymnasium.Env.step): One step(timestamp) can be defined as the duration in which the agent takes actions to keep the cartpole upright till it is unsuccessful.
```bash
>>> import gymnasium as gym
>>> import numpy as np
>>> envs = gym.vector.make("CartPole-v1", num_envs=3)
>>> _ = envs.reset(seed=42)
>>> actions = np.array([1, 0, 1])
>>> observations, rewards, termination, truncation, infos = envs.step(actions)
>>> observations
array([[ 0.02727336,  0.18847767,  0.03625453, -0.26141977],
       [ 0.01431748, -0.24002443, -0.04731862,  0.3110827 ],
       [-0.03822722,  0.1710671 , -0.00848456, -0.2487226 ]],
      dtype=float32)
>>> rewards
array([1., 1., 1.])
>>> termination
array([False, False, False])
>>> termination
array([False, False, False])
>>> infos
{}
```
- [`reset()`](https://gymnasium.farama.org/api/env/#gymnasium.Env.reset): This function is called after the completion of a timestamp, so that the environment can be returned to initial state.
- [`render()`](https://gymnasium.farama.org/api/env/#gymnasium.Env.render): Renders the environments to help visualise what the agent see, examples modes are “human”, “rgb_array”, “ansi” for text.
