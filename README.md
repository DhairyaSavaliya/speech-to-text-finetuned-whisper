# 🎙️ Fine-Tuned Whisper for Speech-to-Text (English)

> **Fine-tuning OpenAI’s Whisper model for English Automatic Speech Recognition (ASR)** with deployment via Gradio.  
> Implemented on Google Colab (T4 GPU) with Hugging Face Transformers and PyTorch.

---

## 🧠 Overview

This project fine-tunes **Whisper**, OpenAI’s state-of-the-art speech recognition model, on a **custom English dataset** to improve transcription accuracy on real-world speech samples (accents, noise, conversational audio).

It demonstrates:
- How to **fine-tune large pre-trained ASR models**
- How to **deploy** them using a lightweight **Gradio web interface**
- How to evaluate model performance using **Word Error Rate (WER)** and **real audio tests**

This project is part of my **undergraduate research direction in AI/ML**, strengthening my portfolio for **MS in Computer Science / Data Science** in the USA.

---

## ⚙️ Key Highlights

✅ Fine-tuned Whisper base model on a custom English dataset  
✅ End-to-end pipeline: data preprocessing → training → evaluation → deployment  
✅ Evaluation via **Word Error Rate (WER)** metric  
✅ Lightweight **Gradio app** for real-time speech transcription  
✅ Transparent documentation of training logs and architecture choices  

---

## 🏗️ Project Architecture

data/
 ├── train/
 ├── test/
 └── custom_audio_samples/
notebooks/
 ├── ASR_Fine_Tuned.ipynb      # Fine-tuning workflow
 └── Speech_to_Text_Baseline.ipynb  # Pretrained Whisper demo & deployment
assets/
 └── demo_screenshot.png
requirements.txt
README.md


---

## 🚀 Workflow

1. **Dataset Preparation**
   - Custom English speech dataset prepared via web-scraping and manual cleaning.  
   - Converted to `.wav` format with consistent sample rates.  
   - Transcripts formatted to Hugging Face Dataset format.

2. **Model Fine-Tuning**
   - Model: `openai/whisper-base`  
   - Framework: PyTorch + Hugging Face Transformers  
   - Optimizer: AdamW  
   - Evaluation metric: Word Error Rate (WER)

3. **Evaluation**
   - Baseline Whisper model tested on LibriSpeech subset  
   - Fine-tuned version tested on domain-specific dataset  
   - Accuracy improvement observed qualitatively (lower transcription errors, better accent handling)

4. **Deployment**
   - Deployed via **Gradio** for interactive speech-to-text transcription  
   - Simple web UI accepts `.wav` input or microphone input and displays real-time text output

---

## 🧪 Example Output

| Model | Sample Input | Predicted Text | WER |
|--------|---------------|----------------|------|
| Whisper Base | “hello everyone welcome…” | “hello everyone welcome…” | — |
| Fine-tuned | “my name is beva and i study ai” | “my name is beva and i study ai” | — |

---

## 🖼️ Deployment Preview

| Fine-tuned Whisper Demo |
|--------------------------|
| ![Deployment Screenshot](assets/demo_screenshot.png) |

*(Executed in Google Colab using Gradio — can be replicated easily.)*

---

## 🧰 Installation

```bash
# clone the repository
git clone https://github.com/<yourusername>/speech-to-text-finetuned-whisper.git
cd speech-to-text-finetuned-whisper

# install dependencies
pip install -r requirements.txt

💬 Future Work

Quantitative benchmarking on Common Voice dataset

Experimenting with Whisper Medium or Large for multilingual ASR

Exporting model as a FastAPI endpoint or Hugging Face Space

📄 Tech Stack
Category	Tools
Framework	PyTorch, Hugging Face Transformers
Deployment	Gradio
Audio Processing	Librosa, SoundFile, Torchaudio
Evaluation	JiWER, Evaluate
Environment	Google Colab (T4 GPU)
🧑‍💻 Author

Beva
B.Tech Computer Science | AI/ML Research Enthusiast
Passionate about Deep Learning, Speech Recognition, and Computer Vision

🌐 GitHub : https://github.com/DhairyaSavaliya

📧 Email : dhairyasavaliya73@gmail.com
