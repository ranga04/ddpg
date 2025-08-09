
# DDPG for Continuous Control in Pendulum Simulation

## Overview
This project demonstrates the implementation of the **Deep Deterministic Policy Gradient (DDPG)** algorithm to solve a continuous control task using the **Pendulum-v1** environment from OpenAI Gym. The goal of the project was to train an agent to stabilize the pendulum by learning optimal control policies through reinforcement learning.

## Key Features:
- **Actor-Critic Architecture**: The DDPG algorithm uses separate Actor and Critic networks to learn the policy and the value function.
- **Continuous Action Space**: The environment involves continuous control of the pendulum, where the agent must balance the pendulum by applying torque.
- **Replay Buffer**: Experiences are stored and sampled from a replay buffer to enable more stable learning.
- **Target Networks**: Soft updates are used for the Actor and Critic target networks to improve stability during training.

## Training Results
- The agent was trained for 200 episodes. Initially, the total rewards were highly negative (around -1500), but after training, the rewards improved significantly, with episodes achieving rewards close to -120.
- The agent exhibited fluctuations in performance, which is common in reinforcement learning. However, it demonstrated the ability to balance the pendulum effectively in many episodes.

### Reward Progression:
- **Initial Phase (0-50 episodes)**: The agent started with highly negative rewards around -1500 as it explored the environment.
- **Middle Phase (50-150 episodes)**: Significant improvement in rewards, with fluctuations between -500 and -100.
- **Final Phase (150-200 episodes)**: The agent’s performance stabilized, with rewards ranging between -500 and -100, and occasional spikes to near-zero rewards.

![Reward Curve](reward_curve.png)  <!-- Add your reward curve image here -->

### Test Results:
After training, the agent was evaluated over 10 test episodes without exploration noise. The rewards for the test episodes were as follows:

```
Test Episode 1:  [-233.18239]
Test Episode 2:  [-125.95068]
Test Episode 3:  [-245.02379]
Test Episode 4:  [-599.8194]
Test Episode 5:  [-368.67355]
Test Episode 6:  [-124.97035]
Test Episode 7:  [-241.57462]
Test Episode 8:  [-122.02011]
Test Episode 9:  [-240.48283]
Test Episode 10: [-357.30594]
```

### Conclusion:
- The DDPG agent successfully learned to control the pendulum, with several test episodes achieving rewards close to -120, indicating effective control. 
- There are still fluctuations in performance, which could be improved with further tuning, but for the purposes of this portfolio project, the results are satisfactory.
- The project highlights the complexity of reinforcement learning in continuous control tasks, balancing exploration and exploitation.

## Future Improvements:
- **Noise Decay**: Implementing a noise decay strategy could help stabilize the policy further in later training episodes.
- **Extended Training**: More training episodes could help the agent fine-tune its policy and improve consistency in performance.
- **Hyperparameter Tuning**: Adjusting learning rates and the soft update parameter could lead to a more stable policy.


## License
This project is licensed under the MIT License.

