# Machine Learning Practices

This repository contains a collection of practical machine learning labs developed for coursework at the University of Zaragoza. The exercises cover classical supervised learning, Gaussian processes, reinforcement learning, convolutional neural networks, transfer learning, autoencoders, deep feature visualization, and deep reinforcement learning.

## Authors

- Eryka Liced Rimacuna Castillo
- Luis Catalan Salas

## Repository Structure

```text
.
|-- p1/                         # Supervised learning notebooks
|-- p2/                         # Gaussian process labs
|-- p3/                         # Reinforcement learning notebooks and Pacman/Gridworld code
|-- p4/                         # CNN, fine-tuning, and semantic segmentation notebooks
`-- P5/                         # Autoencoders, visualization, t-SNE, and deep RL notebooks
```

## Contents

### Practice 1: Supervised Learning

Located in [`p1/`](p1/).

- `p1_songs.ipynb`: regression for year prediction.
- `p1_cifar.ipynb`: classification on the CIFAR-10 dataset.

### Practice 2: Gaussian Processes

Located in [`p2/`](p2/).

- `lab_gps_part_1.ipynb`: one-dimensional Gaussian process regression.
- `lab_gps_part_2.ipynb`: Gaussian processes applied to geographic air-quality data.
- `lab_gps_part_3.ipynb`: implementation of a custom Gaussian process regression workflow.

### Practice 3: Reinforcement Learning

Located in [`p3/`](p3/).

This section includes reinforcement learning notebooks and a Pacman/Gridworld project adapted for value iteration, Q-learning, approximate Q-learning, and policy search.

Main files:

- `policy_search_cart_pole.ipynb`: policy search with REINFORCE for CartPole.
- `FAQs about Lab2.ipynb`: reinforcement learning lab notes.
- `reinforcement/valueIterationAgents.py`: value iteration agents.
- `reinforcement/qlearningAgents.py`: Q-learning and approximate Q-learning agents.
- `reinforcement/analysis.py`: parameter choices for specific Gridworld scenarios.
- `reinforcement/autograder.py`: local autograder entry point.

Sample reinforcement learning outputs:

| Gridworld values | Pacman Q-learning result |
| --- | --- |
| ![Gridworld value estimates](p3/results/q6.png) | ![Pacman training result](p3/results/q8.png) |

### Practice 4: Convolutional Neural Networks

Located in [`p4/`](p4/).

- `Simple2NN_Optional.ipynb`: two-layer neural network exercise.
- `SimpleCNN_Optional.ipynb`: CNN training from scratch on a toy subset of the Oxford-IIIT Pet dataset.
- `CNN_Finetuning.ipynb`: transfer learning and fine-tuning with a pretrained CNN.
- `OPT_TorchVision_SemanticSeg.ipynb`: semantic segmentation using TorchVision models.
- `README`: Oxford-IIIT Pet dataset reference notes.

### Practice 5: Deep Learning Extensions

Located in [`P5/`](P5/).

- `Lab5_VisualizationTSNE.ipynb`: t-SNE visualization of deep CNN feature spaces.
- `Lab5_autoencoder.ipynb`: autoencoders with TensorFlow/Keras.
- `Lab5_VisualizationCNN.ipynb`: saliency maps and fooling images for CNN interpretability.
- `Lab5_DRL_Tutorial_2024.ipynb`: deep reinforcement learning for Atari-style environments.
- `lab5-files/`: helper utilities and small sample image data.

Example images used in the CNN visualization lab:

| Sample image 1 | Sample image 2 |
| --- | --- |
| ![Sample cat image](P5/lab5-files/datasets/img1.jpeg) | ![Sample image](P5/lab5-files/datasets/img2.jpeg) |

## Getting Started

### 1. Clone the repository

```bash
git clone <repository-url>
cd Machine_Learning_Practicas
```

### 2. Create a Python environment

Python 3.9 or newer is recommended for most notebooks.

```bash
python -m venv .venv
source .venv/bin/activate      # macOS/Linux
# .venv\Scripts\activate       # Windows PowerShell
```

### 3. Install common dependencies

There is no single requirements file because each lab uses a different stack. A practical base setup is:

```bash
pip install jupyter numpy pandas scipy matplotlib seaborn scikit-learn
pip install tensorflow keras torch torchvision
pip install GPy geopy pyproj plotly pillow tqdm opencv-python
pip install gymnasium stable-baselines3 ale-py
```

Some notebooks may require additional packages depending on the runtime, dataset source, or GPU availability.

### 4. Launch the notebooks

```bash
jupyter lab
```

Then open the notebook for the practice you want to run.

## Running the Reinforcement Learning Autograder

From the reinforcement learning project folder:

```bash
cd p3/reinforcement
python autograder.py
```

To run a specific question:

```bash
python autograder.py -q q6
```

## Notes

- The notebooks were originally designed for educational environments such as Jupyter or Google Colab.
- Some exercises download datasets at runtime, so an internet connection may be required.
- GPU acceleration is useful for the CNN, autoencoder, and deep reinforcement learning notebooks, but many smaller exercises can run on CPU.
- Generated outputs for the reinforcement learning practice are stored in [`p3/results/`](p3/results/).

## License and Attribution

Several labs are based on or adapted from educational materials, including University of Zaragoza coursework, Stanford CS231n materials, TensorFlow/Keras tutorials, TorchVision tutorials, Berkeley Pacman reinforcement learning projects, and other referenced sources inside the notebooks. Please keep the original attribution notices when reusing or modifying this material.
