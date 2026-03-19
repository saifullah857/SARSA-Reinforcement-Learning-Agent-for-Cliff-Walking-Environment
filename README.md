
# 🧠 SARSA vs. Q-Learning: Cliff Walking RL Agent

[![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Gymnasium](https://img.shields.io/badge/Environment-Gymnasium-orange)](https://gymnasium.farama.org/)
[![RL](https://img.shields.io/badge/Reinforcement_Learning-Temporal_Difference-green)](https://en.wikipedia.org/wiki/Temporal_difference_learning)
[![NumPy](https://img.shields.io/badge/Library-NumPy-blue?logo=numpy)](https://numpy.org/)
[![License](https://img.shields.io/badge/License-MIT-red)](LICENSE)

An implementation and comparative analysis of **On-Policy (SARSA)** and **Off-Policy (Q-Learning)** Reinforcement Learning algorithms within the Gymnasium "Cliff Walking" environment.

---

## 📌 Project Overview

This repository demonstrates how an agent learns to navigate a grid-world while balancing the tradeoff between path efficiency and safety. The **Cliff Walking** environment is a classic reinforcement learning problem where the agent must reach a goal state without falling off a cliff ($reward = -100$).

### 🚀 Objectives
* Implement **Temporal Difference (TD)** learning from scratch.
* Compare convergence and behavioral differences between **SARSA** and **Q-Learning**.
* Visualize the impact of **$\epsilon$-Greedy exploration** on path selection.

---

## 🌍 Environment Dynamics

The agent operates in a **4 × 12 grid**:
* **States:** 48 discrete grid cells.
* **Actions:** `0: Up`, `1: Right`, `2: Down`, `3: Left`.
* **Rewards:** -1 per step, -100 for falling off the cliff.
* **Goal:** Reach the bottom-right cell with maximum cumulative reward.

---

## 🧮 Theoretical Background

### 1. SARSA (On-Policy)
SARSA updates its Q-values based on the action actually taken by the current policy:
$$Q(s,a) \leftarrow Q(s,a) + \alpha [r + \gamma Q(s',a') - Q(s,a)]$$
*SARSA accounts for the next action $a'$, learning a **safer** path to avoid the cliff during exploration.*

### 2. Q-Learning (Off-Policy)
Q-Learning updates based on the maximum possible reward of the next state, regardless of the policy's next action:
$$Q(s,a) \leftarrow Q(s,a) + \alpha [r + \gamma \max_{a'} Q(s',a') - Q(s,a)]$$
*This leads the agent to learn the **optimal** (shortest) path, though it is more "aggressive" during training.*

---

## 📂 Project Architecture

```text
sarsa-qlearning-cliffwalking/
├── 📂 notebooks/
│   ├── SARSA_Code.ipynb      # On-Policy implementation
│   ├── Q-Learning.ipynb      # Off-Policy implementation
│   └── practice-project.ipynb # Experimental sandbox
├── README.md                 # Documentation
└── .gitignore                # Python ignore files

```

---

## 💻 Installation & Usage

### 1. Clone the repository

```bash
git clone https://github.com/saifullah857/sarsa-qlearning-cliffwalking.git
cd sarsa-qlearning-cliffwalking

```

### 2. Install Dependencies

```bash
pip install gymnasium[toy-text] numpy jupyter

```

### 3. Run Notebooks

```bash
jupyter notebook

```

---

## 🎯 Key Insights

* **Path Choice:** **SARSA** takes the "scenic route" (one row away from the cliff) to avoid falling due to random $\epsilon$ moves. **Q-Learning** hugs the cliff edge to find the shortest mathematical path.
* **Convergence:** Q-Learning generally converges to the optimal policy faster, but experiences lower cumulative rewards during training due to frequent "cliff falls."

---

## 👨‍💻 Author

**Saif Ullah**

