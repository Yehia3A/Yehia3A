# ACT-NER: SOTA Code-Switched Arabic-English NER

This repository contains the implementation of a novel three-phase training pipeline for Named Entity Recognition (NER) on Code-Switched (Arabic-English) data. This research achieved a **State-of-the-Art (SOTA) F1-score of 86.4%**, significantly outperforming the CAMELBERT benchmark.

## 📈 Performance Comparison
| Model | F1-Score | Improvement |
| :--- | :--- | :--- |
| **ACT-NER (This Work)** | **86.4%** | **Baseline +7.2%** |
| Ensemble Methods | 81.7% | +4.7% |
| CAMELBERT (Benchmark) | 79.2% | - |

## 🛠️ The Challenge: Tokenizer Fragmentation
Standard multilingual models often fail on mixed-script inputs due to:
1. **Tokenizer Fragmentation:** Breaking Arabic words into meaningless sub-tokens when surrounded by Latin script.
2. **Class Imbalance:** Severe scarcity of ORG/MISC entities in low-resource code-switched datasets.

## 🚀 Key Innovations
- **Three-Phase Pipeline:** Integrated Targeted Data Augmentation, Intermediate Pre-training, and Supervised Contrastive Loss.
- **Curriculum Learning:** Dynamically ordered training data by code-switching density to reduce early-stage model noise.
- **Embedding Stabilization:** Used `paraphrase-multilingual-MiniLM` for lexical augmentation, stabilizing low-resource entity embeddings.

## 💻 Tech Stack
- **Frameworks:** PyTorch, Hugging Face Transformers
- **Techniques:** Supervised Contrastive Loss, LoRA Fine-tuning, Curriculum Learning
- **Data Handling:** Pandas, NumPy, Custom Synthetic Generation Pipelines
