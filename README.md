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
- [`reset()`](https://gymnasium.farama.org/api/env/#gymnasium.Env.reset): 
