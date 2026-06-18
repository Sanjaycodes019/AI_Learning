# Agentic AI

## What is agentic AI?
- Agentic AI refers to systems that act autonomously in an environment.
- An AI agent perceives input, makes decisions, and takes actions to reach goals.
- Agentic systems are often used in robotics, games, automation, and dialogue agents.

## Agent structure
- **Perception**: observe the environment.
- **Reasoning / planning**: decide what action to take.
- **Action**: execute the chosen behavior.
- **Goal**: what the agent tries to achieve.

## Example: Simple agent loop

```python
state = {'battery': 50, 'location': 'home', 'task': 'deliver'}

while state['battery'] > 0:
    if state['task'] == 'deliver':
        action = 'move to delivery point'
    elif state['battery'] < 20:
        action = 'return to base'
    else:
        action = 'wait'

    print(f"Agent action: {action}")

    if action == 'move to delivery point':
        state['location'] = 'delivery point'
        state['battery'] -= 10
    elif action == 'return to base':
        state['location'] = 'base'
        state['battery'] -= 5
    else:
        state['battery'] -= 1

    if state['location'] == 'delivery point':
        state['task'] = 'complete'
```

This example shows a basic decision loop where an agent chooses actions based on state.

## What to learn next
- Reinforcement learning basics
- Environment, state, actions, and rewards
- Planning and search algorithms
- How agentic AI differs from passive prediction models
