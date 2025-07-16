# 🎰 Multi-Armed Bandit Term Project

This project investigates the **Multi-Armed Bandit (MAB)** problem and evaluates various strategies to balance the trade-off between **exploration and exploitation**. It simulates both stationary and non-stationary environments, enhancing classical algorithms for improved adaptability.

---

## 🧩 1. Problem Definition

The MAB problem models sequential decision-making under uncertainty, where an agent must choose among multiple options (bandits) with stochastic rewards.  
The challenge:  
> Maximize total reward by balancing **exploitation** of known good options vs. **exploration** of less-tried ones.

Implemented strategies:
- **ε-Greedy** (static and adaptive)
- **UCB (Upper Confidence Bound)**
- **Thompson Sampling**
- Enhanced versions of the above (smart reward conditions, meta-agents)

---

## 🔍 2. Research Background

- **Thompson Sampling** is a Bayesian approach that samples from posterior distributions and chooses actions accordingly.
- Compared to ε-Greedy (fixed randomness), Thompson Sampling dynamically adapts to feedback.
- Widely used in **online learning**, **advertising**, **recommendation engines**, and **healthcare optimization**.

> “Thompson Sampling achieves low regret while being lightweight and scalable.” — *StatQuest, DeepMind*

📚 Key References:
- Shipra Agrawal & Navin Goyal (2012)
- DeepMind Bandit Learning (2021)
- Sutton & Barto (2018)
- Lilian Weng's Blog on MABs

---

## ⚙️ 3. Environment and Libraries

- **Environment:** Python 3.11, Jupyter Notebook  
- **Libraries Used:** `numpy`, `matplotlib`, `random`, `tqdm`

---

## 🚀 4. Implemented Methods

### ✅ Enhanced Algorithms:
- **Adaptive ε-Greedy:** `ε(t) = 1 / √t` for dynamic exploration
- **Smart Thompson Sampling:** Rewards counted as success only if they exceed current expectations
- **Strategy Switching Agent:** Dynamically selects best strategy based on recent performance

### 🌍 Environment:
- **Non-stationary bandits:** Mean rewards shift every 500 steps
- Tests both **static** and **changing** reward distributions

---

## 🧪 5. Experiments

- **Bandits:** 5 bandits with randomized mean rewards  
- **Steps:** 5000 actions per strategy  
- **Evaluation Metrics:** Total reward, cumulative regret, adaptability

### 🧠 Strategies Compared:
1. ε-Greedy (Static)
2. Adaptive ε-Greedy
3. UCB
4. Thompson Sampling
5. Smart Thompson Sampling
6. Strategy Switching Meta-Agent

### 📊 Key Findings:

| Strategy                    | Approx. Total Reward |
|-----------------------------|----------------------|
| ε-Greedy (static)           | 7200+                |
| Adaptive ε-Greedy           | 7900+                |
| UCB                         | 7800+                |
| Thompson Sampling           | 8400+                |
| Smart Thompson Sampling     | 8500+                |
| Strategy Switching Agent    | 8600+                |

- ✅ **Thompson Sampling** shows superior adaptability and convergence
- ✅ **Smart strategies** better handle dynamic shifts
- ✅ **Meta-agent switching** generalizes well across scenarios

---

## 🧠 6. Conclusion

This project highlights:
- Thompson Sampling’s robust, Bayesian approach
- The benefit of adaptive exploration (ε decay)
- Real-world relevance: recommender systems, adaptive control, financial systems
- Importance of meta-level reasoning in changing environments

📌 Personally, this project strengthened my skills in:
- Exploration vs. exploitation trade-offs
- Reinforcement learning experimentation
- Algorithm design and evaluation

---

## 📚 7. References

1. Weng, L. (2018). *Multi-Armed Bandit Algorithms*
2. Agrawal, S., & Goyal, N. (2012). *Analysis of Thompson Sampling*
3. Sutton & Barto (2018). *Reinforcement Learning: An Introduction*
4. DeepMind. *Bandit Learning Video*
5. Farina et al. (2020). *Meta Bandits, NeurIPS*

---

## 📎 Appendix

### 📌 Performance Enhancements:
- Adaptive ε-decay
- Smart success logic in Thompson Sampling
- Strategy switching based on short-term reward trends

### 📌 Literature Contribution:
- Extended classical algorithms
- Compared under non-stationary settings
- Incorporated practical improvements for real-world AI systems

---

## 💾 How to Run

1. Install dependencies:
```bash
pip install numpy matplotlib tqdm

#run to notebook
jupyter notebook MultiarmBandit.ipynb
