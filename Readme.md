# Sanskrit-to-English Neural Machine Translation

## Overview

This repository contains the implementation of **Assignment 2 – Sanskrit-to-English Neural Machine Translation** for the Natural Language Understanding (NLU) course.

The objective of this project is to develop a Neural Machine Translation (NMT) system that translates Sanskrit sentences into English using a pretrained multilingual Transformer model.

---

## Model

- **Pretrained Model:** facebook/nllb-200-distilled-600M
- **Architecture:** Transformer Encoder–Decoder
- **Framework:** PyTorch & Hugging Face Transformers
- **Tokenizer:** NLLB Tokenizer
- **Inference:** Beam Search (Beam Size = 5)

---

## Dataset

The project uses the Sanskrit-English parallel corpus provided as part of the assignment.

| Dataset | Sentence Pairs |
|----------|---------------:|
| Training | 10,000 |
| Validation | 1,000 |
| Test | 1,000 |

No external datasets or APIs were used.

---

## Training Configuration

| Parameter | Value |
|-----------|-------|
| Epochs | 5 |
| Learning Rate | 3e-5 |
| Optimizer | AdamW |
| Batch Size | 4 |
| Gradient Accumulation | 4 |
| Maximum Sequence Length | 128 |
| Mixed Precision | FP16 |
| Random Seed | 42 |

---

## Results

| Metric | Value |
|---------|------:|
| BLEU Score | 29.85 |
| BERTScore (F1) | 0.5982 *(Assignment evaluation with `rescale_with_baseline=True`)* |
| Inference Time | 584.29 seconds |
| Model Parameters | 615073792 |

---

## Repository Structure

```
.
├── G25AIT1044_NLU_Assignment2.ipynb
├── Report.pdf
├── submission.csv
├── README.md
```

---

## Requirements

- Python 3.12+
- PyTorch
- Transformers
- Datasets
- Accelerate
- SentencePiece
- SacreBLEU
- BERTScore

All required packages are installed within the notebook.

---

## Running the Project

1. Open `G25AIT1044_NLU_Assignment2.ipynb` in Jupyter Notebook or Google Colab.
2. Install the required dependencies.
3. Upload the provided dataset.
4. Run the notebook sequentially.
5. The notebook generates:
   - Trained model
   - BLEU Score
   - BERTScore
   - Inference Time
   - Model Parameters
   - `submission.csv`

---

## Files

- **G25AIT1044_NLU_Assignment2.ipynb** – Complete implementation and evaluation.
- **Report.pdf** – Project report.
- **submission.csv** – Predicted English translations for the test dataset.

---

## References

1. Costa-jussà et al., *No Language Left Behind: Scaling Human-Centered Machine Translation*, 2022.
2. Papineni et al., *BLEU: a Method for Automatic Evaluation of Machine Translation*, ACL 2002.
3. Zhang et al., *BERTScore: Evaluating Text Generation with BERT*, ICLR 2020.
4. Hugging Face Transformers Documentation.

---

## Author

**Balasubramanian Manikandan**

Natural Language Understanding – Assignment 2