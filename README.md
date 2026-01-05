# 📊 Lightweight Transformers for Enterprise NLP  
### Deployment-Oriented Multi-Domain Benchmark  
**© 2025 Muhammad Shahmeer Khan**

---

![Banner](https://dummyimage.com/1100x220/1f2933/ffffff&text=Lightweight+Transformers+for+Enterprise+NLP)

<div align="center">

🧠 **Applied NLP** • ⚡ **Efficiency Benchmarking** • 🏢 **Enterprise Deployment** • 📈 **Reproducible Research**

</div>

---

## 🚀 Project Overview

This repository contains the **experimental code and notebooks** supporting the research paper:

> **“Comparative Efficiency Analysis of Lightweight Transformer Models:  
> A Multi-Domain Empirical Benchmark for Enterprise NLP Deployment”**

The goal of this project is to provide a **deployment-oriented comparison** of widely used **lightweight Transformer models** under **enterprise-relevant constraints**, focusing not only on accuracy but also on **latency, throughput, and memory efficiency**.

Rather than proposing new architectures, this work emphasizes **practical model selection guidance** for real-world NLP systems operating under resource and latency constraints.

---

## 🧪 Models Evaluated

The following pretrained Transformer architectures are benchmarked:

- **DistilBERT** (`distilbert-base-uncased`)
- **MiniLM** (`microsoft/MiniLM-L12-H384-uncased`)
- **ALBERT** (`albert-base-v2`)

All models are fine-tuned using **identical hyperparameters** to ensure fair comparison.

---

## 📚 Evaluation Domains & Datasets

The experiments span **three enterprise-relevant NLP domains**:

### 1️⃣ Customer Sentiment Classification  
**Dataset:** IMDb Movie Reviews  
- Binary sentiment classification  
- Approximates customer feedback analysis and sentiment monitoring

### 2️⃣ News Topic Classification  
**Dataset:** AG News  
- 4-class topic classification  
- Approximates document routing and content automation pipelines

### 3️⃣ Toxicity & Hate Speech Detection  
**Dataset:** Measuring Hate Speech  
- Continuous hate speech scores discretized into 3 classes  
- Approximates content moderation and security filtering workloads

---

## 📈 Metrics Reported

Each model is evaluated using both **quality** and **efficiency** metrics:

### 🔹 Accuracy Metrics
- Accuracy  
- Weighted Precision  
- Weighted Recall  
- Weighted F1-score  

### 🔹 Efficiency Metrics
- Model size (MB, FP32)
- Inference latency (ms per sample, batch size = 1)
- Throughput (samples/sec)
- Approximate RAM usage during evaluation

All inference is performed with `torch.no_grad()` enabled and includes warm-up iterations to stabilize runtime measurements.

---

## ⚙️ Experimental Setup

- Framework: **Hugging Face Transformers & Datasets**
- Hardware: **Single NVIDIA T4 GPU**
- Environment: **Google Colab**
- Epochs: **3**
- Batch size: **16**
- Max sequence length: **128**
- Random seed: **42**

The experiments are designed to reflect **rapid fine-tuning scenarios** commonly seen in enterprise deployments, where training time and infrastructure cost are critical considerations.



Each notebook is **self-contained** and can be executed independently.

---

## 🔁 Reproducibility Notes


This repository provides full code to reproduce the experiments reported in
"Comparative Efficiency Analysis of Lightweight Transformer Models"
(arXiv:2601.00444).

- All dataset splits and training runs use a fixed random seed.
- Results are reported from **single-run evaluations**.
- The analysis focuses on **relative rankings and consistent trends**, not statistical significance testing.

This design choice reflects real-world deployment scenarios, where **latency and throughput** often outweigh marginal accuracy differences.

---

## 📌 Intended Use

This repository is intended for:

- Applied NLP practitioners
- Enterprise ML engineers
- Researchers interested in deployment efficiency
- Students studying real-world model trade-offs

It is **not** intended as a tutorial or beginner-level introduction to Transformers.

---


---

## 📜 License

MIT License  
© 2025 Muhammad Shahmeer Khan

---

## 🤝 Acknowledgements

This project makes use of publicly available datasets and pretrained models provided by the Hugging Face ecosystem.  
All experiments were conducted for academic and research purposes.








