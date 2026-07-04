# ML Pipeline — Thivi's Contribution

> **Biothon 2026** · Marwadi University · Team Creatus · 🏆 Top 50 nationally (Environment & Biodiversity track)

I was responsible for the complete AI/ML pipeline in this project.
The rest of the team handled backend () FastAPI + MongoDB) and frontend ( React).

---

## What I built

### 1. DNABERT fine-tuning (core ML contribution)
- Fine-tuned `zhihan1996/DNA_bert_6` on river eDNA sequences
- Task: binary classification — Clean vs. Polluted water
- k=6 k-mer tokenization of raw DNA sequences
- Dropout regularization + data augmentation to prevent overfitting
- Corrected hyperparameters: lower LR, higher weight decay, fewer epochs
### 2. Biodiversity Health Score
- Feature extraction from Kraken2 metagenomic report (report-level, not per-sequence)
- 0–100 scoring pipeline in pure Python
- Ganga KAN-1 sample (NCBI SRR8837334) scored **80/100 — HEALTHY**


### 3. Gemini 1.5 Flash integration
- Plain-English conservation report generation from biodiversity data

---

## Data source
Real metagenomic data from NCBI-SRA: Study SRP190174, Run SRR8837334 (Ganga river)

## Architecture note
The DNABERT model is the ML research artifact (demonstrated via Colab).
The live demo uses FastAPI + pre-computed Kraken2 output — a deliberate
separation so the backend runs independently without PyTorch.
