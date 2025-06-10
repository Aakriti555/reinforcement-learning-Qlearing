🐢 Q-Learning with Turtles (Tom and Jerry Simulation)
This project demonstrates a basic implementation of Q-Learning, a Reinforcement Learning technique, using Python's turtle module. The simulation involves two agents:

Tom (Predator)

Jerry (Prey)

The goal is for Jerry to escape while Tom tries to catch him on a grid world with obstacles. Both agents learn optimal movement strategies through trial and error over time.

📁 Project Structure
main.py – The core script running the environment and Q-learning loop.

condition.yaml – Stores the learned Q-table for Tom (predator).

prey.yaml – Stores the learned Q-table for Jerry (prey).

1.3 jerry.gif – Custom image for Jerry (Prey).

1.5 tom.gif – Custom image for Tom (Predator).

🛠️ Installation
Make sure you have Python 3 installed.

Install dependencies:

bash
Copy
Edit
pip install pyyaml
The turtle module is built-in and does not require installation.

Run the script:

bash
Copy
Edit
python main.py
🎮 How It Works
1. Grid Environment
The screen is set to a 700x700 window.

The environment is divided into a grid of (x, y) positions from -300 to 300 in steps of 50.

2. Agents
Tom (Predator) starts at (-300, -300).

Jerry (Prey) starts at (300, 300).

Both agents are represented by turtle graphics with custom images.

3. Obstacles
Certain grid cells are marked as obstacles.

Neither agent can pass through obstacles or go outside the boundary.

4. Q-Learning Parameters
alpha (Learning Rate): 0.1

gamma (Discount Factor): 0.9

epsilon (Exploration Rate): 0.1

5. Learning Process
Each agent maintains its own Q-table (stored as YAML files).

Jerry learns to escape from Tom.

Tom learns to chase Jerry.

The reward system encourages agents to maximize distance (Jerry) or minimize distance (Tom).

6. Game Loop
For each pair of start and goal states:

The agents simulate multiple episodes.

After each episode:

Tom scores if he catches Jerry.

Jerry scores if he survives 70 steps.

7. Saving Knowledge
Q-tables are saved to condition.yaml and prey.yaml after training.

These tables can be reused for future simulations without retraining from scratch.

📊 Visualization
Tom’s score and Jerry’s score are displayed on the top-left of the screen.

The environment is animated using Turtle graphics to visualize learning.

📦 Requirements
Python 3.x

pyyaml

turtle (standard library)

🧠 Concepts Demonstrated
Reinforcement Learning (Q-Learning)

Epsilon-Greedy Action Selection

Multi-Agent Training (Predator-Prey)

Custom Grid World Environment

🚀 Future Improvements
Add more intelligent obstacle generation.

Save and load agent states dynamically based on user input.

Introduce different speeds for predator and prey.

Implement neural network approximation instead of Q-table for large-scale environments.

🧑‍💻 Author
Developed as a simulation of reinforcement learning with turtle graphics in Python.
