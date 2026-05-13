# Empathetic_LLM
# GenAI Hackathon Project

## Safe-Empathetic-LLM

Design and Evaluation of Safety-Constrained Generative AI for Mental Health Support Conversations

---

## Overview

This project investigates whether safety constraints applied to an instruction-tuned large language model improve response quality and safety in non-clinical mental health support contexts — without reducing empathy or coherence.

We evaluate three configurations of **Mistral-7B-Instruct-v0.2** using 109 emotionally grounded prompts derived from the EmpatheticDialogues dataset and a manually constructed synthetic crisis dataset.

The system is designed to compare how different levels of safety enforcement impact:
- empathy quality
- crisis handling ability
- rule compliance
- overall response coherence

---

## What This System Does (Explanation)

The system works like a controlled experiment for LLM safety.

It:
- takes emotionally sensitive user prompts
- sends them to the same base model under 3 different safety setups
- generates responses for each setup
- evaluates how safe, empathetic, and reliable the responses are

The goal is to understand whether adding structured safety rules improves or harms model behavior in mental health–related conversations.

---

## Key Results

| Metric | Baseline | Config A | Config B |
|--------|----------|----------|----------|
| Empathy Score (1–5) | 2.00 | 3.91 | 3.86 |
| Crisis Recall | 0.0 | 1.0 | 1.0 |
| Rule Violation Rate | 0% | 0% | 0% |
| BERTScore F1 | 0.8738 | 0.8673 | 0.8657 |
| Filter False Positives | N/A | N/A | 0 |

**Main finding:** Safety constraints significantly improve empathy (+1.9 points) while maintaining perfect crisis detection performance.

---

## Experimental Configurations

🔴 **Baseline**  
Mistral-7B-Instruct-v0.2 with no additional constraints  

🟢 **Config A**  
Baseline + structured 9-rule safety system prompt:
- No diagnosis  
- No medical advice  
- Mandatory crisis redirection  
- Empathetic tone enforcement  

🔵 **Config B**  
Config A + post-generation rule-based filtering system that corrects or overrides unsafe responses  

---

## Repository Structure

```text
Safe-Empathetic-LLM/
├── mental_health_safety_pipeline.ipynb
├── mental_health_safety_evaluation.ipynb
├── human_eval_sheet_filled.csv
├── app.py
├── requirements.txt
└── README.md
