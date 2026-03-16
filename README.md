# 🧠 SARSA & Q-Learning Reinforcement Learning Agent for Cliff Walking

<p align="center">

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white)
![Reinforcement Learning](https://img.shields.io/badge/Machine%20Learning-Reinforcement%20Learning-green?logo=scikitlearn&logoColor=white)
![Gymnasium](https://img.shields.io/badge/Environment-Gymnasium-orange)
![NumPy](https://img.shields.io/badge/Library-NumPy-blue?logo=numpy)
![Jupyter Notebook](https://img.shields.io/badge/Notebook-Jupyter-orange?logo=jupyter)
![License](https://img.shields.io/badge/License-MIT-red)

</p>

---

# 📌 Overview

This project demonstrates **SARSA (On-Policy)** and **Q-Learning (Off-Policy)** algorithms in **Reinforcement Learning**.  

The agent is trained in the **Cliff Walking environment** using **Gymnasium**, learning optimal policies to **navigate safely from start to goal** while avoiding the cliff, which gives a large negative reward.

> 🚀 **Goal:** Safely reach the goal while learning the optimal policy.

---

# ✨ Key Features

- 🟢 **SARSA (On-Policy)** & **Q-Learning (Off-Policy)** implementation  
- 🟢 **Q-Table based learning**  
- 🟢 **Epsilon-Greedy exploration** strategy  
- 🟢 Safe navigation in **Cliff Walking environment**  
- 🟢 Reward maximization and policy optimization  

---

# 🌍 Environment Details

| Feature      | Description                                          |
| ------------ | ---------------------------------------------------- |
| Environment  | CliffWalking-v1                                      |
| Grid Size    | 4 × 12                                               |
| State Space  | 48 states                                            |
| Action Space | 4 actions (Up, Down, Left, Right)                   |
| Goal         | Reach destination without falling into the cliff    |

> ⚠ **Warning:** Falling into the cliff gives a **large negative reward** and resets the agent to the start.

---

# 🧮 Algorithms

### 1️⃣ SARSA (On-Policy Learning)

The SARSA update rule:

\[
Q(s,a) = Q(s,a) + \alpha [r + \gamma Q(s',a') - Q(s,a)]
\]

**Where:**  
- **s** → Current state  
- **a** → Current action  
- **r** → Reward received  
- **s'** → Next state  
- **a'** → Next action  
- **α (alpha)** → Learning rate  
- **γ (gamma)** → Discount factor  

---

### 2️⃣ Q-Learning (Off-Policy Learning)

Q-Learning update rule:

\[
Q(s,a) \leftarrow Q(s,a) + \alpha \left[r + \gamma \max_{a'} Q(s',a') - Q(s,a)\right]
\]

> Instead of using the next action from the policy, Q-Learning uses the **maximum possible future reward**, making it **Off-Policy**.

---

### 🔍 SARSA vs Q-Learning

| Feature               | SARSA               | Q-Learning           |
|-----------------------|-------------------|-------------------|
| Learning Type         | On-Policy          | Off-Policy         |
| Update Uses           | Next action from policy | Best possible action |
| Risk Behavior         | More cautious      | More aggressive   |
| Cliff Walking Result  | Safer path         | Shorter but riskier path |

---

# ⚙️ Training Parameters

| Parameter            | SARSA | Q-Learning |
| -------------------- | ----- | ---------- |
| Episodes             | 500   | 500        |
| Learning Rate (α)    | 0.5   | 0.5        |
| Discount Factor (γ)  | 0.99  | 0.99       |
| Exploration Rate (ε) | 0.1   | 0.1        |

> 📊 **Tip:** You can tune α, γ, and ε to see how the agent's behavior changes.

---

# 📂 Project Structure
sarsa-qlearning-cliffwalking
│
├── SARSA_Code.ipynb
├── Q-Learning.ipynb
├── practice-project.ipynb
├── README.md

---

# 💻 Installation

```bash
pip install gymnasium
pip install "gymnasium[toy-text]"
pip install numpy

▶️ How to Run

1️⃣ Clone the repository
git clone https://github.com/saifullah857/sarsa-qlearning-cliffwalking.git
2️⃣ Navigate to the project folder

cd sarsa-qlearning-cliffwalking

3️⃣ Run the notebook

jupyter notebook

Open SARSA_Code.ipynb and Q-Learning.ipynb to train and visualize the agents.

🎯 Learning Outcomes

✅ Fundamentals of Reinforcement Learning

✅ Implementation of SARSA and Q-Learning

✅ Policy learning using Q-Tables

✅ Exploration vs Exploitation strategies

✅ Interaction with Gymnasium environments

🚀 Future Improvements

📈 Add reward and training visualization graphs

🤖 Implement Deep Q-Network (DQN)

⚡ Test different exploration strategies

📊 Compare SARSA vs Q-Learning performance quantitatively

🛠 Technologies Used

Python

Reinforcement Learning

Gymnasium

NumPy

Jupyter Notebook

👨‍💻 Author

Saif Ullah