---
title: "Explaining RL Decisions using Trajectories"
collection: publications
category: conferences
permalink: /publication/traj_attrib
excerpt: <b>S Deshmukh</b>, A Dasgupta, C Agarwal, N Jiang, B Krishnamurthy, G Theocharous, J Subramanian.
date: 2023-01-21
venue: 'International Conference on Learning Representations (ICLR)'
# slidesurl: 'http://academicpages.github.io/files/slides1.pdf'
paperurl: 'https://openreview.net/pdf?id=5Egggz1q575'
# citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
---

Explanation is a key component for the adoption of reinforcement learning (RL) in many real-world decision-making problems. In the literature, the explanation is often provided by saliency attribution to the features of the RL agent's state. In this work, we propose a complementary approach to these explanations, particularly for offline RL, where we attribute the policy decisions of a trained RL agent to the trajectories encountered by it during training. To do so, we encode trajectories in offline training data individually as well as collectively (encoding a set of trajectories). We then attribute policy decisions to a set of trajectories in this encoded space by estimating the sensitivity of the decision with respect to that set. Further, we demonstrate the effectiveness of the proposed approach in terms of quality of attributions as well as practical scalability in diverse environments that involve both discrete and continuous state and action spaces such as grid-worlds, video games (Atari) and continuous control (MuJoCo). We also conduct a human study on a simple navigation task to observe how their understanding of the task compares with data attributed for a trained RL policy. Keywords -- Explainable AI, Verifiability of AI Decisions, Explainable RL.