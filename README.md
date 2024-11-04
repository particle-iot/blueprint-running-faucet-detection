# Running Faucet Detection

## Overview

The Running Faucet Detection solution is a reference project for detecting if a faucet is running, utilizing Edge Impulse's machine learning platform. This solution is designed for Particle devices like the Photon 2, Boron, and M-SoM, and leverages acoustic or vibration sensors to classify water flow patterns. With Edge Impulse, the app can recognize the unique sounds or vibrations produced by a running faucet, making it ideal for water conservation, leak detection, and smart home automation applications.

## Key Features

- **Edge Impulse Integration**: Uses Edge Impulse's machine learning capabilities to train a model specifically for detecting running water.
- **Water Conservation**: Identifies unintended water flow, helping users conserve water and reduce waste.
- **Seamless Deployment**: Supports Particle devices such as the Photon 2, Boron, and M-SoM, enabling efficient edge processing.
- **Versatile Applications**: Suitable for applications in smart home systems, water leak detection, and environmental monitoring.

## Prerequisites

To complete this project, you will need:

1. **Particle Device**: Photon 2, Boron, or M-SoM.
   - [Purchase here](https://store.particle.io/collections/all-products?filter.p.product_type=Development%20Boards)
2. **Acoustic or Vibration Sensor**: Required to capture the sound or vibration patterns associated with water flow.
3. **Edge Impulse Account**: Sign up at [Edge Impulse](https://www.edgeimpulse.com/) to train the model for faucet detection.

## Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Prerequisites](#prerequisites)
- [Setup Steps](#setup-steps)
  - [1. Configure the Hardware](#1-configure-the-hardware)
  - [2. Collect Training Data](#2-collect-training-data)
  - [3. Train the Model on Edge Impulse](#3-train-the-model-on-edge-impulse)
  - [4. Deploy the Model to Particle](#4-deploy-the-model-to-particle)
  - [5. Test and Fine-Tune](#5-test-and-fine-tune)
- [Conclusion](#conclusion)

## Setup Steps

### 1. Configure the Hardware

1. Connect an microphone to your Particle device (Photon 2, Boron, or M-SoM).
2. Set up your Particle device in the Particle Console to ensure it’s online and ready to transmit data.

## To update this project

### 1. Collect Training Data 

1. **Log into Edge Impulse** and create a new project for faucet detection.
2. Go to the **Data Acquisition** tab and collect sample data for both running and non-running faucet states.
   - Label each sample appropriately (e.g., "Running" and "Not Running").
   - Ensure data is representative of real-world scenarios to improve model accuracy.

### 2. Train the Model on Edge Impulse

1. In Edge Impulse, go to **Create Impulse** and select a suitable **Signal Processing Block** (e.g., Spectral Analysis) for audio or vibration data.
2. Add a **Learning Block** for classification.
3. Go to the **Training** tab, configure training parameters, and start training the model.
4. Monitor the training results to ensure high accuracy in distinguishing running water sounds.

### 3. Deploy the Model to Particle

1. Once the model is trained, go to the **Deployment** tab in Edge Impulse.
2. Export the model as a C++ library or a Particle-compatible model file.
3. Upload the model to your Particle device using the Particle CLI or Web IDE.
4. Configure the device firmware to run the model and classify data from the sensor.

### 4. Test and Fine-Tune

1. Deploy the Particle firmware and begin testing the device in real-world conditions.
2. Use the **Edge Impulse Live Classification** feature to validate model accuracy.
3. Fine-tune the model as needed by collecting additional data or adjusting training parameters.
