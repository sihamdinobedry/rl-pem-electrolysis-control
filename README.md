# rl-pem-electrolysis-control
# Reinforcement Learning-Based Control of PEM Electrolysis for Sustainable Ammonia Synthesis

MSc Dissertation Project in Data Science & Artificial Intelligence.

This repository contains the implementation of a Deep Reinforcement Learning (DRL) agent that uses the Proximal Policy Optimization (PPO) algorithm to autonomously control a simulated Proton Exchange Membrane (PEM) electrolyser. The system is powered by variable solar energy, and the controller optimizes for hydrogen production efficiency, operational stability, and safety, with a focus on applications in sustainable ammonia synthesis.

## Key Findings and Results

The PPO-based controller was rigorously benchmarked against a traditional PID controller, the industry standard. The results demonstrate a significant performance improvement:

-   **19.4% Improvement in Efficiency:** Achieved 0.602 kg H₂/kWh compared to PID's 0.504 kg H₂/kWh.
-   **Enhanced Stability:** Significantly reduced voltage oscillations under dynamic solar input.
-   **Safety Guaranteed:** All operations were constrained within a predefined safety envelope.
-   **Sensitivity Analysis:** A formal analysis identified the clip range (ε) as the most critical hyperparameter for training stability and performance.

## Repository Structure

```
├── agents/          # Code for the PPO agent and PID baseline
├── envs/            # Custom Gymnasium environment for the PEM electrolyser
├── notebooks/       # Jupyter notebooks for analysis and visualization
├── SolarProfile.csv          # Input data: renewable energy profile for simulation
├── Training_analysis.ipynb   # Jupyter notebook for training the PPO agent and benchmarking against PID
├── SensitivityAnalysis.ipynb # Jupyter notebook for hyperparameter sensitivity analysis
├── requirements.txt          # Python package dependencies
└── README.md                 # This file
```
## Installation and Usage

### Prerequisites

-   Python 3.8+
-   pip
# Create and activate a virtual environment (e.g., with venv)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install the required packages
pip install -r requirements.txt

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/rl-pem-electrolysis-control.git
cd rl-pem-electrolysis-control
