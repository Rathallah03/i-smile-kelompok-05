# Klasifikasi URL Phishing Menggunakan Machine Learning

**Study Group I-Smile — EDA to Machine Learning**

Proyek ini merupakan bagian dari kegiatan Study Group I-Smile yang berfokus pada *Exploratory Data Analysis* (EDA), *data cleaning*, dan penerapan machine learning untuk klasifikasi URL phishing.

## 👥 Kelompok 05

| Nama | Tanggung Jawab |
|---|---|
| Raihan Athallah | Koordinasi proyek, persiapan repository dan notebook, integrasi notebook, EDA, pemodelan KNN, cross-validation, tuning hyperparameter, evaluasi dan pemeriksaan hasil akhir. |
| Ridho Darmawan | Data cleaning, pemeriksaan kualitas data, audit dan seleksi fitur, serta kolaborasi dalam penyusunan slide presentasi. |
| Mohammad Harsa Avava | Dukungan koordinasi dan bantuan *backup*. |

**Asisten Pendamping:** [@fxrdhan](https://github.com/fxrdhan)

## 🔗 Tautan Proyek

- **Repository GitHub:** [i-smile-kelompok-05](https://github.com/Rathallah03/i-smile-kelompok-05)
- **Notebook Google Colab:** [Klasifikasi URL Phishing](https://colab.research.google.com/drive/1F8ayecWDf7akkDR-imaB0wjH6ZyfaB21)
- **Dataset resmi:** [PhiUSIIL Phishing URL Website Dataset — UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/967/phiusiil+phishing+url+website+dataset)

## 📌 Latar Belakang

Phishing merupakan bentuk serangan cyber yang memanfaatkan tautan atau situs web palsu untuk menipu pengguna dan berpotensi mencuri informasi sensitif. Karakteristik URL dan fitur terkait situs web dapat dianalisis untuk menemukan pola yang membedakan URL phishing dari URL legitimate.

Proyek ini menerapkan pendekatan klasifikasi biner untuk mempelajari karakteristik tersebut menggunakan dataset publik dan algoritma machine learning.

## 🎯 Tujuan Proyek

- Melakukan EDA untuk memahami struktur, distribusi, dan pola dalam dataset.
- Memeriksa kualitas data dan melakukan seleksi fitur untuk pemodelan.
- Membangun model klasifikasi menggunakan **K-Nearest Neighbors (KNN)**.
- Mengevaluasi model menggunakan metrik klasifikasi dan *cross-validation*.
- Menginterpretasikan hasil serta menjelaskan keterbatasan eksperimen.

## 📊 Dataset

Proyek ini menggunakan **PhiUSIIL Phishing URL Website Dataset** dari UCI Machine Learning Repository.

| Informasi | Keterangan |
|---|---|
| Sumber | UCI Machine Learning Repository |
| Jumlah baris awal | 235.795 |
| Jumlah kolom awal | 56 |
| Jenis masalah | Klasifikasi biner |
| Kolom target | `label` |
| Label 0 | Phishing |
| Label 1 | Legitimate |

Dataset mencakup fitur numerik dan informasi terkait URL serta karakteristik situs web. Sebelum pemodelan, fitur ditinjau dan dipilih berdasarkan kebutuhan analisis.

## 🧪 Metodologi

Proyek dilakukan melalui tahapan berikut:

1. **Exploratory Data Analysis (EDA):** pemeriksaan struktur data, statistik deskriptif, distribusi target, dan visualisasi fitur.
2. **Data Cleaning:** pemeriksaan missing values, URL berulang, duplikasi, dan kandidat outlier.
3. **Seleksi Fitur:** peninjauan kolom identifikasi, kolom nonnumerik, serta fitur yang tidak digunakan dalam model akhir.
4. **Preprocessing:** penyiapan fitur dan penerapan `StandardScaler`.
5. **Pembagian Data:** pemisahan data menjadi training set dan test set dengan rasio 80:20 serta `random_state=42` dan `stratify=y`.
6. **Pemodelan:** penggunaan KNN dengan scaling dalam `Pipeline`.
7. **Evaluasi dan Tuning:** penggunaan Stratified 5-Fold Cross-Validation pada data training serta pengujian kandidat nilai `k`.
8. **Evaluasi Akhir:** pengukuran performa model terpilih pada test set.
9. **Kesimpulan:** interpretasi hasil dan pembahasan keterbatasan model.

## 🤖 Model dan Hasil Evaluasi

Model akhir yang dipilih adalah **K-Nearest Neighbors (KNN) dengan `k = 3`**, berdasarkan hasil perbandingan kandidat hyperparameter pada subset training.

| Metrik | Hasil |
|---|---:|
| Jumlah fitur pada model final | 48 |
| Mean CV accuracy untuk `k = 3` | 99,025% |
| Test accuracy | 99,26% |
| Precision kelas phishing | 99,23% |
| Recall kelas phishing | 99,05% |

Berdasarkan confusion matrix pada test set:

- **19.912** URL phishing diklasifikasikan dengan benar.
- **192** URL phishing salah diklasifikasikan sebagai legitimate.
- **154** URL legitimate salah diklasifikasikan sebagai phishing.
- **26.816** URL legitimate diklasifikasikan dengan benar.

Recall kelas phishing penting diperhatikan karena phishing yang salah diklasifikasikan sebagai legitimate dapat lolos dari proses deteksi.

## ⚠️ Keterbatasan

Hasil evaluasi menunjukkan performa tinggi pada test set yang digunakan, tetapi tidak menjamin model akan memiliki performa serupa pada seluruh URL baru di dunia nyata.

Beberapa keterbatasan eksperimen:

- Tuning hyperparameter hanya membandingkan kandidat `k = 3`, `k = 5`, dan `k = 7` pada subset training.
- Validasi eksternal menggunakan dataset yang sepenuhnya independen belum dilakukan.
- Hasil evaluasi bergantung pada dataset, fitur yang dipilih, dan skema pembagian data.
- Potensi kebocoran informasi atau kemiripan antarobservasi perlu tetap dipertimbangkan ketika menafsirkan hasil.

## 📁 Struktur Repository

```text
i-smile-kelompok-05/
├── README.md
├── .gitignore
└── dataset/
    └── phishing_url_dataset.csv
```

## 📚 Referensi

- UCI Machine Learning Repository. [PhiUSIIL Phishing URL Website Dataset](https://archive.ics.uci.edu/dataset/967/phiusiil+phishing+url+website+dataset).
- Dokumentasi scikit-learn. [K-Nearest Neighbors](https://scikit-learn.org/stable/modules/neighbors.html).
- Dokumentasi scikit-learn. [Model Selection and Cross-Validation](https://scikit-learn.org/stable/modules/cross_validation.html).

---

*Proyek Study Group I-Smile — EDA to Machine Learning, Kelompok 05.*
