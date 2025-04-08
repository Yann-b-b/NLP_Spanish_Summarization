# Spanish Summarization with Small Language Models (SLMs)

This project explores the effectiveness of fine-tuned **Small Language Models (SLMs)** for Spanish-language summarization, using outputs from **Bloom-7b** and **Llama3.1:7b** as training baselines and **Mistral-7B-Instruct** as an automated grader.

## 📄 Overview

We investigate whether smaller models (GPT-Neo-125M, Phi-1.5B, TinyLlama-1.1B) can approach the summarization performance of large language models, focusing on a dataset of 5,000 Spanish Wikipedia biographies.

## 🧠 Models Used

- **GPT-Neo-125M** – Fully fine-tuned.
- **Phi-1.5B** and **TinyLlama-1.1B** – Fine-tuned using LoRA.
- **Bloom-7b** – Used to generate training summaries.
- **Llama3.1:7b** – Reference baseline.
- **Mistral-7B-Instruct** – Automated grading of summaries.

## ⚙️ Methodology

1. Preprocessed Spanish Wikipedia articles.
2. Used Bloom-7b and Llama3.1:7b to generate summaries.
3. Graded summaries with Mistral-7B based on:
   - Relevance
   - Coherence
   - Conciseness
4. Fine-tuned SLMs using LoRA and/or full training.
5. Evaluated using ROUGE, BLEU, METEOR, and BERTScore.

## 📊 Results

- **GPT-Neo-125M** achieved the best scores across all metrics.
- **SLMs** showed competitive performance with much lower compute requirements.
- Mistral-based grading helped guide fine-tuning and evaluate quality.

## 🔍 Key Findings

- Small models can learn to produce high-quality summaries when guided by LLM-generated data and graded feedback.
- LoRA helps scale training for larger SLMs on limited hardware.
- Automated grading offers a promising approach to evaluating and refining generated content.

## 🚧 Limitations

- Dataset limited to 5,000 articles.
- BLEU/ROUGE metrics don't fully capture factual accuracy.
- Computation time for larger models still a constraint.

## 📌 Future Work

- Add factual consistency checks (e.g., entity matching).
- Explore RLHF using grading scores as rewards.
- Scale to other languages and domains.

---

**Author:** Yann Baglin-Bunod  
📧 yann.baglin-bunod@polytechnique.edu  
📍 École Polytechnique

