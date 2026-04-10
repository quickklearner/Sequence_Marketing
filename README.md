# Fake Review Detection with LLMs

## Overview
This project investigates the robustness of Transformers and Large Language Models (LLMs) for fake review detection using the [Difraud](https://huggingface.co/datasets/difraud/difraud) dataset. The study focuses on how model predictions vary under prompt rewording and across different review lengths, providing a more realistic evaluation of LLM behavior in deceptive language detection.

## Dataset
- Source: DIFRAUD (Hugging Face)
- Domain: Amazon product reviews
- Task: Binary classification (Real vs Fake reviews)
- Split: 80% Train / 10% Validation / 10% Test

### Review Length Categories
- Short: ≤ 42 tokens  
- Medium: 43–71 tokens  
- Long: > 71 tokens  

## Models

| Model     | Type          | Description |
|----------|--------------|-------------|
| RoBERTa  | Baseline     | Fine-tuned supervised transformer model |
| Qwen 7B  | LLM          | Prompt-based evaluation (zero-shot & prompt engineering) |
| Mistral  | LLM          | Instruction-tuned model for prompt-based evaluation |

## Methodology
- Fine-tune RoBERTa on labeled training data as a supervised baseline  
- Apply zero-shot and prompt-engineering techniques using Qwen 3.5 and Mistral  
- Evaluate robustness by:
  - Varying prompt formulations (prompt rewording)
  - Analyzing performance across different review lengths  
- Compare LLM performance against the supervised baseline  

## Evaluation Framework

### Quantitative Metrics
- Accuracy  
- Precision  
- Recall (primary metric due to importance of detecting fake reviews)  
- F1 Score  

### Robustness Analysis
- **Prompt Rewording Sensitivity:** Measures how predictions change with different prompt formulations  
- **Review Length Analysis:** Evaluates model performance across short, medium, and long reviews  

## Project Goals
- Assess whether LLMs can outperform traditional transformer models in fake review detection  
- Evaluate the stability of LLM predictions under realistic input variations  
- Analyze how input length impacts classification performance  



