I built an AI that learns to play Nim using Q-learning.

### 1. Q-Value Retrieval

I made a function to get stored Q-values:
- Convert state list to tuple for dictionary keys
- Return 0 if no Q-value exists yet

### 2. Q-Value Updates

I implemented the Q-learning update formula:
- Calculate new value = current reward + future rewards
- Update Q-value using learning rate (alpha)
- Store updated values in the Q-table

### 3. Best Reward Finder

I created a function to find the best possible future reward:
- Get all available actions for a state
- Find action with highest Q-value
- Return 0 if no actions possible

### 4. Action Selection

I built an epsilon-greedy action selector:
- Random action with probability epsilon (exploration)
- Best Q-value action otherwise (exploitation)
- Random choice when multiple actions tie for best

## Key Points

- The AI starts with no knowledge but learns from games
- Negative rewards for losing, positive for winning
- Self-play training builds a strong strategy
- Actions that lead to wins get higher Q-values
- The model balances exploration vs. exploitation