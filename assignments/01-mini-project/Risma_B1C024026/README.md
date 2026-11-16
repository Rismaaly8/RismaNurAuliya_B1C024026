# Mini Assignment - Klasifikasi Kanker Payudara

## Identitas Mahasiswa
- **Nama:** Risma Nur Auliya[cite: 18]
- **NIM:** B1C024026[cite: 18]
- **Kelas:** [A]

---

## Deskripsi Eksperimen
Eksperimen ini bertujuan untuk membandingkan performa dua algoritma *machine learning*, yaitu **Logistic Regression** dan **Random Forest Classifier**, dalam mengklasifikasikan data kanker payudara (*Breast Cancer Wisconsin Dataset*)[cite: 1, 3, 7]. Dataset berjumlah 569 data dengan 30 fitur dan 2 kelas target (`malignant` dan `benign`), yang dibagi menggunakan rasio **70% data training (398 data)** dan **30% data testing (171 data)**[cite: 1, 7, 15].

---

## Hasil Evaluasi Model

| Algoritma | Accuracy | Precision | Recall | F1-Score |
| :--- | :---: | :---: | :---: | :---: |
| **Logistic Regression** | 0.9883 (98.83%)[cite: 7] | 0.9883[cite: 7] | 0.9883[cite: 7] | 0.9883[cite: 7] |
| **Random Forest Classifier** | 0.9357 (93.57%)[cite: 7] | 0.9355[cite: 7] | 0.9357[cite: 7] | 0.9356[cite: 7] |

### Ringkasan Confusion Matrix (171 Data Uji)
- **Logistic Regression:** 63 *True Positive* (`malignant`), 106 *True Negative* (`benign`), 1 *False Positive*, dan 1 *False Negative*[cite: 14].
- **Random Forest:** 58 *True Positive* (`malignant`), 102 *True Negative* (`benign`), 5 *False Positive*, dan 6 *False Negative*[cite: 14].

---

## Analisis & Kesimpulan
1. **Perbandingan Performa:** **Logistic Regression** memberikan hasil klasifikasi yang lebih unggul dibandingkan **Random Forest Classifier** di seluruh metrik evaluasi (akurasi 98.83% berbanding 93.57%)[cite: 7].
2. **Pentingnya Metrik Selain Accuracy:** Dalam diagnosis medis seperti deteksi kanker, metrik **Accuracy** saja tidak cukup karena tidak mencerminkan risiko kesalahan prediksi pada kelas positif (*malignant*)[cite: 4, 7]. Metrik **Recall** sangat krusial untuk meminimalkan kasus *False Negative* (pasien kanker ganas yang terprediksi jinak/sehat sehingga terlambat ditangani)[cite: 4, 7]. Pada eksperimen ini, *Recall* kelas `malignant` pada Logistic Regression mencapai **0.98**, lebih tinggi dibandingkan Random Forest sebesar **0.91**[cite: 7, 15].
