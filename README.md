## Super Mario Bros. AI Agent 🍄

This project features an AI agent trained to play the classic game Super Mario Bros. using reinforcement learning (RL).  The agent learns to navigate the Mushroom Kingdom, overcome obstacles, defeat enemies, and ultimately reach the flagpole at the end of each level.

### Project Goals 🎯

* Implement various RL algorithms (PPO, DQN, A2C, A3C) to train an agent on Super Mario Bros.
* Experiment with hyperparameters and training techniques to optimize agent performance.
* Create a robust training pipeline with logging and model saving capabilities.
* Visualize the agent's gameplay and analyze its decision-making process.

### Dependencies 🛠️

* Python 3.7+
* gym_super_mario_bros
* nes_py
* gymnasium
* stable-baselines3
* opencv-python
* matplotlib

You can install the necessary packages using the following command:

```bash
pip install gym_super_mario_bros nes_py gymnasium "stable-baselines3[extra]" opencv-python matplotlib
```

### Project Structure 📁

```
├── .gitignore
├── README.md
├── Mario.ipynb
├── logs/
│   └── PPO_1/
│       └── events.out.tfevents.1670359306.DESKTOP-SN7COI0.24352.0
└── .git/
    └── ...
```

* **Mario.ipynb:** Jupyter Notebook containing the main code for training and testing the agent.
* **logs/:** Directory storing TensorBoard logs generated during training.
* **README.md:** This file, providing a detailed project description.

### Training the Agent 💪

The `Mario.ipynb` notebook guides you through the entire process:

1. **Environment Setup:** Imports necessary libraries, initializes the Super Mario Bros. environment, and applies preprocessing steps (grayscaling, frame stacking).
2. **Model Selection & Training:** Choose from various RL algorithms (PPO, DQN, A2C, A3C) and configure their hyperparameters. The notebook provides example code for training with the PPO algorithm.
3. **Callbacks & Logging:** Implements a custom callback function (`TrainAndLoggingCallback`) to save model checkpoints at regular intervals and log training progress to TensorBoard.
4. **Model Saving:** Saves the trained model to disk for later evaluation or further training.

### Testing the Agent 🕹️

After training, you can load the saved model and observe its performance:

1. Load the trained model using the appropriate `load()` function from stable-baselines3.
2. Reset the environment and start the game loop.
3. Use the trained model to predict actions for each game state.
4. Render the environment to visualize the agent's gameplay.

### Future Work 🚀

* **Improve Agent Performance:** Experiment with more sophisticated RL algorithms (e.g., Rainbow DQN, A3C with LSTM), hyperparameter optimization techniques, and reward shaping strategies.
* **Level Generalization:** Train the agent on a wider variety of levels to improve its generalization capabilities and enable it to solve unseen challenges.
* **Curriculum Learning:** Gradually increase the difficulty of levels during training to help the agent learn more effectively.
* **Human-Level Performance:** Aim to train an agent that can achieve human-level performance or even surpass it, potentially uncovering novel strategies for playing the game.


This project provides a starting point for exploring the exciting field of reinforcement learning applied to video games. Feel free to experiment with different algorithms, environments, and training techniques to further enhance the agent's capabilities! 
