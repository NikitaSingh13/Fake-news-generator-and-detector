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

## 📦 Installation & Usage

### 🔧 Installation
```bash
pip install torch transformers gradio
▶️ Usage
If you're running the code in a Python script:

bash
Copy
Edit
python app.py
If using a Jupyter Notebook or Google Colab:

Just run all cells in order.

Gradio will generate a public link to open the interface.

📁 File Structure
bash
Copy
Edit
├── Fake-news-generator-and-detector.ipynb   # Main notebook file
├── README.md                                # Project documentation
📌 Future Improvements
Fine-tune GPT-2 on domain-specific datasets for more relevant generation.

Improve BERT classification accuracy with custom datasets.

Add support for multilingual fake news detection.

Deploy the model using Flask or FastAPI for production use.

Add a download option for generated articles.

Add explainability using LIME or SHAP for the BERT model.

🧪 Sample Use Cases
Education: Demonstrate AI's ability to generate and detect fake content.

Research: Explore ethical AI and misinformation propagation.

Media: Assist fact-checking by quickly validating article content.

📚 References
Hugging Face Transformers

Gradio Documentation

LIAR Dataset (Fake News Detection)

🔒 Disclaimer
This tool is created for educational and research purposes only. Generating or spreading misinformation intentionally is unethical and may be illegal. Use responsibly.

🤝 Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change or improve.
