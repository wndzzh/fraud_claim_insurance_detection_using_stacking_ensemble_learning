# Insurance Automobile Claim Fraud Detection  
## Using Stacking Ensemble Learning

## 🔍 Overview
Proyek ini bertujuan untuk mendeteksi **penipuan (fraud)** pada klaim asuransi kendaraan bermotor menggunakan pendekatan **Stacking Ensemble Learning**.  
Pendekatan ini mengombinasikan model non-linear dan linear untuk meningkatkan performa klasifikasi pada data yang **tidak seimbang (imbalanced)**.

Model akhir dibangun dengan:
- **XGBoost** sebagai *base learner* non-linear
- **Lasso Logistic Regression** sebagai *base learner* linear dengan seleksi fitur otomatis
- **Logistic Regression** sebagai *meta-learner*

Proyek ini dikembangkan sebagai bagian dari **Tugas Akhir (Skripsi)** Program Studi **Sains Data**.

---

## 📊 Dataset
- **Jenis data:** Klaim asuransi kendaraan bermotor  
- **Target:** Indikasi fraud (0 = Non-Fraud, 1 = Fraud)  
- **Karakteristik data:**
  - Campuran fitur numerik dan kategorikal
  - Distribusi kelas tidak seimbang (fraud rate rendah)

> Dataset telah melalui proses *data cleaning*, *feature engineering*, dan *preprocessing* berbasis pipeline.

---

## 🛠️ Metode & Tools

### 🔹 Metode
- Exploratory Data Analysis (EDA)
- Feature Engineering berbasis domain asuransi
- Pipeline Preprocessing (Imputasi, Encoding, Scaling)
- Train–Test Split
- Hyperparameter Optimization (Optuna)
- Stacking Ensemble Learning
- Evaluasi Model Klasifikasi

### 🔹 Algoritma
- XGBoost
- Lasso Logistic Regression (L1 Regularization)
- Ridge Logistic Regression (Meta-learner)

### 🔹 Evaluasi
- Confusion Matrix
- Precision, Recall, F1-Score, Akurasi
- ROC-AUC

---

## 📁 Struktur Proyek

```

.
├── 01_eda.ipynb
├── 02_feature_engineering.ipynb
├── 03_preprocessing_0.ipynb
├── 04_split_data.ipynb
├── 05_preprocessing_1.ipynb
├── 06_XGBoost.ipynb
├── 07_Lasso_Logistic.ipynb
├── 08_Stacking_Ensemble.ipynb
│
├── train_test_data.pkl
├── preprocessing_pipeline.pkl
├── feature_names.pkl
└── best_params.pkl

```

---

## 🔬 Hasil Utama
- Model **stacking ensemble** menunjukkan performa lebih stabil dibandingkan model individual.
- **XGBoost** efektif menangkap pola non-linear pada data klaim.
- **Lasso Logistic Regression** berhasil mengeliminasi fitur tidak relevan melalui regularisasi L1.
- Pendekatan pipeline berhasil mencegah **data leakage** selama proses pelatihan dan validasi.

> Nilai metrik evaluasi dapat bervariasi tergantung *random seed* dan versi library.

---

## ▶️ Cara Menjalankan
1. Jalankan notebook secara **berurutan** dari `01_eda.ipynb` hingga `08_Stacking_Ensemble.ipynb`
2. Pastikan file `.pkl` berhasil dibuat sebelum melanjutkan ke tahap berikutnya
3. Seluruh eksperimen dilakukan menggunakan Python 3.8+

---

## 👤 Author
**Wanda Azizah**  
Undergraduate Student – Data Science  
Telkom University

---

## 📄 License
Proyek ini dibuat untuk keperluan akademik (Tugas Akhir / Skripsi).  
Kode dapat digunakan sebagai referensi dengan mencantumkan atribusi kepada penulis.
```
