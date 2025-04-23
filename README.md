# 🧠 Text-to-SQL BART Fine-Tuning

This project fine-tunes the `facebook/bart-base` model to convert natural language prompts into SQL queries using the [Gretel Synthetic Text-to-SQL](https://huggingface.co/datasets/gretelai/synthetic_text_to_sql) dataset.

It demonstrates the use of Large Language Models (LLMs) for domain-specific structured generation, with evaluation using BLEU scores and a Gradio-powered interactive demo.

---

## 📂 Project Structure

```
text-to-sql-bart-finetuning/
├── LLMFinetuning.ipynb           # Full implementation notebook
├── Technical_Report.pdf          # Technical report detailing methods & results
├── requirements.txt              # pip-based environment
├── environment.yml               # Conda environment file
```

---

## 🚀 Features

- ✅ Fine-tuning `facebook/bart-base` on SQL generation
- ✅ Custom tokenizer and dataset preprocessing
- ✅ BLEU score evaluation using Hugging Face `evaluate`
- ✅ Real-time testing with a Gradio interface
- ✅ Dataset: subset of 3,000 training + 500 test examples

---

## 🧪 How to Run

### 1. Install dependencies

Using pip:
```bash
pip install -r requirements.txt
```

Or with conda:
```bash
conda env create -f environment.yml
conda activate llm-finetuning
```

### 2. Open notebook

Launch Jupyter or run in Google Colab:
```bash
jupyter notebook LLMFinetuning.ipynb
```

---

## 📊 Evaluation

Model performance is measured using the BLEU score:

- **BLEU Score:** `20.04`  
- Indicates strong SQL pattern learning with room for fine-tuning on edge cases

---

## 🎮 Gradio Interface

A lightweight Gradio app allows you to input any natural language query and compare:
- Output from base `facebook/bart-base`
- Output from the fine-tuned model

Launch using:
```python
import gradio as gr
interface.launch()
```

---

## ⚙️ Future Work

- Incorporate full 100k+ dataset for diverse SQL structures
- Use schema-aware prompting
- Add SQL execution testing and exact match evaluation
- Extend Gradio UI for schema inputs and multi-table joins

---

## 🙌 Acknowledgments

- [Hugging Face Transformers](https://huggingface.co/docs/transformers)
- [Gretel Synthetic Text-to-SQL Dataset](https://huggingface.co/datasets/gretelai/synthetic_text_to_sql)
- [Gradio](https://www.gradio.app/)
