# 📰 Fake News Generator & Detector

This project is a dual-purpose **Natural Language Processing (NLP)** application built using transformer-based models. It includes:

- A **Fake News Generator** using **GPT-2** to create realistic-looking news articles based on a given prompt.
- A **Fake News Detector** using **BERT** to classify whether a news article or statement is fake or real.

It also features a clean and user-friendly **Gradio** web interface for easy interaction with both models.

---

## 🎯 Objectives

- Showcase the creative and discriminative powers of transformer models.
- Provide hands-on experience in both generating synthetic content and detecting misinformation.
- Deliver an interactive tool for exploring ethical and technical aspects of AI-generated content.

---

## 🛠️ Tech Stack

- **Python**
- **PyTorch**
- **Transformers Library** (Hugging Face)
  - GPT-2 for text generation
  - BERT (bert-base-uncased) for binary classification
- **Gradio** for the web-based user interface

---

## 📈 How It Works

1. **Load Pre-trained Models**  
   - GPT-2 is used for generating content.
   - BERT is used for detecting fake vs real news.

2. **Fake News Generation**  
   - User provides a news headline or topic.
   - GPT-2 generates a news-like paragraph based on the prompt.

3. **Fake News Detection**  
   - User pastes an article or statement.
   - BERT classifies it as **Fake** or **Real** with confidence score.

4. **Gradio Interface**  
   - Two tabs: one for generation and one for detection.
   - Outputs are displayed interactively in the browser.

---

## 💡 Challenges Faced & Solutions

- **Slow Inference with Large Models**  
  Models like GPT-2 and BERT were slow on free-tier Colab.  
  ✅ *Used Colab Pro for GPU and optimized generation with shorter sequences.*

- **Limited Dataset for Fake News Detection**  
  Training from scratch wasn’t feasible.  
  ✅ *Fine-tuned pre-trained BERT (`bert-base-uncased`) on benchmark datasets like LIAR.*

- **Gradio Integration Issues**  
  Multiple components caused sync and layout bugs.  
  ✅ *Modularized logic and tested each UI tab independently before merging.*

---

## 📦 Installation

### 🔧 Installation
pip install torch transformers gradio


