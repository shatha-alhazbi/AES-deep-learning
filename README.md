# Cross-Prompt Automated Essay Scoring Using Neural Models

This repository implements various approaches for Cross-Prompt Automated Essay Scoring (AES) using deep learning techniques. The project covers holistic and trait-based essay scoring, leveraging neural models for performance improvements across different prompts. The approaches include traditional Feedforward Neural Networks (FFN) and advanced models like BERT.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Approaches](#approaches)
   - [Approach A: FFN for Holistic Scoring](#approach-a-ffn-for-holistic-scoring)
   - [Approach B: Joint Model for Holistic and Trait Scoring](#approach-b-joint-model-for-holistic-and-trait-scoring)
   - [Approach C: BERT for Holistic Scoring](#approach-c-bert-for-holistic-scoring)

## Project Overview
This project applies deep learning to the task of **Automated Essay Scoring (AES)**, specifically solving the challenge of **cross-prompt AES**. The goal is to train models that score essays written for a different prompt than the one they were trained on. The models are built using PyTorch and the Hugging Face Transformers library.

The project includes three primary approaches:
- **Approach A**: Uses Feedforward Neural Networks for holistic scoring.
- **Approach B**: A joint model that performs both holistic and trait-based scoring using FFNs.
- **Approach C**: Implements BERT for holistic scoring (this is an optional, more advanced approach).

## Approaches

### Approach A: FFN for Holistic Scoring
This approach utilizes a **Feedforward Neural Network (FFN)** to predict a single holistic score for essays. The model is trained on various essay features, and the output is a predicted quality score for each essay.

#### Key Components:
- Input: Essay features (e.g., word embeddings, sentence features).
- Output: Single holistic score for the essay.
- Model: A simple FFN architecture.

### Approach B: Joint Model for Holistic and Trait Scoring
This model extends Approach A by jointly predicting both **holistic scores** and **trait-specific scores** (e.g., content, fluency, word choice). The FFN is modified to output multiple predictions at once.

#### Key Components:
- Input: Essay features (similar to Approach A).
- Output: Holistic score and trait scores (multiple outputs).
- Model: Modified FFN for multi-task learning.

### Approach C: BERT for Holistic Scoring (Bonus)
In this approach, **BERT** (Bidirectional Encoder Representations from Transformers) is fine-tuned to predict holistic scores for essays. This approach leverages the power of transformer models for improved performance in scoring essays across different prompts.

#### Key Components:
- Input: Tokenized essay text.
- Output: Single holistic score.
- Model: Fine-tuned BERT model using Hugging Face's Transformers library.
