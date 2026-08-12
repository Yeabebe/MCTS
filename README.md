# Monte Carlo Tree Search (MCTS) for Tic-Tac-Toe

A clean, educational, and research-oriented implementation of **Pure Monte Carlo Tree Search (MCTS)** applied to the Tic-Tac-Toe environment. This project explores the core MCTS algorithm, evaluates its performance, and implements practical optimizations such as **Tree Reuse** inspired by modern game-playing systems like AlphaGo and AlphaZero.

---

## Project Overview

This project was developed to study decision-making algorithms and Monte Carlo Tree Search in depth. The implementation follows the classical four-stage MCTS pipeline without using any neural networks.

The notebook includes:

- Pure Monte Carlo Tree Search
- UCT (Upper Confidence Bound applied to Trees)
- Random rollout simulations
- Negamax-style backpropagation
- Tree Reuse optimization
- Action masking demonstration
- Performance evaluation
- Simulation budget analysis
- Runtime analysis
- Search tree visualization
- Root visit heatmap
- Experimental comparison between baseline and optimized MCTS

---

## Features

### Pure MCTS

Implements the complete Monte Carlo Tree Search algorithm:

- Selection
- Expansion
- Simulation (Random Rollout)
- Backpropagation

---

### UCT Selection Policy

Uses the classical UCT formula

\[
UCT = Q(s,a) + c\sqrt{\frac{\ln N(s)}{N(s,a)}}
\]

to balance exploration and exploitation.

---

### Negamax Backpropagation

The implementation follows the negamax formulation for two-player zero-sum games by alternating the propagated reward at each level of the search tree.

---

### Tree Reuse

Instead of rebuilding the search tree after every move, the explored subtree corresponding to the chosen action becomes the new root.

Benefits include:

- Reduced computation
- Preserved search statistics
- Faster future searches
- More efficient planning

---

### Action Masking

Demonstrates how legal actions can be represented using binary masks.

Although pure MCTS does not require action masking, this concept is included because it is commonly used in AlphaZero-style policy networks.

---

### Search Visualization

The notebook visualizes the internal search process through:

- MCTS search tree
- Root visit heatmap
- Simulation budget analysis
- Runtime analysis
- Performance comparison charts

---

## Project Structure

```text
MCTS_TicTacToe.ipynb

├── Imports
├── TicTacToe Environment
├── MCTS Node
├── UCT Selection
├── Pure MCTS
├── Random Agent
├── Evaluation Functions
├── Action Masking
├── Tree Reuse
├── Simulation Budget Experiments
├── Performance Evaluation
├── Visualizations
└── Save Results
```

---

## MCTS Workflow

```text
                Root

                  │
                  ▼

            1. Selection
                  │
                  ▼

            2. Expansion
                  │
                  ▼

        3. Random Rollout
                  │
                  ▼

         4. Backpropagation
                  │
                  ▼

        Repeat for N Simulations
```

---

## Experimental Evaluation

The notebook evaluates the algorithm using several experiments.

### Baseline

- Pure MCTS vs Random Agent

### Optimization

- Pure MCTS
- MCTS with Tree Reuse

### Simulation Budget

Different search budgets are evaluated:

- 25 simulations
- 50 simulations
- 100 simulations
- 250 simulations
- 500 simulations
- 1000 simulations

---

## Visualizations

The notebook includes several visualizations for better understanding of MCTS.

- Search Tree Visualization
<img width="950" height="658" alt="image" src="https://github.com/user-attachments/assets/6a43d7d6-a6d0-4b06-92ed-6ce53d47c881" />


- Root Visit Heatmap
<img width="424" height="405" alt="image" src="https://github.com/user-attachments/assets/10f95e23-8ae5-45e5-91ec-ac7eb23c6e5c" />


- Win Rate vs Simulation Budget
<img width="764" height="475" alt="image" src="https://github.com/user-attachments/assets/c7b0b8ba-ac17-4864-952b-6398c9d9d229" />


- Runtime vs Simulation Budget
<img width="686" height="475" alt="image" src="https://github.com/user-attachments/assets/aa1a9dc1-497e-455f-84aa-9df9ef70d09e" />


- Baseline vs Optimized Performance Comparison
<img width="686" height="591" alt="image" src="https://github.com/user-attachments/assets/559df30d-ea14-4ec9-8c7f-3ce528577522" />



---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- NetworkX

---

## Repository Contents

```text
.
├── MCTS_TicTacToe.ipynb
├── mcts_simulation_budget_results.csv
├── mcts_final_comparison.csv
└── README.md
```

---

## Learning Objectives

This project demonstrates:

- Monte Carlo Tree Search
- Online search algorithms
- Multi-Armed Bandit problem
- UCT exploration strategy
- Negamax search
- Random rollouts
- Tree reuse optimization
- Experimental evaluation of search algorithms

---

## Relation to AlphaGo / AlphaZero

This implementation is a **Pure MCTS** algorithm.

Unlike AlphaGo or AlphaZero, it **does not use**:

- Neural networks
- Policy networks
- Value networks
- PUCT
- Self-play training

Instead, it serves as a baseline implementation upon which AlphaZero-style methods can be understood.

---

## Future Improvements

Possible extensions include:

- Connect Four environment
- Gomoku implementation
- PUCT implementation
- Policy-Value Network integration
- AlphaZero-style self-play training
- Parallel MCTS
- Heuristic-guided rollouts
- Transposition tables

---

## References

- Browne, C. et al. (2012). *A Survey of Monte Carlo Tree Search Methods.*
- Kocsis, L. & Szepesvári, C. (2006). *Bandit Based Monte-Carlo Planning.*
- Silver, D. et al. (2016). *Mastering the Game of Go with Deep Neural Networks and Tree Search.*
- Silver, D. et al. (2017). *Mastering Chess and Shogi by Self-Play with a General Reinforcement Learning Algorithm.*

---

## License

This project is intended for educational and research purposes.
