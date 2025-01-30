# BraVE: Offline Reinforcement Learning for Discrete Combinatorial Action Spaces

This repository contains the official BraVE implementation.
## How to run the code

### Install dependencies
```
pip install --upgrade pip
pip install -r requirements.txt
```

### Create offline data
```
python agents/A_Star.py --save_transitions --grid_dimension 10 --grid_size 5 --num_pits 5 --num_clusters 1 --small_state --suboptimal_rate 0.9
```

### Run training/evaluation
```
python agents/BraVE.py --data_load_path offline_data/10-5-5-1-0.9 --q_loss_multiplier 20 --num_beams 200 --num_network_layers 2
```
