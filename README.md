# Reinforcement Learning - Car Expedition Environment

This project implements a Reinforcement Learning environment for a car expedition game using Python and Gymnasium. The environment simulates a 4x4 grid world where a car must navigate through various obstacles and collect rewards.

## Features

- 4x4 Grid World Environment
- Deterministic and Stochastic Modes
- Multiple Object Types:
  - Car (Agent)
  - Fuel Stations
  - Rocks (Obstacles)
  - Hotel (End Point)
- Reward/Penalty System
- Visualization using Matplotlib

## Requirements

- Python 3.x
- Gymnasium
- Matplotlib
- NumPy
- OpenCV (cv2)
- Google Colab (optional for visualization)

## Installation

Install the required packages using pip:

```bash
pip install gymnasium matplotlib numpy opencv-python
```

## How to Run

1. Create an instance of the ExpeditionEnvironment:
```python
env = ExpeditionEnvironment(environment_type='deterministic')
```

2. Reset the environment to start a new episode:
```python
env.reset()
```

3. Take actions using the step function:
```python
action = 0  # 0: Right, 1: Left, 2: Up, 3: Down
observation, reward, terminated, truncated, info = env.step(action)
```

## Environment Details

- **State Space**: Discrete 4x4 grid (16 possible states)
- **Action Space**: 4 discrete actions (Right, Left, Up, Down)
- **Rewards**: 
  - Positive rewards for collecting fuel
  - Penalties for hitting rocks
  - Final reward for reaching hotel

## Project Structure

- [ReinforcementLearning_4x4Grid.ipynb](ReinforcementLearning_4x4Grid.ipynb): Main implementation file
- [README.md](README.md): Project documentation

## Visualization

The environment includes visualization capabilities that show:
- Car position
- Fuel stations
- Rocks
- Hotel
- Current action taken
- Reward information

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request
