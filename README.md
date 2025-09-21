# mental-health-in-tech
Analisis Data Mental Health in Tech menggunakan Google Colab

# Mental Health in Tech Analysis

Oleh: **Kholishotul Mu'diyah**

---

## Overview
Proyek ini bertujuan untuk menganalisis faktor-faktor yang berhubungan dengan kesehatan mental di kalangan profesional teknologi menggunakan dataset survei publik.  
Analisis dilakukan dengan bantuan **Google Colab**, serta model machine learning untuk prediksi.

---

## Dataset
Dataset yang digunakan adalah:  
**Mental Health in Tech Survey** dari Kaggle  
🔗 [https://www.kaggle.com/datasets/osmi/mental-health-in-tech-survey](https://www.kaggle.com/datasets/osmi/mental-health-in-tech-survey)

---

## Analysis Process
1. **Pengumpulan Data**  
   - Mengunduh dataset dari Kaggle menggunakan `opendatasets`.

2. **Persiapan Data**  
   - Memilih kolom relevan: `Age`, `Gender`, `family_history`, `remote_work`, `work_interfere`, `treatment`.  
   - Menangani missing value (`dropna`).  
   - Encoding data kategorikal dengan `LabelEncoder`.

3. **Pemodelan**  
   - **Random Forest Classifier** → memprediksi apakah responden mencari perawatan (`treatment`).  
   - **Deep Learning (Keras Sequential Model)** → prediksi dengan jaringan saraf sederhana.

4. **Evaluasi Model**  
   - Random Forest → `classification_report` (akurasi ±74%).  
   - Keras → evaluasi akurasi & loss (akurasi ±79.9%).

5. **Analisis Fitur**  
   - Menggunakan feature importance (Random Forest) untuk melihat faktor paling berpengaruh.

6. **Eksplorasi dengan LLM**  
   - Menggunakan LLM (Replicate `meta/llama-2-70b-chat`) untuk menghasilkan wawasan & ide pertanyaan penelitian.

---

## Insight & Findings
- **Performa Model**  
  - Random Forest: akurasi ±74%.  
  - Keras: akurasi ±79.9%.  

- **Faktor Penting**  
  - Usia (`Age`), gangguan kerja (`work_interfere`), dan jenis kelamin (`Gender`) adalah prediktor utama treatment.  

- **Hubungan Family History & Treatment**  
  - Responden dengan riwayat keluarga gangguan mental lebih cenderung mencari perawatan.  

- **Distribusi Usia**  
  - Mayoritas pencari treatment berusia 20–35 tahun.  

- **Wawasan LLM**  
  - Pertanyaan baru: *Apakah ukuran perusahaan atau kebijakan kesehatan memengaruhi tingkat pencarian treatment?*  
  - Potensi penelitian lebih lanjut terkait remote work & work interfere.  

---

## Kesimpulan & Rekomendasi
- Faktor seperti usia, riwayat keluarga, dan gangguan kerja signifikan memengaruhi keputusan mencari perawatan.  
- Model prediktif dapat membantu perusahaan mengidentifikasi pegawai berisiko.  
- Perusahaan sebaiknya memperkuat kebijakan support mental health & edukasi.  
- Analisis lanjutan bisa fokus ke **lokasi geografis**, **ukuran perusahaan**, dan **budaya perusahaan**.  

---

## AI Support Explanation
Dalam proyek ini, AI digunakan untuk:
- **Google Colab** → pengolahan data, visualisasi, pemodelan machine learning.  
- **Random Forest & Deep Learning (Keras)** → prediksi treatment.  
- **LLM (Replicate)** → menghasilkan insight tambahan & pertanyaan riset.  

---

## Repository Content
- `notebooks/Project_Akhir_IBM_Kholishotul_Mu'diyah.ipynb` → notebook analisis utama.  
- `README.md` → dokumentasi project.  
- `data/` → (opsional) dataset mentah.  
- `visuals/` → (opsional) grafik/visualisasi hasil analisis.  

---
