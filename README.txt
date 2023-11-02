Welcome to our project code_base directory. This guide provides a detailed walkthrough of the folder structure, the utilities provided, and a brief overview of how to navigate and understand the different experiments.





Table of Contents

1. Directory Structure
2. Utilities
3. Experiments
4. Usage Guidelines





Directory Structure

code_base/
│
├── utilities/
│   ├── data.py - data.ipynb
│   ├── eval_pred_funcs.py - eval_pred_funcs.ipynb
│   ├── models.py - models.ipynb
│   ├── similarity_funcs.py - similarity_funcs.ipynb
│   ├── train_funcs.py - train_funcs.ipynb
│   └── utils.py - utils.ipynb
│
├── outputs/
│   ├── evaluation(experiment 2)/
│   └── prediction(experiment 3)/
│
├── models/
│   ├── evaluation(experiment 2)/
│   └── prediction(experiment 3)/
│
├── figures/
│
├── experiment_1.ipynb
├── experiment_2.ipynb
└── experiment_3.ipynb

Subfolders Description:

1. utilities: This folder contains essential utilities and functions used across the experiments.
2. outputs: Contains the raw CSV results for experiments.
    - evaluation: Results for experiment 2.
    - prediction: Results for experiment 3.
3. models: Houses the saved models for the classic approach that is further utilised by the novel approach. (Note: Due to upload size restrictions on Learn, the actual model files have been deleted before the submission.)
    - evaluation: Saved classic models for experiment 2.
    - prediction: Saved classic models for experiment 3.
4. figures: Contains visual figure plots generated from all three experiments.





Utilities

The utilities folder houses several Python files, in both .py and .ipynd formats, that offer various functionalities:

1. data: Data processing and loading utilities.
2. eval_pred_funcs: Functions for evaluation and prediction procedures.
3. models: Definitions for different model architectures.
4. similarity_funcs: Functions to determine supermask overlaps and similarity between tasks.
5. train_funcs: Training functions for the models.
6. utils: General utility functions to support the experiments.





Experiments

There are three main Jupyter notebooks that represent our three distinct experiments:

1. experiment_1.ipynb: 
    - Libraries imported from utilities:
        - train_funcs: train
        - eval_pred_funcs: evaluate
        - models: MultitaskFC, MultitaskMaskLinear
        - data: MNISTPerm, PartitionMNIST, RotatingMNIST
        - similarity_funcs: jaccard_index, plot_supermask
        - utils: cache_masks, set_model_task, set_num_tasks_learned

2. experiment_2.ipynb:
    - Libraries imported from utilities:
        - eval_pred_funcs: evaluate
        - train_funcs: train, trainV2
        - models: MultitaskFC, MultitaskFCV2
        - data: MNISTPerm, PartitionMNIST, RotatingMNIST
        - utils: cache_masks, set_model_task, set_num_tasks_learned
        - similarity_funcs: calculate_task_similarityE1, calculate_task_similarityE2, determine_alphas

3. experiment_3.ipynb:
    - Libraries imported from utilities:
        - eval_pred_funcs: predict
        - train_funcs: train, trainV2
        - models: MultitaskFC, MultitaskFCV2
        - data: MNISTPerm, PartitionMNIST, RotatingMNIST
        - utils: cache_masks, set_model_task, set_num_tasks_learned
        - similarity_funcs: calculate_task_similarityE2, determine_alphas





Usage Guidelines

1. Setting Up:
    - Ensure you have the required Python libraries installed.
    - Navigate to the code_base folder to view its contents.

2. Utilities:
    - Before diving into the experiments, familiarise yourself with the utilities folder. This will give you insights into the underlying functions and structures that power the experiments.

3. Running Experiments:
    - You can start any of the provided Jupyter notebooks to run the respective experiment, however make sure to train the classic model before training the novel model.
    - Each notebook contains an imported libraries section at the beginning. This is where the essential utilities for the experiment are imported. This will give you a good idea of what aspects of the utilities each experiment is leveraging.

4. Outputs and Models:
    - After running the experiments, you can check the outputs folder for the raw CSV results. Note: Saved model files are not available due to Learn upload size restrictions.

5. Visualisations:
    - All generated visual plots from the experiments can be found in the figures folder.

We hope this guide provides clarity on navigating and understanding our code_base directory. If you have any further questions or encounter issues, please refer to the documentation within each Python file or notebook for more detailed explanations.