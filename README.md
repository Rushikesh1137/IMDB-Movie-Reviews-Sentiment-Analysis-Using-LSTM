# IMDB-Movie-Reviews-Sentiment-Analysis-Using-LSTM


This project is a **natural language processing (NLP) application that performs sentiment analysis on movie reviews. It uses a Long Short-Term Memory (LSTM) neural network built with Keras to classify whether a review is **positive or **negative. The model is served using FastAPI for backend API services and Gradio for an interactive web interface.

## 🔧  Tech Stack

**🧠 Deep Learning**: LSTM (Long Short-Term Memory) using TensorFlow/Keras

**⚙️ Backend API**: FastAPI

**🌐 UI Interface**: Gradio

**📦 Model Format**: .h5 (Keras saved model)

**🚀 Deployment Options**: Render, local Uvicorn, or Gradio public share
<img width="1460" height="238" alt="Screenshot 2025-08-02 at 11 14 29 PM" src="https://github.com/user-attachments/assets/d032b1d8-8840-4bd0-9193-1bc29b063056" />
                           <img width="768" height="79" alt="Screenshot 2025-08-02 at 11 14 43 PM" src="https://github.com/user-attachments/assets/21e0bf7c-bc6b-4412-8588-b12ff8dfbdb7" />




## 🔁 Model Training Overview
The model was built using an LSTM architecture on a dataset of IMDB reviews:

**Tokenize**r: Keras tokenizer with num_words=10000

**Embedding Layer**: Embedding + LSTM

**Loss**: Binary crossentropy

**Activation**: Sigmoid for binary classification

**Trained** model is saved as sentiment_model.h5.


## Why LSTM?
Traditional RNNs suffer from vanishing gradient problems, making them ineffective for learning long-term dependencies in text.

LSTMs are designed to remember information for long periods using gates that regulate the flow of information.

This makes them well-suited for modeling sequential data like text, where the order and context of words matter.

<img width="888" height="484" alt="image" src="https://github.com/user-attachments/assets/6ad924cf-ec1f-41a9-b9c9-43249da28b55" />

## 🧹 Data Preprocessing
The input data (e.g., IMDB reviews) undergoes several preprocessing steps before training:

**Text Tokenization:**

Converts words to integer sequences using Tokenizer(num_words=10000)

Rare words are treated as <OOV> (out-of-vocabulary)

**Padding:**

All sequences are padded or truncated to a uniform length (e.g., 200) using pad_sequences()

**Train-Test Split:**

Typically 80/20 split is used.

**Label Encoding:**

Reviews are labeled as 1 (positive) or 0 (negative)

## 🔬 Training Details

**Loss Function**: binary_crossentropy – suitable for binary classification

**Optimizer**: adam – adaptive learning rate for better convergence

**Metrics**: accuracy

**Epochs**: 5–10 (depending on model performance and dataset size)

**Batch Size**: 32 or 64

## 📝 Future Improvements
🔒 Add authentication to API

📊 Visualize predictions using charts

🧠 Replace LSTM with Transformer (e.g., BERT)

💾 Add support to save/load Tokenizer (tokenizer.json)

📦 Add Docker support


