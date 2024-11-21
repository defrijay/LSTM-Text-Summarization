# Text Summarization using LSTM

Proyek ini mengimplementasikan model **Long Short-Term Memory** (LSTM) untuk menghasilkan ringkasan teks dari artikel berita. Model ini memanfaatkan teknik prapemrosesan data, augmentasi teks, serta pembelajaran mendalam untuk merangkum teks secara otomatis.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
- [Installation](#installation)
- [Project Creator](#project-creator)

## Overview

Ringkasan teks otomatis (text summarization) adalah teknik **Natural Language Processing** (NLP) untuk membuat versi pendek dari suatu teks sambil mempertahankan makna utamanya. Proyek ini menggunakan model **LSTM** untuk menghasilkan ringkasan dari artikel berita, khususnya dalam bahasa Indonesia.

## Features

- **Data Preprocessing**: Membersihkan teks, mengubah menjadi sequences, serta melakukan padding untuk memastikan panjang konsisten.
- **Tokenization & Vocabulary**: Menggunakan tokenizer untuk mengubah kata menjadi angka, dengan ukuran vocabulary dinamis.
- **Augmentasi Data**: Menambah variasi data dengan teknik sinonim dan back-translation.
- **Training & Evaluation**: Melatih model LSTM dengan callback seperti **ReduceLROnPlateau** dan **EarlyStopping**.
- **WordCloud & Visualizations**: Menyediakan representasi visual dari distribusi kata.
- **Prediction Function**: Menghasilkan ringkasan otomatis dari input teks pengguna.

## Dataset

Dataset **Liputan6** adalah kumpulan data berskala besar yang berisi pasangan dokumen dan ringkasan artikel berita dalam Bahasa Indonesia. Dataset ini dirancang untuk mendukung model summarization baik dalam bentuk ekstraktif maupun abstraktif.

### Detail Dataset

- **Jenis Ringkasan**: Ekstraktif dan Abstraktif.
- **Bahasa**: Indonesia.
- **Ukuran Dataset**: 16.5 MB.
- **Tugas yang Didukung**: Text summarization.
- **Referensi**: [arxiv:2011.00679](https://arxiv.org/abs/2011.00679).

### Struktur Data

Dataset memiliki beberapa kolom utama:
- **id**: ID unik artikel.
- **url**: URL artikel asli.
- **clean_article**: Artikel yang telah dibersihkan.
- **clean_summary**: Ringkasan abstraktif artikel.

Contoh data:

```json
{
  "id": "26408",
  "url": "https://www.liputan6.com/news/read/26408/pbb-siap-membantu-penyelesaian-konflik-ambon",
  "clean_article": "Liputan6.com, Ambon: Partai Bulan Bintang wilayah Maluku bertekad membantu pemerintah menyelesaikan konflik di provinsi tersebut...",
  "clean_summary": "Konflik Ambon telah berlangsung selama tiga tahun. Partai Bulan Bintang wilayah Maluku siap membantu pemerintah menyelesaikan kasus di provinsi tersebut.",
  "extractive_summary": "Liputan6.com, Ambon: Partai Bulan Bintang wilayah Maluku bertekad membantu pemerintah menyelesaikan konflik di provinsi tersebut."
}
```

### Instalasi

```python
pip install numpy pandas matplotlib seaborn nltk tensorflow googletrans wordcloud scikit-learn

```

