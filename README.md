# AIORI-3 Hackathon Projects

This repository contains the code, resources, and implementation developed as part of the **AIORI-3 Hackathon**.

## Live Demo

**Deployed Application:** https://fedflow.netlify.app/

Explore the deployed application to see the project in action.

## Team Introduction

Watch our team introduction video:

[**AIORI-3 Team Introduction Video**](https://youtu.be/Zrpoz8Gk6qA)

## About the Project

**FedFlow** explores traffic-flow forecasting using Federated Learning, combining time-series prediction with communication-efficient collaborative model training.

The project investigates how multiple clients can collaboratively train a shared traffic forecasting model while keeping their raw training data local.

### Key Features

- **Traffic-Flow Forecasting:** Uses a Gated Recurrent Unit (GRU) neural network to predict future traffic from historical measurements.
- **Federated Learning:** Implements Federated Averaging (FedAvg) to aggregate model updates from distributed clients.
- **IID and Non-IID Experiments:** Evaluates learning under different distributions of traffic data across clients.
- **Communication Efficiency:** Compares FP32, FP16, and INT8 model-update representations to measure communication overhead.
- **Performance Evaluation:** Analyses forecasting accuracy, convergence behaviour, and communication costs using metrics such as MAE, RMSE, and MAPE.

### Implementation Overview

The implementation uses Python, PyTorch, and the PeMS traffic datasets (PeMS-03, PeMS-04, PeMS-07, and PeMS-08).

A compact GRU model takes one hour of historical traffic measurements, along with time-related features, to forecast traffic flow over the next hour. Four simulated clients train locally on their assigned sensor data, while a central server aggregates their model updates using FedAvg.

The experimental framework compares centralised, local-only, and federated training to investigate the trade-offs between predictive performance and communication cost.

## Technology Stack

- **Language:** Python
- **Deep Learning:** PyTorch
- **Model:** GRU
- **Learning Paradigm:** Federated Learning (FedAvg)
- **Datasets:** PeMS Traffic Datasets
- **Deployment:** Netlify

## Objective

To investigate how federated learning can support traffic-flow forecasting while balancing prediction accuracy, distributed data ownership, and communication efficiency.

---

**Built for the AIORI-3 Hackathon.**
