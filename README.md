# NLP-edit-intent-classification
Edit Intent Classification using Large Language Models
This project focuses on classifying the intent behind text edits using Large Language Models (LLMs). Given an original sentence and its edited version, the goal is to identify the purpose of the edit.

Problem Statement
Edit intent classification aims to determine why a piece of text was modified. The model predicts one of the following labels:

Grammar
Clarity
Claim
Fact/Evidence
Other
Project Overview
In this project, we implement and compare four different LLM-based approaches:

Model	Description
GEN	Generative model using prompt-based classification
SEQC	Transformer-based sequence classification model
SNET	Structured input model capturing semantic differences
XNET	Enhanced model with improved input representation
Methodology
The system follows a unified pipeline:

Input: Source text + Edited text
Tokenization using transformer tokenizer
Processing using LLM-based models
Classification into edit intent categories
We compare:

Prompt-based approach (GEN)
Fine-tuned transformer models (SEQC, SNET, XNET)
Results
Fine-tuned models outperform generative approaches
SEQC, SNET, and XNET achieve higher accuracy and F1-score
GEN model provides flexibility but lower consistency
Evaluation Metrics
We evaluate models using:

Accuracy
Precision
Recall
F1 Score
Confusion Matrix
Sample Prediction
Source: "The sentence has many grammar mistake."
Target: "The sentence has many grammar mistakes."

Prediction:
GEN  → Grammar
SEQC → Grammar
SNET → Grammar
XNET → Grammar
How to Run the Project
Step 1: Clone the Repository
git clone https://github.com/Devanshu1013/Edit_Intent.git
cd Edit_Intent
Step 2: Train the Models (Optional)
Go to the src/ folder
Open each training notebook in Google Colab:
train_gen.ipynb
train_seqc.ipynb
train_snet.ipynb
train_xnet.ipynb
Run all cells and download models
Step 3: Add Models
Copy trained models into the model/ folder
OR
Use provided links to download models directly
Step 4: Run Inference
cd src
python infer_gen.py
python infer_seqc.py
python infer_snet.py
python infer_xnet.py
Step 5: Run Final Notebook
Open Edit_Intent.ipynb and run all cells.
