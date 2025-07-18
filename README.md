# KL-FedDis: A Federated Learning Approach with Distribution Information Sharing

![KL-FedDis](https://img.shields.io/badge/Federated%20Learning-KL--FedDis-blue)  
A PyTorch-based implementation of **KL-FedDis**, a federated learning framework that incorporates Kullback–Leibler divergence for effective communication and training in non-IID environments.

## 🧠 About

This repository provides the official code for the paper:  
**"KL-FedDis: A Federated Learning Approach with Distribution Information Sharing Using Kullback-Leibler Divergence for Non-IID Data"**  
Published in *Neuroscience Informatics (Q1 Journal), Elsevier.*

**Authors:** Md. Rahad, Ruhan Shabab, Mohd. Sultan Ahammad, Md. Mahfuz Reza, Amit Karmaker, Md. Abir Hossain, PhD  
[[https://www.sciencedirect.com/science/article/pii/S277252862400027X](#)] 

---

## 📌 Highlights

- KL divergence-based model distribution sharing
- Improves training convergence under Non-IID settings
- Benchmarked on CIFAR-10 using PyTorch
- Simulated multi-client federated environment

---

## 🗂️ Project every file Structure

```bash
🧱 1. Model Definitions
VAE — Variational Autoencoder for learning data distributions

Net — CNN-based image classification model

📦 2. Data Preparation
transform — Data normalization and transformation pipeline

CIFAR10 — Dataset loading

train_set, val_set, test_set — Data split

DataLoader — Batching and shuffling

📚 3. Loss Functions
vae_loss(recon_x, x, mu, logvar) — Combines reconstruction loss + KL divergence

CrossEntropyLoss() — For classification model training

🏋️ 4. Training Functions
vae_train(vae, trainloader, epochs) — Trains VAE on local client data

train(net, trainloader, valloader, epochs) — Trains classification model

📊 5. Evaluation
evaluate(net, testloader) — Computes test accuracy of classification model

🧑‍🤝‍🧑 6. Federated Client Simulation
initialize_clients(trainset, transform, batch_size, num_clients)
→ Splits data and creates local data loaders per client

🔄 7. Distribution Sharing for KL-FedDis
get_distribution_info(vae) — Extracts mean & std from VAE

send_distribution_info(info) — Stub to send info to global server

receive_distribution_info() — Stub to receive info from other clients

generate_augmented_data(vae, info) — Synthesizes new data using Truncated Normal

🌐 8. Model Aggregation and Communication
send_model_update(client_id, model_update) — Stub to send model to server

(Note: No aggregation logic yet, could be added later)

🔁 9. Federated Training Coordinator
federated_train(...) — Manages full round: local training + sharing + updating

🧠 10. Global Orchestration
global_server() — Initializes models, clients, coordinates FL rounds

if __name__ == "__main__" — Entry point to run the simulation



---

## 📚 Citation
If you use this code, please cite:

bibtex

@article{rahad2024klfeddis,
  title={KL-FedDis: A Federated Learning Approach with Distribution Information Sharing Using Kullback-Leibler Divergence for Non-IID Data},
  author={Rahad, Md. and Shabab, Ruhan and Ahammad, Mohd. Sultan and Reza, Md. Mahfuz and Karmaker, Amit and Hossain, Md. Abir},
  journal={Neuroscience Informatics},
  year={2024},
  publisher={Elsevier}
}

---
## 🤝 Contact
For questions, feel free to contact:

Md. Rahad
📧 rahad3100@gmail.com

