# Model Selection Checklist & Evaluation Template
Published:  2026-02-14

> A structured, repeatable template for selecting the correct Hugging Face model.

---

# 1. Selection Brief Template

## Project Name:

## Date:

## Owner:

---

## Use Case Definition
- Primary Task (e.g., Embeddings / Chatbot / Sentiment / Image Classification):
- Business Objective:
- Target Users:
- Domain (e.g., finance, support tickets, retail images):

---

## Technical Constraints
- Deployment Target (Colab GPU / Cloud GPU / Other):
- GPU Type & VRAM (if known):
- Latency Requirement (e.g., <2s interactive):
- Expected Input Length (tokens or image size):
- Required Context Window (LLMs only):
- Expected Throughput:
- Storage Constraints:

---

## Compliance & Risk
- Commercial Use Required? (Yes/No)
- License Restrictions:
- Data Sensitivity Considerations:
- Safety/Alignment Requirements:

---

# 2. Shortlist Comparison Table

| Model Name | Parameters | Precision | Context Window | License | Leaderboard Rank | Notes |
|------------|------------|-----------|----------------|---------|------------------|-------|
|            |            |           |                |         |                  |       |
|            |            |           |                |         |                  |       |
|            |            |           |                |         |                  |       |
|            |            |           |                |         |                  |       |
|            |            |           |                |         |                  |       |

Guidelines:
- Include 2 top-performing models
- Include 1–2 smaller/faster alternatives
- Include 1 widely adopted baseline

---

# 3. Evaluation Results Table

## Evaluation Dataset Description
- Number of Samples:
- Source:
- Domain Alignment:

---

| Model Name | Accuracy / Recall@k | Latency (ms) | Memory Usage | Observed Failure Modes | Overall Score |
|------------|--------------------|--------------|--------------|-----------------------|---------------|
|            |                    |              |              |                       |               |
|            |                    |              |              |                       |               |
|            |                    |              |              |                       |               |

---

# 4. Final Decision Rationale

## Selected Model:

## Why This Model Was Chosen:
- Performance Justification:
- Latency Justification:
- Memory/Infrastructure Fit:
- License Approval:
- Risk Considerations:

## Trade-offs Accepted:

## Deployment Notes:

---

# Example Use Case (From Guide)

## Scenario: Embeddings for Semantic Search / RAG

Business Objective:
Improve internal document search accuracy for a knowledge base.

Constraints:
- Deployment: Single GPU (Colab)
- Latency: <500ms per query
- Commercial license required

Shortlist Strategy:
- 2 top MTEB retrieval models
- 2 smaller embedding models
- 1 widely adopted baseline

Evaluation Metrics:
- Recall@5
- nDCG@10
- Query latency
- Embedding dimension impact on vector DB size

Decision Example:
Selected a mid-sized embedding model with slightly lower leaderboard score but 40% lower latency and acceptable Recall@5 performance.

Rationale:
Balanced retrieval quality with infrastructure efficiency while meeting license requirements.

---

This checklist ensures model selection decisions are documented, reproducible, and defensible from both an engineering and governance perspective.

---

(c) 2026 Brock Frary - All rights reservered
