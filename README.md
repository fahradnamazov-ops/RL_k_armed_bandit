# K-Armed Bandit — Reinforcement Learning Practice

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![NumPy](https://img.shields.io/badge/NumPy-1.21%2B-orange)
![License](https://img.shields.io/badge/License-MIT-green)

This repository contains a from-scratch implementation of the **K-Armed Bandit** problem, covering the core exploration-exploitation strategies from Chapter 2 of *Reinforcement Learning: An Introduction* (Sutton & Barto).

Completed as part of the **Deep Reinforcement Learning** course at **Eötvös Loránd University (ELTE)**, 2025–2026.

---

## 📖 What is the K-Armed Bandit Problem?

Imagine you're in a casino facing `k` slot machines (bandits), each with a different (unknown) reward distribution. At every step you must choose which machine to pull. Your goal is to **maximize total reward** over time.

This requires balancing two competing objectives:
- **Exploitation** — pull the machine you currently believe is best
- **Exploration** — try other machines to improve your estimates

---

## 🧠 Strategies Implemented

| Strategy | Description |
|---|---|
| **ε-Greedy** | Explores randomly with probability ε, otherwise exploits the best known action |
| **UCB (Upper Confidence Bound)** | Balances exploration by adding an uncertainty bonus to each action's value estimate |
| **Gradient Bandit** | Learns action preferences via policy gradient updates using a softmax distribution |

All strategies support:
- Sample-average updates (`step_size=None`)
- Constant step-size updates (`step_size=α`)
- Optimistic initialization (`initial > 0`)

---

## 🌍 Environments

| Environment | Description |
|---|---|
| `KArmedBandit` | Stationary — true action values are fixed throughout each run |
| `NonStationaryKArmedBandit` | Non-stationary — true action values drift over time via random walk |

---

## 📊 Results

### Epsilon Sensitivity (Stationary)
![Epsilon Sensitivity](results/epsilon_sensitivity.png)

### UCB Exploration Coefficient
![UCB](results/ucb.png)

### Gradient Bandit with/without Baseline
![Gradient Baseline](results/gradient_baseline.png)

### Comprehensive Comparison
![Comprehensive](results/comprehensive.png)

### Non-Stationary Environment
![Non-Stationary](results/nonstationary.png)

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/fahradnamazov-ops/RL_k_armed_bandit.git
cd RL_k_armed_bandit
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the notebook
Open `k_armed_bandit.ipynb` in Jupyter or [Google Colab](https://colab.research.google.com/).

---

## 📁 Project Structure

```
RL_k_armed_bandit/
│
├── k_armed_bandit.ipynb   # Main notebook with all implementations
├── requirements.txt        # Python dependencies
├── results/                # Output plots from simulation runs
│   ├── epsilon_sensitivity.png
│   ├── ucb.png
│   ├── gradient_baseline.png
│   ├── comprehensive.png
│   └── nonstationary.png
├── .gitignore
└── README.md
```

---

## 📚 Reference

Sutton, R. S., & Barto, A. G. (2018). *Reinforcement Learning: An Introduction* (2nd ed.). MIT Press.  
Available free at: [http://incompleteideas.net/book/the-book.html](http://incompleteideas.net/book/the-book.html)

---

## 👤 Author

**Fahrad Namazov**  
MSc Artificial Intelligence — Eötvös Loránd University (ELTE)  
[GitHub](https://github.com/fahradnamazov-ops)
