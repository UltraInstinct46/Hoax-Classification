# Klasifikasi Berita Palsu (Fake News) pada Platform X Menggunakan Algoritma SVM

Repositori ini berisi *source code* dan visualisasi data untuk penelitian skripsi: **"Klasifikasi Berita Palsu pada Platform X Menggunakan Algoritma SVM"**. Penelitian ini berfokus pada pengembangan sistem deteksi otomatis untuk menyaring disinformasi menggunakan pendekatan *Natural Language Processing* (NLP) dan algoritma *Machine Learning*.

## 📌 Deskripsi Proyek
Penyebaran informasi palsu di media sosial, khususnya Platform X (Twitter), terjadi dengan sangat cepat. Proyek ini bertujuan untuk mengklasifikasikan teks berita ke dalam dua kategori: **Valid (1)** dan **Palsu (0)**. 

Model ini dievaluasi menggunakan *Fake and Real News Dataset* dan berhasil mencapai tingkat akurasi sebesar **99%** dengan memadukan ekstraksi fitur berdimensi optimal dan penalti ketat pada *hyperplane* SVM.

## ⚙️ Metodologi dan Alur Kerja
1. **Pra-pemrosesan Teks (NLP):** * *Case folding*, pembersihan URL/tanda baca (*cleansing*), tokenisasi, *stopword removal*, dan *lemmatization*.
2. **Ekstraksi Fitur:** * Menggunakan pembobotan `TfidfVectorizer` dengan batasan `max_features=2000` untuk mencegah *curse of dimensionality*.
3. **Pemodelan Machine Learning:** * **Algoritma:** *Support Vector Machine* (SVM)
   * **Optimasi:** Penyetelan *hyperparameter* menggunakan `GridSearchCV` (Kombinasi terbaik: `Kernel = RBF`, `C = 10`, `gamma = scale`).
4. **Evaluasi:** * Diukur menggunakan *Confusion Matrix*, Akurasi, Presisi, *Recall*, dan *F1-Score*.

## 📁 Struktur Repositori
* `Hoax Classification.ipynb` : *Jupyter Notebook* utama yang memuat seluruh alur kode dari *load dataset* hingga evaluasi model.
* `distribusi_panjang_teks.png` : Visualisasi perbandingan jumlah kata antara berita palsu dan berita valid.
* `distribution_bigram.png` : Grafik frekuensi kemunculan kombinasi dua kata (*Bigram*) tertinggi pada setiap kelas.
* `distribution_trigram.png` : Grafik frekuensi kemunculan kombinasi tiga kata (*Trigram*) tertinggi pada setiap kelas.
* `wordcloud.png` : Representasi visual dari kata-kata yang paling dominan di korpus teks.

## 🛠️ Teknologi yang Digunakan
* **Bahasa:** Python 3
* **Pustaka Utama:** `Scikit-Learn`, `NLTK`, `Pandas`, `NumPy`
* **Visualisasi:** `Matplotlib`, `Seaborn`, `WordCloud`

---
**Penulis:** Restuaji Eliansyah (Universitas Trilogi)