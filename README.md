
Klasifikasi URL Phishing Menggunakan Machine Learning

Study Group I-Smile — EDA to Machine Learning | Kelompok 5
Sebuah proyek machine learning yang berfokus pada analisis fitur terkait URL dan mengklasifikasikan URL sebagai situs web phishing atau sah (legitimate).

👥 Anggota Tim

Study Group I-Smile — Kelompok 5

Anggota	Tanggung Jawab
Raihan Athallah	Koordinasi proyek dan integrasi notebook
Ridho Darmawan	Pemeriksaan kualitas data dan preprocessing
Mohammad Harsa Avava	Pengembangan dan evaluasi model

Tanggung jawab ini bersifat sementara dan harus diperbarui untuk mencerminkan pembagian tugas yang disepakati serta kontribusi aktual tim.

📌 Tentang Proyek

Phishing adalah jenis serangan siber yang mencoba menipu pengguna agar mengunjungi situs web palsu atau membocorkan informasi sensitif. Menganalisis karakteristik URL dapat membantu mengidentifikasi pola yang terkait dengan situs web yang berpotensi berbahaya.
Proyek ini mengeksplorasi dataset URL phishing melalui Exploratory Data Analysis (EDA), pembersihan data, preprocessing, dan klasifikasi machine learning.
Tujuan utamanya adalah membangun dan mengevaluasi model klasifikasi yang dapat membedakan URL phishing dari URL yang sah menggunakan fitur dataset yang tersedia.

🎯 Tujuan Proyek

• Mengeksplorasi dataset dan mengidentifikasi pola yang terkait dengan URL phishing dan URL sah.
• Memeriksa kualitas data dan mempersiapkan fitur untuk machine learning.
• Membangun model klasifikasi menggunakan K-Nearest Neighbors (KNN).
• Mengevaluasi performa model menggunakan metrik klasifikasi yang sesuai.
• Menginterpretasikan hasil dan mendiskusikan keterbatasan model.

📊 Dataset

Proyek ini menggunakan PhiUSIIL Phishing URL Website Dataset dari UCI Machine Learning Repository.
• Sumber: UCI Machine Learning Repository — PhiUSIIL Phishing URL Website Dataset
• Ukuran Dataset: 235.795 instans
• Jumlah Kolom: 56, termasuk target dan kolom terkait pengidentifikasi (identifier)
• Jenis Masalah: Klasifikasi biner
• Variabel Target: label
	• 0 — Phishing
	• 1 — Sah (Legitimate)
Dataset ini berisi fitur-fitur terkait URL dan halaman web yang dapat diselidiki selama EDA dan persiapan fitur.
Kolom FILENAME merupakan bidang terkait pengidentifikasi dan akan ditinjau sebelum pemodelan. Keputusan pemilihan fitur dan preprocessing akan didokumentasikan di dalam notebook.

🧪 Metodologi

Proyek ini mengikuti tahapan-tahapan berikut:
1. Exploratory Data Analysis (EDA) — Memeriksa struktur dataset, statistik deskriptif, distribusi target, dan pola fitur yang relevan.
2. Pembersihan Data (Data Cleaning) — Memeriksa nilai yang hilang (missing values), catatan duplikat, tipe data, dan masalah kualitas data potensial lainnya.
3. Preprocessing — Mempersiapkan fitur yang cocok untuk pemodelan, termasuk menyandikan (encoding) atau memilih fitur jika diperlukan, serta menskalakan fitur numerik untuk KNN.
4. Pemisahan Data (Data Splitting) — Memisahkan data pelatihan dan pengujian untuk mengevaluasi generalisasi.
5. Pengembangan Model — Melatih pengklasifikasi KNN sebagai model utama dan mengevaluasi model tambahan jika disertakan dalam eksperimen.
6. Evaluasi Model — Menilai performa menggunakan akurasi, presisi, recall, matriks kebingungan (confusion matrix), dan validasi silang (cross-validation) jika memungkinkan.
7. Kesimpulan — Merangkum temuan, performa model, dan keterbatasan.
Semua keputusan pemilihan fitur dan preprocessing akan didokumentasikan untuk mengurangi risiko kebocoran data (data leakage).

🤖 Machine Learning

Model utamanya adalah K-Nearest Neighbors (KNN).
Skalasi fitur (feature scaling) sangat penting untuk KNN karena algoritma ini mengandalkan jarak antar titik data. Pemilihan model dan penyetelan parameter (parameter tuning) akan dilakukan menggunakan data pelatihan, dengan evaluasi akhir pada kumpulan data pengujian yang ditahan (held-out test set).
