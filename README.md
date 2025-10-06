# Nim AI

This project implements an AI to play the game of **Nim** using **Q-learning**. The AI can learn optimal strategies by playing games against itself and then compete against a human player.

## Overview

The project contains the following main components:

1. **nim.py**:  
   - `Nim` class: Handles gameplay mechanics, including state management, valid moves, and switching players.  
   - `NimAI` class: Implements a Q-learning AI to play Nim. Functions include:
     - `get_q_value`: Retrieves the Q-value for a state/action pair.
     - `update_q_value`: Updates the Q-value using the Q-learning formula.
     - `best_future_reward`: Computes the best possible future reward from a given state.
     - `choose_action`: Selects an action, either greedily or with epsilon-greedy exploration.
   - `train` function: Trains the AI by simulating games against itself.  
   - `play` function: Allows a human to play against the trained AI.  

2. **play.py**: Optional script to test and play against the trained AI.

## Features

- Q-learning AI that learns optimal strategies through self-play.
- Epsilon-greedy action selection to balance exploration and exploitation.
- Supports human-AI gameplay after training.

## Installation

1. Clone this repository:

```bash
git clone https://github.com/your-username/nim-ai.git
cd nim-ai
```
2. (Optional) Create a virtual environment:
```python
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```
3. Install required packages:
```python
pip install -r requirements.txt
```
**Note**: Only standard Python libraries are required (e.g., `random`), so no additional packages are strictly necessary unless you extend functionality.

## Usage
1. Train the AI:
```python
from nim import NimAI, train
ai = train(n=10000)  # Train AI with 10,000 simulated games
```
2. Play against the AI:
```python
from nim import play
play(ai)
```
3. Use the AI in a custom script:
```python
from nim import NimAI, Nim
ai = NimAI()
# Use ai.get_q_value, ai.choose_action, etc.
```
## Requirements
- Python 3.8+ 
- Standard libraries only (`random`, `itertools`, etc.)
- Optional: `numpy` or `pandas` if extending functionality

## License
This project is licensed under the MIT License. See the LICENSE
