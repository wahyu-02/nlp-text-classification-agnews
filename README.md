# NLP Text Classification: Yahoo Answers

## Deskripsi Proyek
Proyek ini mengimplementasikan tiga metode klasifikasi teks menggunakan **PyTorch**:
- **FastText** (Mean Pooling)
- **Transformer** (Self-Attention Mechanism)
- **LSTM** (Long Short-Term Memory)

Dataset yang digunakan adalah **Yahoo Answers**, dengan representasi kata menggunakan **GloVe Pre-trained Embeddings**.

## Struktur Folder
- `data/` : Dataset (train.csv, test.csv)
- `models/` : Implementasi FastText, Transformer, dan LSTM.
- `results/` : Hasil evaluasi seperti confusion matrix dan learning curve.
- `scripts/` : Skrip utama untuk training dan evaluasi.
- `requirements.txt` : Library yang diperlukan.

## Instalasi
1. Clone repository:
