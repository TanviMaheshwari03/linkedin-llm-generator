# Model Card: LinkedIn Post Generator LLM (LoRA-tuned Mistral-7B)

## 📌 Model Overview

**LinkedIn Post Generator LLM** is a lightweight, fine-tuned large language model designed to generate high-quality, human-like, and professional posts tailored for LinkedIn. The model takes in key parameters such as **theme**, **tone**, **audience**, and **call-to-action**, and outputs a coherent, context-aware, and stylistically aligned LinkedIn post.

This model was developed entirely on **Google Colab**, without any dependency on commercial APIs (e.g., OpenAI, Anthropic), using **LoRA (Low-Rank Adaptation)** to fine-tune **Mistral-7B-Instruct** on a **fully synthetic dataset**.

---

## 🧠 Base Model Details

- **Base Model**: [`mistralai/Mistral-7B-Instruct-v0.1`](https://huggingface.co/mistralai/Mistral-7B-Instruct-v0.1)
- **Architecture**: Decoder-only transformer (7B parameters)
- **License**: Apache 2.0 (Open-source & commercially permissible)

---

## 🧪 Training Details

### Training Platform:
- Google Colab (T4 GPU, 4-bit quantized model)

### Finetuning Technique:
- **PEFT + LoRA** (Parameter-Efficient Fine-Tuning)
- Quantized using `bitsandbytes` (4-bit NF4 precision)
- Target Modules: `q_proj`, `k_proj`, `v_proj`, `o_proj`
- LoRA Config:
  - Rank (`r`): 8  
  - Alpha: 16  
  - Dropout: 0.05  
  - Optimizer: AdamW

### Training Duration:
- ~3 epochs on 1,000 samples
- Batch Size: 4  
- Gradient Accumulation: 4  
- Learning Rate: 2e-4  
- Mixed Precision: FP16

---

## 📊 Dataset Summary

- **Type**: Instruction-tuned synthetic dataset
- **Size**: 1,000 rows
- **Format**: `prompt` + `response`
- **Fields Included**:
  - `theme`: (e.g., Career Advice, Internship)
  - `tone`: (e.g., Humble, Grateful, Visionary)
  - `audience`: (e.g., Hiring Managers, Students)
  - `post_body`: synthetic human-style post text
  - `cta`: (call to action)

> ⚠️ No personal, scraped, or user-generated content was used. All data is 100% synthetic and copyright-safe.

---

## 🎯 Intended Use

This model is intended for:

- Generating professional LinkedIn posts automatically
- Helping students, interns, or job-seekers create thought-leadership content
- Powering personal branding assistants or resume-booster tools
- Educational use in NLP, instruction tuning, and LoRA-based training

---

## 🚫 Limitations

- May overuse common phrasing due to limited synthetic diversity
- Not fine-tuned for other platforms like Twitter, Instagram, or long-form blogs
- Lacks deep world knowledge or external fact grounding (no RAG)
- Does not include grammar-checking or filtering logic post-generation

---

## 📄 License & Rights

- **Model Code**: MIT License
- **Training Data**: Fully synthetic, copyright (c) 2025 Tanvi [Last Name]
- **Adapter Weights**: Redistributable under MIT or Apache 2.0

> This model does not depend on OpenAI, Anthropic, or proprietary datasets, and is independently copyrightable.

---

## 💬 Contact

**Author**: Tanvi Maheshwari  
**Institution**: [MIT World Peace University, Pune]  
**Project Timeline**: July 2025  
**Submission Deadline**: 13 July 2025

For demo requests or contributions,Lets Connect.

---

