# 🧠 SARSA Reinforcement Learning Agent for Cliff Walking

<p align="center">

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python\&logoColor=white)
![Reinforcement Learning](https://img.shields.io/badge/Machine%20Learning-Reinforcement%20Learning-green?logo=scikitlearn\&logoColor=white)
![Gymnasium](https://img.shields.io/badge/Environment-Gymnasium-orange)
![NumPy](https://img.shields.io/badge/Library-NumPy-blue?logo=numpy)
![Jupyter Notebook](https://img.shields.io/badge/Notebook-Jupyter-orange?logo=jupyter)


</p>

---

# 📌 Overview

This project demonstrates the implementation of the **SARSA (State–Action–Reward–State–Action)** algorithm in **Reinforcement Learning**.

The agent is trained in the **Cliff Walking environment** using the **Gymnasium library**, where it learns an optimal policy through continuous interaction with the environment.

The main objective of the agent is to **navigate safely from the start state to the goal state while avoiding the cliff**, which results in a large negative reward.

---

# ✨ Key Features

✔ Implementation of **SARSA On-Policy Reinforcement Learning algorithm**
✔ Training an agent in the **Cliff Walking grid environment**
✔ **Q-Table based learning** approach
✔ **Epsilon-Greedy exploration strategy**
✔ Policy optimization through **reward maximization**

---

# 🌍 Environment Details

| Feature      | Description                                          |
| ------------ | ---------------------------------------------------- |
| Environment  | CliffWalking-v1                                      |
| Grid Size    | 4 × 12                                               |
| State Space  | 48 states                                            |
| Action Space | 4 actions (Up, Down, Left, Right)                    |
| Goal         | Reach the destination without falling into the cliff |

⚠ If the agent falls into the **cliff region**, it receives a **large negative reward** and returns to the **starting position**.

---

# 🧮 Algorithm

The SARSA update rule is:

[
Q(s,a) = Q(s,a) + \alpha [r + \gamma Q(s',a') - Q(s,a)]
]

### Where

* **s** → Current state
* **a** → Current action
* **r** → Reward received
* **s'** → Next state
* **a'** → Next action
* **α (alpha)** → Learning rate
* **γ (gamma)** → Discount factor

---

# ⚙️ Training Parameters

| Parameter            | Value |
| -------------------- | ----- |
| Episodes             | 500   |
| Learning Rate (α)    | 0.5   |
| Discount Factor (γ)  | 0.99  |
| Exploration Rate (ε) | 0.1   |

---

# 📂 Project Structure

```
sarsa-cliffwalking-reinforcement-learning
│
├── sarsa_cliffwalking.ipynb
├── README.md
```

---

# 💻 Installation

Install the required dependencies:

```bash
pip install gymnasium
pip install "gymnasium[toy-text]"
pip install numpy
```

---

# ▶️ How to Run

### 1️⃣ Clone the repository

```bash
git clone https://github.com/yourusername/sarsa-cliffwalking-reinforcement-learning.git
```

### 2️⃣ Navigate to the project folder

```bash
cd sarsa-cliffwalking-reinforcement-learning
```

### 3️⃣ Run the notebook

```bash
jupyter notebook
```

Open **sarsa_cliffwalking.ipynb** and run all cells to train the agent.

---

# 🎯 Learning Outcomes

This project demonstrates:

📌 Fundamentals of **Reinforcement Learning**
📌 Implementation of the **SARSA algorithm**
📌 Policy learning using **Q-Tables**
📌 **Exploration vs Exploitation** strategies
📌 Interaction with **Gymnasium RL environments**

---

# 🚀 Future Improvements

Possible extensions for this project:

🔹 Implement **Q-Learning** for comparison
🔹 Add **reward and training visualization graphs**
🔹 Implement **Deep Q-Network (DQN)**
🔹 Improve exploration using **advanced strategies**

---

# 🛠 Technologies Used

* 🐍 Python
* 🤖 Reinforcement Learning
* 🎮 Gymnasium
* 🔢 NumPy
* 📓 Jupyter Notebook



# 👨‍💻 Author

Saif Ullah
