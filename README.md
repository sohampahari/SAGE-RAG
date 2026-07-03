# SAGE-RAG: Semantic-Aware Graph Retrieval-Augmented Generation for Knowledge-Intensive Multimodal Question Answering

## Abstract

Knowledge-intensive multimodal question answering requires models to reason over both visual and textual information while leveraging external knowledge sources. Existing retrieval-augmented generation approaches often struggle to effectively organize retrieved evidence and perform multi-hop reasoning across heterogeneous modalities. To address these challenges, we propose **SAGE-RAG**, a Semantic-Aware Graph Retrieval-Augmented Generation framework that constructs and reasons over structured multimodal knowledge graphs. By integrating graph-based retrieval with large multimodal language models, SAGE-RAG improves evidence aggregation, semantic grounding, and reasoning capabilities for complex visual question answering tasks.

Extensive experiments on benchmark datasets demonstrate that SAGE-RAG achieves competitive performance against state-of-the-art multimodal retrieval-augmented generation methods. Our results highlight the effectiveness of graph-structured knowledge retrieval for improving factual accuracy and reasoning in knowledge-intensive multimodal settings.

---

## Main Results

| Model                    | LLM / MLLM   | E-VQA Single-Hop |      E-VQA All | InfoSeek Unseen-Q | InfoSeek Unseen-E |   InfoSeek All |
| ------------------------ | ------------ | ---------------: | -------------: | ----------------: | ----------------: | -------------: |
| BLIP-2                   | Flan-T5XL    |             12.6 |           12.4 |              12.7 |              12.3 |           12.5 |
| InstructBLIP             | Flan-T5XL    |             11.9 |           12.0 |               8.9 |               7.4 |            8.1 |
| LLaVA-v1.5               | Vicuna-7B    |             16.3 |           16.9 |               9.6 |               9.4 |            9.5 |
| LLaVA-More               | LLaMA-3.1-8B |             15.8 |           16.0 |               9.0 |               8.2 |            8.6 |
| Qwen2-VL                 | Qwen2-VL-7B  |             19.9 |           19.7 |              19.8 |              18.5 |           19.2 |
| RORA-VLM                 | Vicuna-7B    |               -- |           20.3 |              25.1 |              27.3 |             -- |
| EchoSight                | LLaMA-3.1-8B |             22.4 |           21.7 |              30.0 |              30.7 |           30.4 |
| ReflectiVA               | LLaMA-3.1-8B |             35.5 |           35.5 |              28.6 |              28.1 |           28.3 |
| mR2AG                    | Vicuna-7B    |               -- |             -- |              40.6 |              39.8 |           40.2 |
| Wiki-LLaVA†              | Vicuna-7B    |             21.8 |           26.4 |              30.1 |              27.8 |           28.9 |
| mKG-RAG†                 | LLaMA-3.1-8B |             38.4 |           36.3 |              41.4 |              39.6 |           40.5 |
| Query-Driven MM-GraphRAG | LLaMA-3.1-8B |             37.9 |           35.8 |              40.9 |              39.4 |           40.1 |
| SAGE-RAG (Ours)          | LLaMA-3.1-8B |       28.0 ± 0.4 |     27.0 ± 0.3 |        33.5 ± 0.5 |        31.9 ± 0.4 |     32.7 ± 0.3 |
| **SAGE-RAG (Ours)†**     | LLaMA-3.1-8B |   **39.2 ± 0.3** | **37.0 ± 0.3** |    **42.1 ± 0.4** |    **40.2 ± 0.3** | **41.1 ± 0.3** |

† Fine-tuned on the corresponding dataset.

---

## Code Availability

The source code is currently not included in this repository.

The complete implementation, training scripts, evaluation pipeline, and documentation will be publicly released upon publication of the associated research paper.

This repository is currently intended to accompany the manuscript during the review process. Following publication, we will release:

* Source code
* Model checkpoints (subject to licensing constraints)
* Training and evaluation scripts
* Dataset preparation utilities
* Reproducibility instructions

Thank you for your interest in our work.
