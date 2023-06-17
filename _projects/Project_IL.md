---
layout: page
title: Q-Learning 
description: 
img: assets/img/video_12000_IL.gif
importance: 1
category: Academic
---

**Introduction:**
In the field of artificial intelligence, reinforcement learning is a powerful technique that enables an agent to learn optimal actions through trial and error. In this blog post, we'll explore a simple yet effective example of reinforcement learning using Q-tables. We'll train an agent to navigate a grid world, avoiding enemies and seeking rewards.

**Setting up the Environment:**
Our grid world consists of a square grid with a specified size. The agent, represented by a blue blob, moves within this grid. We also have food items (green blobs) that provide rewards when reached and enemies (red blobs) that impose penalties when encountered.

<div class="row">
    <div class="col-sm mt-3 mt-md-0" style="text-align:center">
        {% include figure.html path="assets/img/Grid_world.png" title="Environment" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Fig 1: Our Grid World Environment. Green : Food, Red : Enemy and Blue : Agent.
</div>

**Defining the Q-Table:**
To facilitate the learning process, we utilize a Q-table, which is a lookup table that maps state-action pairs to their corresponding Q-values. The Q-value represents the expected future reward for taking a specific action in a given state. Initially, the Q-table is randomly initialized.

**Training the Agent:**
We run multiple episodes of interaction between the agent and the environment. In each episode, the agent selects actions based on an exploration-exploitation trade-off controlled by the epsilon parameter. If a random value is greater than epsilon, the agent exploits its current knowledge and chooses the action with the highest Q-value. Otherwise, it explores by selecting a random action.

<div class="row">
    <div class="col-sm mt-3 mt-md-0" style="text-align:center">
        {% include figure.html path="assets/img/Video_12000_IL.gif" title="Agent in action" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Fig 2: Our agent in action. 
</div>

During the episode, the agent moves in the grid world, and its state changes based on the relative positions of the food and enemies. The agent updates its Q-values using the Q-learning algorithm, which incorporates the observed rewards and future Q-values. The learning rate and discount factor influence the weight given to immediate rewards and future rewards, respectively.

**Visualizing the Training:**
To provide visual feedback, we use OpenCV and matplotlib. We create an image for each step of the episode, highlighting the agent, food, and enemies in different colors. These images are combined to create a video that showcases the agent's behavior and learning progress. We also plot a moving average of the episode rewards to track the agent's performance over time.

<div class="row">
    <div class="col-sm mt-3 mt-md-0" style="text-align:center">
        {% include figure.html path="assets/img/MA_plot.png" title="Moving Average" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Fig 3: The results after training. We have calculated moving average of reward at every 3000 episode and plotted it against No. of Episodes. 
</div>


**Conclusion:**
In this blog post, we've explored the concept of reinforcement learning using Q-tables and applied it to train an agent in a grid world environment. By updating Q-values based on rewards and future expectations, the agent learns to make optimal decisions. We've visualized the training process using videos and plotted the episode rewards to analyze the agent's performance.




