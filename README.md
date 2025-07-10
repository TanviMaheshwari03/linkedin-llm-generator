# LinkedIn Post Generator LLM 🔗🤖

A lightweight, LoRA-tuned Large Language Model designed to generate professional, human-like LinkedIn posts across various tones, themes, and audiences. This project was developed using an open-source base (Mistral-7B) and trained on a **fully synthetic dataset** with zero dependency on commercial APIs.

## 💡 Features
- Accepts custom themes, tones, audiences, and CTA prompts
- Generates posts in a variety of styles: advice, milestone, story, announcement
- Includes both CLI and Gradio-powered UI for seamless interaction
- Designed to run in Google Colab with 4-bit quantization for efficient fine-tuning

## 🧠 Model
- **Base**: `Mistral-7B-Instruct-v0.1`
- **Adapter**: LoRA (rank=8) using PEFT
- **Training Dataset**: 1,000 synthetic posts in instruction format

📦 Files
linkedin-lora-model/: LoRA adapter weights
generate_post.py: Inference script (CLI + Gradio)
synthetic_linkedin_dataset.csv: Cleaned training data
sample_outputs.pdf: 20 generated LinkedIn posts


---

## ✅ 2. `model_card.md` (Standard HuggingFace-style)

## Model Overview
This model is designed to generate professional LinkedIn posts in various tones and themes. It is fine-tuned using LoRA adapters on top of the Mistral-7B-Instruct model using synthetic instruction-tuned data.

## Training Data
The dataset is **fully synthetic** and was programmatically generated to simulate human-like posts across:
- Themes: Career Advice, Internships, Leadership, Women in Tech, etc.
- Tones: Inspirational, Grateful, Visionary, Humble
- Audience: Students, Hiring Managers, Tech Peers

## Model Details
- Base: `mistralai/Mistral-7B-Instruct-v0.1`
- Fine-tuning: PEFT (LoRA)
- Tokenization: SentencePiece tokenizer

## Intended Use
To generate LinkedIn-style professional content suitable for:
- Job announcements
- Internship reflections
- Career milestones
- General thought leadership

## License
MIT License. All training data is synthetic and original.

## Limitations
- May generate boilerplate-style output under repeated prompting
- Not tuned for other social media styles (e.g., Twitter, Instagram)

## Ethical Considerations
All data is synthetic and contains no real user data, personal stories, or scraped content.
