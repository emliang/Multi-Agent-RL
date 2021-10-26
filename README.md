# Multi-Agent-RL
Paper list of multi-agent reinforcement learning (MARL)

- [Multi-Agent-RL](#multi-agent-rl)
  - [Credit Assignment Problem in MARL](#credit-assignment-problem-in-marl)
    - [Explicit assignment](#explicit-assignment)
      - [Reward Assignment](#reward-assignment)
        - [Distributed Welfare Games](#distributed-welfare-games)
        - [Difference Rewards Policy Gradients](#difference-rewards-policy-gradients)
        - [Social Influence as Intrinsic Motivation](#social-influence-as-intrinsic-motivation)
        - [Incentivizing Collaboration in a Competition](#incentivizing-collaboration-in-a-competition)
        - [Social Diversity and Social Preferences in Mixed-Motive Reinforcement Learning](#social-diversity-and-social-preferences-in-mixed-motive-reinforcement-learning)
        - [Inducing Cooperation through Reward Reshaping based on Peer Evaluations](#inducing-cooperation-through-reward-reshaping-based-on-peer-evaluations)
        - [Gifting in Multi-Agent Reinforcement Learning](#gifting-in-multi-agent-reinforcement-learning)
        - [Cooperation and Reputation Dynamics with Reinforcement Learning](#cooperation-and-reputation-dynamics-with-reinforcement-learning)
      - [Value Assignment](#value-assignment)
        - [MADDPG: Multi-Agent Actor-Critic for Mixed Cooperative-Competitive Environments](#maddpg-multi-agent-actor-critic-for-mixed-cooperative-competitive-environments)
        - [COMA: Counterfactual Multi-Agent Policy Gradients](#coma-counterfactual-multi-agent-policy-gradients)
        - [Shapley Q-value: Shapley Q-value: A Local Reward Approach to Solve Global Reward Games](#shapley-q-value-shapley-q-value-a-local-reward-approach-to-solve-global-reward-games)
        - [CPGs: Causal Policy Gradients](#cpgs-causal-policy-gradients)
    - [Implicit assignment](#implicit-assignment)
      - [Value Decomposition](#value-decomposition)
        - [VDN: Value-Decomposition Networks For Cooperative Multi-Agent Learning](#vdn-value-decomposition-networks-for-cooperative-multi-agent-learning)
        - [QMIX: Monotonic Value Function Factorisation for Deep Multi-Agent Reinforcement Learning](#qmix-monotonic-value-function-factorisation-for-deep-multi-agent-reinforcement-learning)
        - [DOP: Off-Policy Multi-Agent Decomposed Policy Gradients](#dop-off-policy-multi-agent-decomposed-policy-gradients)
        - [LICA: Learning Implicit Credit Assignment for Cooperative Multi-Agent Reinforcement Learning](#lica-learning-implicit-credit-assignment-for-cooperative-multi-agent-reinforcement-learning)
        - [CollaQ: Multi-agent Collaboration via Reward Attribution Decomposition](#collaq-multi-agent-collaboration-via-reward-attribution-decomposition)
      - [Reward shaping](#reward-shaping)
        - [LIIR: Learning Individual Intrinsic Reward in Multi-Agent Reinforcement Learning](#liir-learning-individual-intrinsic-reward-in-multi-agent-reinforcement-learning)
        - [Adaptive Mechanism Design: Learning to Promote Cooperation](#adaptive-mechanism-design-learning-to-promote-cooperation)
        - [Learning to Incentivize Other Learning Agents](#learning-to-incentivize-other-learning-agents)
        - [Learning to Share in Multi-Agent Reinforcement Learning](#learning-to-share-in-multi-agent-reinforcement-learning)
        - [Inducing Desirable Equilibria in Non-Cooperative Systems](#inducing-desirable-equilibria-in-non-cooperative-systems)
        - [D3C: Reducing the Price of Anarchy in Multi-Agent Learning](#d3c-reducing-the-price-of-anarchy-in-multi-agent-learning)
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
         1. marginal contribution of agent (coalition)![](2021-10-26-19-21-52.png)
      2. Wonderful Life Utility: 
         1. counterfactual baseline![](2021-10-26-19-23-51.png)


### Explicit assignment
Explicitly calculate the contribution of single agent

#### Reward Assignment
Global reward -> (explicit calculation) -> local reward 
##### Distributed Welfare Games
   1. rules of assignment
      1. Budget balance
      2. Informational dependencies
      3. Induced nash equilibrium
   2. assignments
      1. Equally Shared
      2. Marginal Contribution
      3. Shapley Value
      4. The Weighted Shapley Value
##### Difference Rewards Policy Gradients
   1. counterfactual reward![](2021-10-26-20-27-50.png)
   2. difference return![](2021-10-26-20-28-15.png)

##### Social Influence as Intrinsic Motivation

##### Incentivizing Collaboration in a Competition

##### Social Diversity and Social Preferences in Mixed-Motive Reinforcement Learning

##### Inducing Cooperation through Reward Reshaping based on Peer Evaluations

##### Gifting in Multi-Agent Reinforcement Learning

##### Cooperation and Reputation Dynamics with Reinforcement Learning


#### Value Assignment
Global Q value -> (explicit calculation) -> local Q value
##### MADDPG: Multi-Agent Actor-Critic for Mixed Cooperative-Competitive Environments
   1. use global Q value![](2021-10-26-19-27-19.png)
##### COMA: Counterfactual Multi-Agent Policy Gradients
   1. minus a counterfactual baseline![](2021-10-26-19-27-50.png)
   2. COMA:![](2021-10-26-19-29-09.png)
##### Shapley Q-value: Shapley Q-value: A Local Reward Approach to Solve Global Reward Games
   1. use shapley value to calculate assignment![](2021-10-26-19-30-36.png)

##### CPGs: Causal Policy Gradients
   1. Multi-objective MDP
      1. consider causal graph between actions and objectives
      2. causal baseline![](2021-10-26-20-12-53.png)






### Implicit assignment

#### Value Decomposition
Global Q value -> (learning decomposition) -> Local Q value
IGM: individual-global-maximization

##### VDN: Value-Decomposition Networks For Cooperative Multi-Agent Learning
   1. Value decomposition:
![](2021-10-26-20-34-13.png)

##### QMIX: Monotonic Value Function Factorisation for Deep Multi-Agent Reinforcement Learning
   1. Value decomposition:
![](2021-10-26-20-36-17.png)

##### DOP: Off-Policy Multi-Agent Decomposed Policy Gradients
   1. Value decomposition + policy gradient
![](2021-10-26-20-38-06.png)![](2021-10-26-20-38-26.png)

##### LICA: Learning Implicit Credit Assignment for Cooperative Multi-Agent Reinforcement Learning
   1. Value decomposition + policy gradient
![](2021-10-26-20-44-18.png)

##### CollaQ: Multi-agent Collaboration via Reward Attribution Decomposition
   1. learning value decomposition by taylor approximation of optimal reward
![](2021-10-26-20-45-22.png)
   2. approximate two terms directly
![](2021-10-26-20-46-17.png)
![](2021-10-26-20-46-32.png)



#### Reward shaping
Shaping individual reward -> maximize real env-reward
Learning shaping strategy through optimization (bi-level, black-box, ...)
##### LIIR: Learning Individual Intrinsic Reward in Multi-Agent Reinforcement Learning

##### Adaptive Mechanism Design: Learning to Promote Cooperation

##### Learning to Incentivize Other Learning Agents

##### Learning to Share in Multi-Agent Reinforcement Learning

##### Inducing Desirable Equilibria in Non-Cooperative Systems

##### D3C: Reducing the Price of Anarchy in Multi-Agent Learning



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
