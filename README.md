# Klasifikasi Tingkat Kematangan Buah Pisang Menggunakan Ekstraksi Fitur GLCM dengan Perbandingan Metode KNN, SVM, dan Random Forest

## Nama Anggota

| NIM | Nama |
|-----|------|
| F1D02410014 | M. Arya Raka Bimo |
| F1D02410093 | Sabrina Salsabila |
| F1D02410103 | Andre Astamam |
| F1D02410117 | Lalu Ahmad Faiz Haqiqi |

---

# Project Overview

Pada project PCD ini, kami melakukan eksperimen klasifikasi **tingkat kematangan buah pisang** menggunakan pendekatan pengolahan citra digital. Tingkat kematangan pisang dibagi menjadi beberapa kelas berdasarkan perubahan warna, tekstur, dan kondisi permukaan kulit. Hal ini bertujuan untuk:
- Menguji kemampuan dalam mengimplementasikan teknik pengolahan citra digital untuk melakukan klasifikasi citra.
- Memilih tahapan preprocessing yang tepat sesuai dengan karakteristik visual buah pisang.

Eksperimen dilakukan sebanyak **3 kali percobaan** dengan penambahan preprocessing secara bertahap:

- **Percobaan Pertama** : Preprocessing 1, Preprocessing 2 
- **Percobaan Kedua** : Preprocessing 1, Preprocessing 2, Preprocessing 3 (tahap awal)
- **Percobaan Ketiga** : Preprocessing 1, Preprocessing 2, Preprocessing 3 (lengkap)

Dari setiap percobaan, akan dibandingkan akurasi masing-masing model: **KNN**, **SVM**, dan **Random Forest**.

---

# Import Library

Pada tahap ini dilakukan import seluruh library yang dibutuhkan selama proses klasifikasi, mulai dari library pengolahan citra, ekstraksi fitur, hingga pembuatan model machine learning.

---

# Load Data

Dataset berisi citra buah pisang yang dibagi ke dalam beberapa folder berdasarkan tingkat kematangannya (label). Pada tahap ini seluruh citra dibaca sekaligus beserta labelnya, kemudian diseragamkan ukurannya agar proses selanjutnya dapat berjalan konsisten.

🔗 **Link Dataset:** [Banana Ripeness Dataset — Kaggle](https://www.kaggle.com/datasets/xxxxxxx) *(ganti dengan link dataset kalian)*

---

# Data Understanding

Setelah data dimuat, dilakukan eksplorasi untuk memahami karakteristik dataset, meliputi:
- Jumlah total citra dan distribusi per kelas kematangan
- Kondisi visual citra (background, pencahayaan, noise)
- Sampel citra dari masing-masing kelas

Tahap ini penting untuk menentukan teknik preprocessing yang paling sesuai dengan kondisi data.

---

# Preprocessing

Pemilihan preprocessing didasarkan pada karakteristik visual citra pisang yang berubah seiring kematangan, seperti warna kulit, kemunculan bintik gelap, dan variasi pencahayaan. Berikut preprocessing yang digunakan:

**Preprocessing 1 : Grayscale + Ekualisasi Histogram + Normalisasi**

**Preprocessing 2 : Grayscale + Deteksi Tepi Prewitt + Threshold**

**Preprocessing 3 : Grayscale + Median Filter + Morfologi Opening**

---

# Feature Extraction

Ekstraksi fitur dilakukan menggunakan metode **Gray Level Co-occurrence Matrix (GLCM)** dengan konfigurasi. Fitur yang diekstrak dari setiap citra meliputi, Contrast, Dissimilarity, Homogeneity, Energy, Correlation, ASM, dan Entropy.
