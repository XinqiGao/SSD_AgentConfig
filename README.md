[![Build Status](https://travis-ci.com/eugenevinitsky/sequential_social_dilemma_games.svg?branch=master)](https://travis-ci.com/eugenevinitsky/sequential_social_dilemma_games)
# Implementation and Learning for Multiagent SSD setting of DeepMind Sequential Social Dilemma Games

This repo is forked and modified based on an open-source implementation of DeepMind's Sequential Social Dilemma (SSD) multi-agent game-theoretic environments [[1]](https://arxiv.org/abs/1702.03037). SSDs can be thought of as analogous to spatially and temporally extended Prisoner's Dilemma-like games. The reward structure poses a dilemma because individual short-term optimal strategies lead to poor long-term outcomes for the group.

The implemented environments are structured to be compatible with [OpenAIs gym environments](https://github.com/openai/gym) as well as [RLlib's Multiagent Environment](https://github.com/ray-project/ray/blob/master/rllib/env/multi_agent_env.py)

## Implemented Games

* **Cleanup**: A public goods dilemma in which agents get a reward for consuming apples, but must use a cleaning beam to clean a river in order for apples to grow. While an agent is cleaning the river, other agents can exploit it by consuming the apples that appear.

<img src="images/cleanup.png" alt="Image of the cleanup game" width="170" height="246"/>

* **Harvest**: A tragedy-of-the-commons dilemma in which apples regrow at a rate that depends on the amount of nearby apples. If individual agents employ an exploitative strategy by greedily consuming too many apples, the collective reward of all agents is reduced.

<img src="images/harvest.png" alt="Image of the Harvest game" width="483" height="187"/>

<img src="images/schelling.png" alt="Schelling diagrams for Harvest and Cleanup" width="953" height="352"/>

The above plot shows the empirical Schelling diagrams for both Cleanup (A) and Harvest (B) (from [[2]](https://arxiv.org/abs/1803.08884)). These diagrams show the payoff that an individual agent can expect if it follows a defecting/exploitative strategy (red) vs a cooperative strategy (blue), given the number of other agents that are cooperating.  We can see that an individual agent can almost always greedily benefit from detecting, but the more agents that defect, the worse the outcomes for all agents.  


## Relevant papers

1. Leibo, J. Z., Zambaldi, V., Lanctot, M., Marecki, J., & Graepel, T. (2017). [Multi-agent reinforcement learning in sequential social dilemmas](https://arxiv.org/abs/1702.03037). In Proceedings of the 16th Conference on Autonomous Agents and MultiAgent Systems (pp. 464-473).

2.  Hughes, E., Leibo, J. Z., Phillips, M., Tuyls, K., Dueñez-Guzman, E., Castañeda, A. G., Dunning, I., Zhu, T., McKee, K., Koster, R., Tina Zhu, Roff, H., Graepel, T. (2018). [Inequity aversion improves cooperation in intertemporal social dilemmas](https://arxiv.org/abs/1803.08884). In Advances in Neural Information Processing Systems (pp. 3330-3340).

3. Jaques, N., Lazaridou, A., Hughes, E., Gulcehre, C., Ortega, P. A., Strouse, D. J., Leibo, J. Z. & de Freitas, N. (2018). [Intrinsic Social Motivation via Causal Influence in Multi-Agent RL](https://arxiv.org/abs/1810.08647). arXiv preprint arXiv:1810.08647.
        
# Contributors
This code base was initially developed by Eugene Vinitsky and Natasha Jaques; help with reproduction was provided by Joel Leibo, Antonio Castenada, and Edward Hughes. Additional development was done by Hugo Heemskerk. Support for PettingZoo was provided by Rohan Potdar. 


