# 🈂️ English to Urdu Neural Machine Translation 🇬🇧➡️🇵🇰  
A sequence-to-sequence (Seq2Seq) neural translation model using a **Bidirectional LSTM** encoder and decoder built with TensorFlow/Keras. This project demonstrates a simple yet effective approach to translating English sentences into Urdu.

---

## 🚀 Overview  
This project implements a full NMT (Neural Machine Translation) pipeline:
- Preprocessing and cleaning parallel corpora (English–Urdu)  
- Tokenization and padding  
- Sequence-to-sequence model with a Bidirectional LSTM encoder  
- LSTM decoder with a dense output layer  
- Evaluation with BLEU score and qualitative outputs

---

## 🧠 Model Architecture  
**Encoder**: Embedding → Bidirectional LSTM  
**Decoder**: Embedding → LSTM → Dense (Softmax)  

The model learns to generate Urdu translations of English sentences by encoding context with BiLSTM and decoding one word at a time.

---

## 📁 Dataset  
The dataset consists of parallel English–Urdu sentence pairs.  
Preprocessing steps include:
- Lowercasing and stripping whitespace  
- Adding `<sos>` (start of sentence) and `<eos>` (end of sentence) tokens  
- Padding sequences to a uniform length

---

## 🛠️ Requirements  
Install required packages:  
`pip install numpy pandas matplotlib tensorflow nltk`

---

## 🏃‍♂️ Training  
The model is trained using teacher forcing with categorical crossentropy loss.  
Example training snippet:

```python
model.fit(
    [encoder_input_data, decoder_input_data],
    decoder_target_data,
    batch_size=64,
    epochs=100,
    validation_split=0.2
)
```

## 📊 Evaluation  
Evaluation is performed using BLEU scores and example translations.  

**Sample Output:**  
**English:** How are you?  
**Predicted Urdu:** آپ کیسے ہیں؟

---

## ✅ To Do  
- [x] Build BiLSTM encoder-decoder  
- [x] Preprocess parallel corpus  
- [x] Evaluate with BLEU  
- [ ] Add attention mechanism  
- [ ] Use larger dataset  
- [ ] Explore Transformer models

---

## 🤝 Contributing  
Feel free to fork this repo and submit pull requests.  
For major changes, open an issue first to discuss what you would like to change.

---

## 📜 License  
This project is licensed under the **MIT License** – see the `LICENSE` file for details.

---

## 🙋 Contact  
**Developed by:** Omer Nasir & Abdul Ahad  
Reach out via GitHub or LinkedIn for collaboration or questions.
