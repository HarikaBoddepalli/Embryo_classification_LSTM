# Embryo Development Stage Classification (CNN-LSTM)
# Project Overview
This project implements a Deep Learning pipeline to classify human embryo development stages using a **CNN-LSTM** architecture. By processing sequences of frames rather than individual images, the model captures the temporal "story" of embryogenesis, ensuring that predictions respect biological growth patterns.

# Architecture
* **Feature Extractor (CNN):** A Time-Distributed Convolutional Neural Network extracts spatial features from each frame in a sequence.

* **Sequence Processor (LSTM):** A Long Short-Term Memory network analyzes temporal dependencies across a sliding window of 5 frames.

* **Custom Loss Function:** An Ordinal Loss function (CCE + Distance Penalty) was used to penalize predictions based on their biological distance from the true stage.

# Key Features
* **Temporal Consistency:** The model ensures that development stages follow a logical biological order.

* **Ordinal Awareness:** The custom loss function treats the 16 development phases as an ordered progression rather than independent categories.

# Performance Evaluation
* **Confusion Matrix:** Displays high accuracy along the diagonal, indicating correct stage classification.

* **Temporal Plots:** Visualizes the predicted "staircase" of development for individual embryos, demonstrating smooth transitions between phases.
