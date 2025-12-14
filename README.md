# RajneetiDrishti  
### A Two-Stage Vision–Language Ensemble Framework for Political Meme Classification

RajneetiDrishti is a **resource-efficient, test-only, two-stage vision–language ensemble framework** designed for **binary political meme classification** in the Bangladeshi context. The framework leverages **multimodal reasoning**, **metadata enrichment**, and **knowledge-injected validation** to achieve state-of-the-art performance **without any training or fine-tuning requirements**.

🏆 **Ranked 1st on the PoliMemeDecode private leaderboard**  
⚡ **Runs on free-tier GPUs with ~4s inference time per sample**  
📊 **Achieves up to 93.71% Macro F1-score**

---

## 📌 Key Features

- **Two-Stage Sequential Ensemble**
  - Stage 1: Metadata-enhanced classification
  - Stage 2: Knowledge-driven validation and correction
- **No Training Required**
  - Operates entirely on test data
  - No fine-tuning or backpropagation
- **Multimodal Understanding**
  - Combines image content, OCR text, and semantic metadata
- **Low-Resource Friendly**
  - Designed for free-tier GPUs
  - Suitable for low-resource languages like Bangla
- **Domain Knowledge Injection**
  - Uses a curated Bangladeshi political keyword knowledge base

---

## 🧠 Framework Overview

### 🔹 Stage 1: Metadata-Enhanced Classification
- **Model:** `Qwen2.5-VL-7B-Instruct`
- **Inputs:**
  - Meme image
  - OCR-extracted text
  - Metadata CSV:
    - Language
    - Humor
    - Metaphor
    - Meme Explanation
    - Metaphor Object
    - Political Intensity
- **Output:** Initial binary prediction (Political / Non-Political)

### 🔹 Stage 2: Knowledge-Enhanced Validation
- **Model:** `Phi-3-Vision-128k-Instruct`
- **Enhancements:**
  - Injected Bangladeshi political entities, parties, events, and terminology
- **Inputs:**
  - Original meme image
  - Stage 1 prediction
  - Selected metadata
- **Output:** Final validated prediction

---

## 📂 Dataset

- **Dataset:** PoliMemeDecode
- **Total Memes:** 2,800
- **Test Samples Used:** 330
- **Languages:** Bangla, English, Banglish
- **Annotations (Generated via Qwen):**
  - Humor type
  - Metaphor localization
  - Political intensity
  - Semantic explanations

⚠️ This framework **only uses the test split** to demonstrate resource-efficient inference.

---

## 📊 Performance Summary

| Configuration | Macro F1 (%) |
|---------------|-------------|
| Qwen2.5-VL-7B (Single) | 91.61 |
| Phi-3-Vision-128k (Single) | 89.66 |
| **Qwen2.5-VL-7B + Phi-3-Vision-128k** | **93.71** |

⏱ **Inference Time:**  
- Single model: ~3.5s  
- Two-stage ensemble: ~4.0s  

🖥 **GPU Requirement:** Free-tier GPU (no high-end hardware)

---

## 🔬 Evaluation Metric

- **Macro F1-score**
  - Ensures balanced evaluation across political and non-political classes
  - Robust to class imbalance

---

## 🚀 Why RajneetiDrishti?

- Avoids **black-box fine-tuning**
- Demonstrates **test-only ensemble intelligence**
- Practical for **real-world deployment**
- Ideal for **privacy-sensitive and low-resource environments**
- Establishes a **blueprint for equitable multimodal AI**

---

## 📄 Paper

If you use this work, please refer to the original paper:

> **RajneetiDrishti: A Two-Stage Vision-Language Ensemble Framework for Political Meme Classification**  
> Team NeuronX  
> Chittagong University of Engineering and Technology &  
> Daffodil International University, Bangladesh :contentReference[oaicite:0]{index=0}

---
