# Capstone Project Modul 3 Telco Customer Churn Prediction
Perusahaan telekomunikasi berbasis langganan sangat bergantung pada kemampuan mempertahankan pelanggan untuk menjaga pendapatan secara berkelanjutan. Tantangan utama yang dihadapi adalah churn pelanggan, yaitu ketika pelanggan memutuskan untuk berhenti berlangganan, yang berdampak langsung pada penurunan pendapatan dan meningkatnya biaya akuisisi pelanggan baru.

Dengan semakin banyaknya data pelanggan yang tersedia seperti lama berlangganan, jenis kontrak, hingga layanan yang digunakan perusahaan memiliki peluang besar untuk menggunakan data tersebut sebagai dasar pengambilan keputusan yang lebih cerdas. Dengan pendekatan ini, tim manajemen dan pemasaran dapat menyusun strategi retensi yang lebih tepat sasaran untuk menurunkan churn dan meningkatkan kepuasan pelanggan.

## Pernyataan Masalah
Saat ini, perusahaan belum memiliki sistem prediktif yang mampu mengidentifikasi pelanggan yang berpotensi churn. Hal ini menyebabkan keterlambatan dalam melakukan tindakan pencegahan, sehingga peluang mempertahankan pelanggan hilang dan menyebabkan penurunan pendapatan serta pembengkakan biaya operasional.

## Dataset Description
Dataset yang digunakan adalah Telco Customer Churn yang berisi informasi profil pelanggan, termasuk:

- Tenure: Lama berlangganan dalam bulan

- InternetService, OnlineSecurity, TechSupport: Jenis layanan digital yang digunakan pelanggan

- Contract, PaperlessBilling: Tipe kontrak dan metode tagihan

- MonthlyCharges: Biaya bulanan yang dibayarkan pelanggan

- Churn: Status apakah pelanggan berhenti (Yes) atau tetap berlangganan (No)

## Data Preparation

- Data cleaning: menghapus duplikasi, menangani data kosong, dan konsistensi tipe data.

- Encoding: variabel kategorik dikonversi menjadi numerik (OneHot/Ordinal Encoding).

- Scaling: standardisasi nilai numerik agar setara skala.

- Feature engineering: menyederhanakan kategori layanan (misal: "No internet service" → "No").

## Modelling dan Evaluation
Beberapa algoritma klasifikasi yang digunakan:

- Logistic Regression

- Decision Tree

- Random Forest

## Evaluation Metrics
Metrik evaluasi yang digunakan:

- Accuracy

- Precision

- Recall (metrik utama karena penting untuk mendeteksi sebanyak mungkin pelanggan yang akan churn)

- F1-Score

- ROC AUC Score

## Hasil Akhir
Model terbaik yang diperoleh adalah Logistic Regression dengan hasil:

- Recall: 0.8213

- F1 Score: 0.6372

- Accuracy: 0.7505

Model ini dipilih karena memiliki nilai recall tertinggi dibandingkan model lain, sehingga paling optimal dalam mendeteksi pelanggan yang benar-benar akan melakukan churn, sesuai dengan fokus utama bisnis.

## Kesimpulan
Berdasarkan evaluasi tiga algoritma, Logistic Regression menunjukkan performa terbaik untuk memprediksi pelanggan yang berisiko churn, dengan recall 0.82 dan ROC AUC 0.85. Recall dipilih karena fokus bisnis adalah mengenali sebanyak mungkin pelanggan yang akan berhenti berlangganan.

Meskipun Random Forest mencatatkan accuracy dan precision yang lebih tinggi, nilai recall-nya jauh lebih rendah sehingga kurang cocok untuk kebutuhan ini.

Fitur yang paling berpengaruh menurut analisis koefisien adalah MonthlyCharges, Tenure, dan Contract, yang menunjukkan bahwa pelanggan dengan biaya tinggi, durasi langganan singkat, dan kontrak jangka pendek lebih berisiko churn.

## Rekomendasi 
