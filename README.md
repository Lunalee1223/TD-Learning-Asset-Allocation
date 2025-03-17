# Asset Allocation Using Temporal Difference Learning

## Overview
This repository contains the implementation of a **Temporal Difference (TD) Learning-based** investment strategy for **discrete-time asset allocation**. The problem is formulated as a **Markov Decision Process (MDP)**, where an investor allocates wealth between **risky and risk-free assets** over a time horizon of **T=10** periods. The goal is to **learn an optimal investment strategy** that maximizes the expected **CARA (Constant Absolute Risk Aversion) utility of final wealth**.

## Repository Structure
- `p1_2.ipynb` - Jupyter Notebook containing the implementation, training, and evaluation.
- `report.tex` - LaTeX report detailing the methodology and findings.
- `README.md` - Documentation for understanding and running the project.

## Repository Link
This project is hosted on GitHub:
[TD-Learning-Asset-Allocation](https://github.com/Lunalee1223/TD-Learning-Asset-Allocation.git)

## Implementation Details
The implementation consists of:
1. **Asset Environment (`Asset` class)**: Simulates asset allocation, defining the investment process.
2. **TD Learning Algorithm (`td_learning` function)**: Learns optimal Q-values using an epsilon-greedy approach.
3. **Testing Framework**: Includes unit, system, and acceptance tests.

## Dependencies
To run the project, install the following dependencies:
```bash
pip install numpy matplotlib jupyter
```

## Running the Code
1. Clone the repository:
```bash
git clone https://github.com/Lunalee1223/TD-Learning-Asset-Allocation.git
cd TD-Learning-Asset-Allocation
```
2. Open the Jupyter Notebook:
```bash
jupyter notebook p1_2.ipynb
```
3. Run all cells to execute the TD learning algorithm and evaluate the results.

## Testing Strategy
The model is evaluated using five different test cases with varying market conditions:
| Test Case | Parameters (a, b, p, r) | Expected Behavior |
|-----------|----------------|----------------|
| **1. Always High Return** | (0.8, 0.5, 0.4, 0.1) | Full investment in risky asset. |
| **2. Always Low Return** | (0.1, 0.1, 1.0, 0.8) | Full investment in risk-free asset. |
| **3. Equal Expected Return** | (0.6, 0.2, 0.5, 0.4) | Conservative investment due to variance. |
| **4. High Expected Return** | (0.8, 0.2, 0.5, 0.4) | More investment in risky asset. |
| **5. Small Risk Premium** | (0.3, 0.1, 0.4, 0.15) | Early aggressive investment, later conservative. |


