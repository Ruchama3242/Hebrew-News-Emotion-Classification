# Hebrew-News-Emotion-Classification


This project explores the use of Deep Learning models to classify emotional reactions triggered by short Hebrew news headlines, collected in the period following 7/10/2023 in Israel.

# Project Goal

To build a system that receives a short news headline in Hebrew and predicts the dominant emotional response:

Fear (0)

Pain (1)

Determination (2)

# Dataset

~900 manually collected Hebrew news headlines

Sources: Israeli news sites such as Rotter, Maariv, and MivzakimNet

Balanced distribution of classes:

Fear: 289

Pain: 298

Determination: 308

# Methodology

The project combines Hebrew embeddings with different neural architectures:

Embeddings: HeBERT, AlephBERT

Models: MLP, Bi-LSTM/GRU (RNN), Transformer (fine-tuning partial & full)

Techniques used: Dropout, L2 Regularization, Batch/Layer Normalization, EarlyStopping

# Results

Best overall performance: MLP with AlephBERT (~80% accuracy)

Fine-tuning BERT (partial) improved stability and reduced overfitting

Recall by class:

Pain: 0.83 (highest)

Determination: 0.67

Fear: 0.50 (most challenging to classify)

# Key Insights

AlephBERT embeddings consistently outperformed HeBERT

Short headlines may not benefit significantly from complex sequence models, making MLP surprisingly effective

Overfitting was mitigated using Dropout (0.3–0.4) and L2 Regularization

# Limitations & Future Work

Relatively small, manually labeled dataset (<1,000 headlines)

No external validation dataset used

Possible extensions:

Semi-supervised labeling for larger datasets

Adding more emotion categories (hope, anger, frustration, etc.)

Training smaller custom Transformers for short-text tasks

# References

HeBERT

AlephBERT

Data sources: Rotter, Maariv, MivzakimNet
