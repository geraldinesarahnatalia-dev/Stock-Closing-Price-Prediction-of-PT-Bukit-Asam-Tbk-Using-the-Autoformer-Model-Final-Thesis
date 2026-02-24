# Prediksi Harga Penutupan Saham PT Bukit Asam Tbk Menggunakan Model Autoformer

Repository ini berisi implementasi penelitian tugas akhir yang berjudul:

**“Prediksi Harga Penutupan Saham PT Bukit Asam Tbk Menggunakan Model Autoformer”**

Penelitian ini bertujuan untuk menganalisis performa model Autoformer dalam memprediksi harga penutupan saham PT Bukit Asam Tbk (PTBA) menggunakan data historis time series periode 2020–2025.

---

## 📌 Latar Belakang

Pergerakan harga saham yang fluktuatif menjadikan prediksi harga sebagai aspek penting dalam pengambilan keputusan investasi. PT Bukit Asam Tbk (PTBA) merupakan salah satu perusahaan tambang batu bara terbesar di Indonesia yang memiliki volatilitas harga cukup tinggi dalam beberapa tahun terakhir.

Perkembangan teknologi kecerdasan buatan, khususnya deep learning, memungkinkan pendekatan prediksi yang lebih kompleks dibandingkan metode tradisional. Model berbasis Transformer, terutama Autoformer, memiliki keunggulan dalam menangkap pola jangka panjang melalui mekanisme **Auto-Correlation** dan **Series Decomposition**, sehingga lebih efektif untuk data time series.

---

## 🎯 Tujuan Penelitian

Tujuan penelitian ini adalah menganalisis kinerja model Autoformer dalam memprediksi harga penutupan saham PT Bukit Asam Tbk (PTBA) dengan evaluasi menggunakan:

* Mean Squared Error (MSE) sebagai fungsi loss
* Mean Absolute Percentage Error (MAPE) sebagai metrik evaluasi

---

## 📊 Dataset

Dataset yang digunakan berupa data harga penutupan saham harian PT Bukit Asam Tbk (PTBA) pada periode:

**2 Januari 2020 – 2 Januari 2025**

Penelitian ini hanya menggunakan satu variabel yaitu **harga penutupan (closing price)** tanpa variabel tambahan seperti:

* Harga pembukaan
* Harga tertinggi
* Harga terendah
* Volume perdagangan
* Indikator teknikal
* Faktor makroekonomi

Pembatasan ini dilakukan untuk fokus pada evaluasi kemampuan Autoformer dalam memodelkan satu variabel time series.

---

## 🧠 Model yang Digunakan

Model yang digunakan adalah **Autoformer**, yaitu arsitektur deep learning berbasis Transformer yang dirancang khusus untuk time series forecasting dengan dua komponen utama:

### 1. Series Decomposition

Memisahkan data menjadi:

* Komponen tren (trend)
* Komponen musiman (seasonal)

### 2. Auto-Correlation Mechanism

Mendeteksi pola berulang dalam data secara efisien menggunakan pendekatan berbasis frekuensi (FFT).

Arsitektur model terdiri dari:

* Embedding Layer
* Encoder
* Decoder
* Series Decomposition Blocks
* Feed Forward Network

---

## ⚙️ Metodologi Penelitian

Tahapan penelitian meliputi:

1. Preprocessing data
2. Normalisasi menggunakan StandardScaler
3. Pembagian data (training, validation, testing)
4. Perancangan arsitektur Autoformer
5. Eksperimen konfigurasi hyperparameter
6. Pelatihan model menggunakan MSE
7. Pemilihan model terbaik
8. Denormalisasi hasil prediksi
9. Evaluasi menggunakan MAPE
10. Analisis hasil prediksi

Sebanyak **8 konfigurasi model** diuji untuk memperoleh performa terbaik.

---

## 🏆 Model Terbaik

Model terbaik diperoleh pada **Model 3** dengan parameter:

* seq_len = 96
* label_len = 60
* pred_len = 24

---

## 📈 Hasil Penelitian

Performa terbaik model:

* Validation Loss: **0,57**
* MAPE: **3,02%**

Model mampu mengikuti arah pergerakan harga saham secara umum dan cukup baik dalam menangkap tren jangka pendek. Namun masih terdapat deviasi pada beberapa periode akibat volatilitas pasar dan karakteristik data yang tidak sepenuhnya periodik.

---

## 🚀 Cara Menjalankan

1. Buka file notebook berikut menggunakan:

   * Jupyter Notebook
   * Google Colab
   * VS Code (Python Extension)

```
Code_TA_Sarah_Natalia_Geraldine_121450022.ipynb
```

2. Jalankan seluruh cell secara berurutan untuk melihat proses:

   * Preprocessing
   * Training model
   * Evaluasi
   * Prediksi

---

## 📂 Struktur Repository

```
│── Code_TA_Sarah_Natalia_Geraldine_121450022.ipynb
│── README.md
```

---

## 👩‍💻 Penulis

**Sarah Natalia Geraldine**
NIM: 121450022
Program Studi Sains Data
Fakultas Sains
Institut Teknologi Sumatera (ITERA)
2025

---

## 📜 Lisensi

Project ini dibuat untuk kepentingan akademik dan penelitian.
