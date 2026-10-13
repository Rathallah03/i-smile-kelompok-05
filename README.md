# Klasifikasi URL Phishing Menggunakan Machine Learning

**Study Group I-Smile — EDA to Machine Learning | Kelompok 5**

## 👥 Tim Proyek

### Anggota Kelompok

| Nama | Tanggung Jawab |
|---|---|
| Raihan Athallah | Koordinasi proyek dan integrasi notebook |
| Ridho Darmawan | |
| Mohammad Harsa Avava | |

### Asisten Pendamping

| Peran | Profil GitHub |
|---|---|
| Asisten Pendamping Kelompok 5 | [@fxrdhan](https://github.com/fxrdhan) |

## 🔗 Tautan Proyek

- **Notebook Google Colab:** [Buka Notebook Proyek](https://colab.research.google.com/drive/1F8ayecWDf7akkDR-imaB0wjH6ZyfaB21)
- **Repository GitHub:** [i-smile-kelompok-05](https://github.com/Rathallah03/i-smile-kelompok-05)
- **Dataset:** [PhiUSIIL Phishing URL Website Dataset — UCI](https://archive.ics.uci.edu/dataset/967/phiusiil+phishing+url+website+dataset)

## 📌 Tentang Proyek

Phishing merupakan salah satu bentuk serangan cyber yang berupaya menipu pengguna agar mengunjungi situs web palsu atau memberikan informasi sensitif. Karakteristik URL dan halaman web dapat dianalisis untuk mempelajari pola yang berkaitan dengan situs phishing.

Proyek ini berfokus pada analisis karakteristik URL melalui **Exploratory Data Analysis (EDA)** serta penerapan machine learning untuk mengklasifikasikan URL ke dalam dua kategori, yaitu phishing dan situs yang sah (*legitimate*).

Proyek ini merupakan bagian dari kegiatan Study Group I-Smile dengan topik EDA to Machine Learning.

## 🎯 Tujuan Proyek

- Mengeksplorasi dataset dan mengidentifikasi pola yang berkaitan dengan URL phishing dan legitimate.
- Memeriksa kualitas data serta mempersiapkan fitur untuk pemodelan.
- Membangun model klasifikasi menggunakan **K-Nearest Neighbors (KNN)**.
- Mengevaluasi performa model menggunakan metrik klasifikasi yang sesuai.
- Menginterpretasikan hasil eksperimen dan membahas keterbatasan model.

## 📊 Dataset

Proyek ini menggunakan **PhiUSIIL Phishing URL Website Dataset** dari UCI Machine Learning Repository.

- **Sumber:** [UCI Machine Learning Repository — PhiUSIIL Phishing URL Website Dataset](https://archive.ics.uci.edu/dataset/967/phiusiil+phishing+url+website+dataset)
- **Jumlah data:** 235.795 baris
- **Jumlah kolom:** 56, termasuk kolom target dan kolom terkait identifikasi
- **Jenis masalah:** Klasifikasi biner (*binary classification*)
- **Variabel target:** `label`

Keterangan label:

- `0` — Phishing
- `1` — Legitimate (situs yang sah)

Dataset ini berisi berbagai fitur terkait struktur URL dan karakteristik halaman web. Fitur-fitur tersebut akan dieksplorasi untuk mengetahui pola yang dapat membantu proses klasifikasi.

Kolom `FILENAME` akan ditinjau sebelum pemodelan karena berkaitan dengan identifikasi data. Pemilihan fitur dan keputusan preprocessing akan dijelaskan lebih lanjut dalam notebook.

## 🧪 Metodologi

Proyek ini direncanakan melalui beberapa tahapan berikut:

1. **Exploratory Data Analysis (EDA)** — Memeriksa struktur dataset, statistik deskriptif, distribusi target, dan pola pada fitur yang relevan.
2. **Data Cleaning** — Memeriksa nilai yang hilang, data duplikat, tipe data, dan potensi masalah kualitas data lainnya.
3. **Preprocessing** — Mempersiapkan fitur untuk pemodelan, termasuk pemilihan fitur, encoding jika diperlukan, dan scaling untuk KNN.
4. **Pembagian Data** — Memisahkan data menjadi data latih (*training set*) dan data uji (*testing set*).
5. **Pengembangan Model** — Membangun model KNN sebagai model utama dan model pembanding apabila digunakan dalam eksperimen.
6. **Evaluasi Model** — Mengukur performa menggunakan accuracy, precision, recall, confusion matrix, serta cross-validation sesuai kebutuhan.
7. **Kesimpulan** — Merangkum hasil analisis, performa model, dan keterbatasan penelitian.

Setiap keputusan terkait pemilihan fitur dan preprocessing akan didokumentasikan untuk membantu mengurangi risiko *data leakage*.

## 🤖 Model Machine Learning

Model utama yang digunakan dalam proyek ini adalah **K-Nearest Neighbors (KNN)**.

KNN mengklasifikasikan data berdasarkan kedekatannya dengan sejumlah tetangga terdekat. Oleh karena itu, scaling fitur menjadi salah satu tahap penting agar perbedaan skala antarfitur tidak mendominasi perhitungan jarak.

Pemilihan model dan penyesuaian parameter akan dilakukan menggunakan data latih, sedangkan data uji akan digunakan untuk evaluasi akhir.

Model tambahan dapat digunakan sebagai pembanding apabila benar-benar diterapkan dan dievaluasi dalam notebook.

## 📈 Hasil dan Evaluasi

-------
