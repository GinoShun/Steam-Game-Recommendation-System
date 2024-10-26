# Steam Game Recommender System

## Project Overview
This project aim to build a recommendation system for Steam games. 
It utilizes different machine learning models including LSTM, ResNet, and NCF (Neural Collaborative Filtering) to predict and recommend games based on user data and interactions. 
The dataset used for this project is from Kaggle: [Game Recommendations on Steam]
(https://www.kaggle.com/datasets/antonkozyriev/game-recommendations-on-steam/data?select=games_metadata.json).

## Project Structure
The project repository is organized into the following folders and files:

### 1. model/
This directory contains the trained models used in the recommendation system.
- **balanced(best)/**: Contains the best models trained using forcus loss balancing.
  - `best_ncf_model(epoch77).h5`: The best Neural Collaborative Filtering model
  - `lstm__strongActions(epoch8).h5`: The best LSTM model
  - `resnet_best(epoch34).h5`: The best ResNet model
- **unbalanced(old)/**: Contains models trained without focal loss balancing.

### 2. notebook/
This folder includes Jupyter notebooks used for training and analyzing the models.
- `diagram.ipynb`: Notebook to visualize the structure of the models.
- `model_evaluation.ipynb`: Notebook for evaluating model performance, including metrics such as accuracy and ROC curve.
- `prepare.ipynb`: Data structure visualization.
- `steam_game_recommender.ipynb`: Recommender system realization.
- `train.ipynb`: The main notebook for data processing and model training.

### 3. outcome/
This directory contains results of the models, including plots and evaluation metrics.
Including accuracy, confuision matrix and loss plots under focal loss alpha value equals to 0.13 and 0.14.
- **LSTM/**: Results from LSTM models.
- **NCF/**: Results from NCF models.
- **ResNet/**: Results from ResNet models.

### Other Files
- `.gitignore`: Specifies files and directories to be ignored by Git.
- `headers.txt`: Contains headers used in requests or API calls for data collection.