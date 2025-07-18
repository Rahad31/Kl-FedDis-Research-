# KL-FedDis: A Federated Learning Approach with Distribution Information Sharing

![KL-FedDis](https://img.shields.io/badge/Federated%20Learning-KL--FedDis-blue)  
A PyTorch-based implementation of **KL-FedDis**, a federated learning framework that incorporates Kullback–Leibler divergence for effective communication and training in non-IID environments.

## 🧠 About

This repository provides the official code for the paper:  
**"KL-FedDis: A Federated Learning Approach with Distribution Information Sharing Using Kullback-Leibler Divergence for Non-IID Data"**  
Published in *Neuroscience Informatics (Q1 Journal), Elsevier.*

**Authors:** Md. Rahad, Ruhan Shabab, Mohd. Sultan Ahammad, Md. Mahfuz Reza, Amit Karmaker, Md. Abir Hossain, PhD  
[[Link to Paper](#)] ← *(Add actual link)*

---

## 📌 Highlights

- KL divergence-based model distribution sharing
- Improves training convergence under Non-IID settings
- Benchmarked on CIFAR-10 using PyTorch
- Simulated multi-client federated environment

---

## 🗂️ Project Structure

```bash
KL-FedDis/
├── data_loader.py        # Data loading and partitioning
├── models.py             # VAE and CNN models
├── train.py              # Client and server training logic
├── utils.py              # Helper functions
├── main.py               # Main script to run training
├── config.yaml           # Configuration parameters
└── README.md             # Project documentation
