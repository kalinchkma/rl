# Multi-armed Bandit

## Epsilon-Greedy (Theory)
- UCB1 and Bayesian methods work better but they all have tha same api

Pseudocode:
- Greedy
    - while True:
        - j = argmax(predicted bandit means)
        - x = play bandit j and get reward
        - bandits[j].update_mean(x)
  
- Epsilon-Greedy
    - While True:
      - p = random number in [0, 1]
      - if p < epsilon:
        - j = choose a random bandit
      - else:
        - j = argmax(predicted bandit means)
      - x = play bandit j and get reward
      - bandits[j].update_mean(x)
- Decaying Epsilon:
  - e(t) <=> 1/t "<=>" (proportional), "e" (epsilon)
  - e(t) = max(e(0) - kt, e(min))
  - e(t) = e(0)t
  - e(t) = a / (log(bt+c))
   
# Methods
  - epsilon greedy
    - optimistic initial value (it usage pure greedy method)
    - pure greedy

