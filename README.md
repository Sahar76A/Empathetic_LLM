# 🧠 Safety-Constrained AI for Mental Health Support

This is an interactive **Streamlit dashboard** for comparing different safety configurations of a large language model (Mistral-7B-Instruct-v0.2) on mental health–related prompts.

The app visualizes how safety constraints affect:
- Empathy in responses
- Crisis handling ability
- Rule compliance
- Overall response quality

---

## 🚀 Features

- Browse **109 evaluation prompts**
- Filter prompts by emotion
- Compare 3 model configurations side-by-side:
  - 🔴 Baseline (no constraints)
  - 🟢 Config A (safety system prompt)
  - 🔵 Config B (system prompt + post-filtering)
- View:
  - Empathy scores (1–5)
  - Crisis handling indicators
  - Rule compliance status
- Interactive comparison table for each prompt

---

## 📊 Dataset

The app uses a labeled evaluation dataset:

- `human_eval_sheet_filled_new.csv`
- Contains:
  - Prompts
  - Emotional categories
  - Model responses (3 configurations)
  - Human evaluation scores (empathy, crisis handling, rule compliance)

---

## 🧠 Goal of the Project

This dashboard is designed to support experiments in **LLM safety for mental health contexts**, focusing on:

- Improving empathy without reducing safety
- Evaluating crisis-sensitive responses
- Comparing different safety strategies in LLMs

---

## 🖥️ How to Run

### 1. Install dependencies
```bash
pip install streamlit pandas numpy
