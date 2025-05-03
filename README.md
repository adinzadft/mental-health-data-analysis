# Mental‑Health‑in‑Tech – Data Analysis & Prediction

Menganalisis **faktor demografis** dan **lingkungan kerja** yang memengaruhi kesehatan mental pekerja teknologi berdasarkan data survei publik (OSMI – Mental Health in Tech).

Proyek ini menjawab empat pertanyaan riset utama dan membuat model machine‑learning untuk memprediksi apakah responden akan **mencari bantuan kesehatan mental**.

Proyek ini menggunakan dataset "Mental Health in Tech Survey". (https://www.kaggle.com/osmi/mental-health-in-tech-survey)

---

## ❓ Pertanyaan Penelitian
1. **Gender vs Gangguan Mental** – Apakah terdapat hubungan signifikan?
2. **Usia vs Gangguan Mental** – Apakah usia berpengaruh?
3. **Dukungan Perusahaan vs Seek Help** – Apakah program wellness mendorong karyawan mencari bantuan?
4. **Prediksi Seek Help** – Bisakah kita memprediksi perilaku tersebut dari variabel demografi & budaya kerja?

---

## 🔧 Tech Stack
| Area | Tools |
|------|-------|
| Bahasa | Python 3.10 |
| Analisis & EDA | pandas · numpy · matplotlib · seaborn |
| Statistik | SciPy (chi‑square, ANOVA) |
| ML Models | scikit‑learn (Decision Tree, Random Forest) |
| Repositori | Git & GitHub |

---

## 🗂️ Struktur Proyek
- dataset
  -survey.csv
- notebooks
  - MentalhealthAnalysis.ipynb
- README.md

---

## 🧑‍🔬 Tahapan Analisis
1. **Exploratory Data Analysis** – statistik deskriptif & visualisasi distribusi.
2. **Data Cleaning & Encoding** – normalisasi gender, filtering usia wajar, handling missing.
3. **Statistik Inferensial**  
   * Chi‑Square (Gender ↔ Mental‑Health‑Consequence)  
   * ANOVA (Age ↔ Mental‑Health‑Consequence)  
   * Chi‑Square (Wellness Program ↔ Seek Help)
4. **Modelling**  
   * Baseline Decision Tree (multiclass)  
   * Random Forest (n_estimators=100, max_depth=5)  
5. **Evaluasi** – Confusion Matrix & classification report per kelas.

---

## 📊 Ringkasan Hasil
| Metric (multiclass) | Baseline RF |
|---------------------|-------------|
| **Accuracy**        | **0.72** |
| Macro F1‑score      | 0.68 |
| Kelas 1 (Seek Help) F1 | **0.82** (recall 0.94) |
| Kelas 0 (Not Seek Help) F1 | 0.50 |
| Kelas 2 (Maybe) F1 | 0.72 |

*Model cukup kuat untuk mengenali responden yang memang akan mencari bantuan (recall 94 %).*

---

## Insight Kunci
* **Program wellness perusahaan berasosiasi signifikan** dengan kecenderungan karyawan mencari bantuan (p < 0.05, χ² test).  
* Responden usia **≤ 40 tahun** tanpa program wellness paling besar kemungkinannya *seek help* (hasil pohon keputusan).  
* Gender tidak menunjukkan perbedaan signifikan pada dataset ini.

---
