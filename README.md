# 🗺️ Autonomous Terrain Analysis & Pathfinding AI

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

> **A Deep Learning pipeline that perceives complex terrains and plans optimal trajectories in 20x20 grid environments.**

---

## 🚀 Overview

This project tackles the challenge of **autonomous navigation** in unstructured environments. Given a raw map image containing various terrains (forests, deserts, labs), the system must:
1.  **Perceive**: Identify walkable paths, obstacles (walls), hazards, start points, and goal points using Computer Vision.
2.  **Plan**: Compute the safest and most efficient path from Start to Goal.

The solution integrates **Deep Semantic Segmentation (ResNet-UNet)** with **Classical Graph Search (A*)** to achieve near-perfect navigation performance.

---

## ✨ Key Features

* **🧠 Advanced Perception**: Uses a **ResNet34-UNet** architecture to segment 20x20 maps with high pixel-wise accuracy.
* **🏭 Synthetic Data Engine**: Includes a custom generator that creates thousands of synthetic training maps with realistic textures to overcome data scarcity.
* **⚡ Velocity-Aware A***: A custom A* implementation that handles variable terrain costs (avoiding hazards vs walls).
* **🛡️ Robust Inference**: Implements **Test-Time Augmentation (TTA)** (flips/rotations) to ensure stable predictions on unseen data.
* **🎯 High Accuracy**: Achieved **>99% pathfinding success rate** on the validation set.

---

## 🛠️ Tech Stack

| Domain | Technology |
| :--- | :--- |
| **Deep Learning** | PyTorch, Torchvision (ResNet34 Backbone) |
| **Image Processing** | OpenCV, PIL, Albumentations |
| **Data Handling** | NumPy, Pandas |
| **Algorithms** | A* (A-Star), BFS, Manhattan Geometry |
| **Visualization** | Matplotlib, Seaborn |

---

## 📂 Project Structure

```bash
📦 Terrain-Pathfinding-AI
 ┣ 📂 input
 ┃ ┣ 📂 train
 ┃ ┃ ┣ 📂 images      # Raw terrain images
 ┃ ┃ ┗ 📂 labels      # Ground truth JSONs
 ┣