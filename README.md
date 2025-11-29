# Cuisine-recommender
It is a cuisine recommender based on accent identified from english speech
# 🎙️ Accent-Based Cuisine Recommender  
### Predict an Indian regional accent from an audio sample and get matching cuisine recommendations.

🔗 **Live Working Application:**  
https://krishnendua-cuisine-recommender.hf.space/?__theme=system&deep_link=X8s0LJ2v9OE  

---

## 📌 Project Overview  
The **Accent-Based Cuisine Recommender** is an AI system that predicts a user’s **Indian regional accent** using speech audio and then recommends popular cuisine from that region.

The model uses:
- **MFCC features**  
- **HuBERT (facebook/hubert-base-ls960) embeddings**  
- **Support Vector Classifier (SVC)** for classification  

The final project is deployed using **Gradio** on **Hugging Face Spaces**.

---

## 🧠 Features  
- Upload or record speech audio  
- Real-time accent detection  
- Cuisine recommendations based on predicted region  
- Clean and interactive web interface  
- High accuracy (100% on test set)  
- Works with `.wav`, `.mp3`, etc.  

---

## 🗂️ Dataset  
The dataset used contains **983 labelled audio files**, covering **six major Indian accents**:

| Accent      | Region           |
|-------------|------------------|
| Andhra      | Andhra Pradesh   |
| Gujrat      | Gujarat          |
| Jharkhand   | Jharkhand        |
| Karnataka   | Karnataka        |
| Kerala      | Kerala           |
| Tamil       | Tamil Nadu       |

➡️ The dataset structure and accent categories were inspired by:  
**DarshanaS/IndicAccentDb**

---

## 🧩 Models Used  

### **1️⃣ MFCC (Mel-Frequency Cepstral Coefficients)**  
- Extracted using `librosa`  
- 20-dimensional vector per audio  
- Captures pronunciation, tone, and accent patterns  

### **2️⃣ HuBERT (facebook/hubert-base-ls960)**  
- Pretrained transformer model  
- Extracts deep contextual speech embeddings  
- Captures accent-specific articulation and rhythm  

### **3️⃣ Support Vector Classifier (SVC)**  
- Kernel: **RBF**  
- Trained on fused MFCC + HuBERT embeddings  
- Achieved **100% accuracy** on test data  

---

## 🔧 How to Run the Project Locally  

### **1. Clone the Repository**
```bash
git clone https://github.com/your-username/accent-cuisine-recommender.git
cd accent-cuisine-recommender
