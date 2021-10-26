# Multi-Agent-RL
Paper list of multi-agent reinforcement learning (MARL)

- [Multi-Agent-RL](#multi-agent-rl)
  - [Credit Assignment Problem in MARL](#credit-assignment-problem-in-marl)
    - [Explicit assignment](#explicit-assignment)
      - [Value Assignment](#value-assignment)
        - [MADDPG: Multi-Agent Actor-Critic for Mixed Cooperative-Competitive Environments](#maddpg-multi-agent-actor-critic-for-mixed-cooperative-competitive-environments)
        - [COMA: Counterfactual Multi-Agent Policy Gradients](#coma-counterfactual-multi-agent-policy-gradients)
        - [Shapley Q-value: Shapley Q-value: A Local Reward Approach to Solve Global Reward Games](#shapley-q-value-shapley-q-value-a-local-reward-approach-to-solve-global-reward-games)
        - [CollaQ: Multi-agent Collaboration via Reward Attribution Decomposition](#collaq-multi-agent-collaboration-via-reward-attribution-decomposition)
        - [CPGs: Causal Policy Gradients](#cpgs-causal-policy-gradients)
      - [Reward Assignment](#reward-assignment)
    - [Implicit assignment](#implicit-assignment)
      - [Value Decomposition](#value-decomposition)
      - [Reward shaping](#reward-shaping)
  - [Information Sharing in MARL](#information-sharing-in-marl)
    - [State Aggregation](#state-aggregation)
    - [State & Action Aggregation](#state--action-aggregation)
  - [Planning in MARL](#planning-in-marl)
    - [Explicit planning](#explicit-planning)
    - [Implicit planning](#implicit-planning)
- [Hierarchical Reinforcement Learning](#hierarchical-reinforcement-learning)
  - [Goal-conditioned HRL](#goal-conditioned-hrl)
  - [HAM](#ham)
  - [UVFA](#uvfa)
  - [FuN](#fun)
  - [h-DQN](#h-dqn)
  - [HER](#her)
  - [HIRO](#hiro)
  - [Language as an Abstraction](#language-as-an-abstraction)


## Credit Assignment Problem in MARL
In the cooperative MARL setting, either global reward or individual reward is coupled with other agents. The Credit Assignment Problem is to assign proper reward or value to agents, so agents can make cooperative decisions individually.
1. Difference reward
   1. [Optimal Payoff Functions for Members of Collectives. 2001](http://www.eecs.harvard.edu/cs286r/courses/spring06/papers/wolptumer_optimalPay01.pdf)
      1. Aristocrat Utility:
         1. marginal contribution of agent (coalition)
      2. Wonderful Life Utility: 
         1. counterfactual baseline
2. Potential game
   1. [Distributed Welfare Games. 2013](https://pubsonline.informs.org/doi/pdf/10.1287/opre.1120.1137)
      1. Resource Allocation Problems
         1. separable welfare functions: $W(a)=\sum_{r \in \mathcal{R}} W_{r}\left(\{a\}_{r}\right)$
         2. submodular welfare function: $W_{r}(S \cup\{i\})-W_{r}(S) \geq W_{r}(T \cup\{i\})-W_{r}(T)$ if $S \subseteq T \subseteq N$, decreasing marginal returns
         3. finite strategic-form game: finite action sets
         4. potential game: change in play's utility function equals to the change in a global potential function. exist pure nash equilibrium
         5. Budget balance: $\sum_{i \in S} f_{r}(i, S)=W_{r}(S)$
         6. Informational dependencies: 
      2. Utility Design for Distributed Welfare Games
         1. Equally Shared: $f_{r}^{\mathrm{ES}}(i, S)=\frac{W_{r}(S)}{|S|}$
            1. budget balanced, low information dependency
            2. if players are anonymous, become congestion game, exit nash equilibrium.
         2. Marginal Contribution: $f_{r}^{\mathrm{MC}}(i, S)=W_{r}(S)-W_{r}(S \backslash\{i\})$
            1. wonderful life utility (WLU)
            2. not budget balanced, mid information dependency 
            3. potential function is global welfare function 
            4. any action profile that maximizes the global welfare is an equilibrium.
         3. Shapley Value: $f_{r}^{\mathrm{SV}}(i, S)=\sum_{T \subseteq S \backslash\{i\}} \frac{|T| !(|S|-|T|-1) !}{|S| !}\left(W_{r}(T \cup\{i\})-W_{r}(T)\right)$ 
            1. high informational dependency, budget balanced
            2. the potential function is as:
         4. The Weighted Shapley Value: $f_{r}^{\mathrm{WSV}}(i, S):=\sum_{T \subseteq S: i \in T} \frac{w_{i}}{\sum_{j \in T} w_{j}}\left(\sum_{R \subseteq T}(-1)^{|T|-|R|} W_{r}(R)\right)$

### Explicit assignment

#### Value Assignment
##### MADDPG: Multi-Agent Actor-Critic for Mixed Cooperative-Competitive Environments
##### COMA: Counterfactual Multi-Agent Policy Gradients
##### Shapley Q-value: Shapley Q-value: A Local Reward Approach to Solve Global Reward Games
##### CollaQ: Multi-agent Collaboration via Reward Attribution Decomposition
##### CPGs: Causal Policy Gradients

#### Reward Assignment


### Implicit assignment

#### Value Decomposition

#### Reward shaping







## Information Sharing in MARL

### State Aggregation
### State & Action Aggregation





## Planning in MARL

### Explicit planning

### Implicit planning


## Hierarchical Reinforcement Learning
### Goal-conditioned HRL
#### HAM
#### UVFA
#### FuN
#### h-DQN
#### HER
#### HIRO
#### Language as an Abstraction
