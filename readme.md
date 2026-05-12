# Perbandingan Algoritma Naïve Bayes dan K-Nearest Neighbor dalam Analisis Concept Drift pada Ulasan MyAnimeList

## Deskripsi Project

Project ini merupakan penelitian analisis sentimen berbasis *machine learning* yang bertujuan untuk membandingkan performa algoritma Naïve Bayes dan K-Nearest Neighbor (*KNN*) dalam menghadapi *concept drift* pada ulasan anime MyAnimeList.

Penelitian menggunakan dua dataset dari periode waktu berbeda, yaitu dataset tahun 2020 dan dataset tahun 2024. Dataset tahun 2020 digunakan sebagai data *baseline* untuk pelatihan model, sedangkan dataset tahun 2024 digunakan untuk menguji perubahan performa model terhadap data temporal yang berbeda.

Perubahan pola bahasa, penggunaan istilah baru, dan perubahan distribusi data pada ulasan anime dari waktu ke waktu dapat menyebabkan penurunan performa model klasifikasi. Fenomena tersebut dikenal sebagai *concept drift*.

---

## Tujuan Penelitian

- Menganalisis pengaruh *concept drift* terhadap performa model klasifikasi sentimen
- Membandingkan performa algoritma Naïve Bayes dan *KNN* pada ulasan anime MyAnimeList
- Menentukan algoritma yang lebih stabil terhadap perubahan distribusi data temporal

---

## Dataset

Dataset yang digunakan berasal dari platform Kaggle dan berisi ulasan anime dari MyAnimeList.

### Dataset yang digunakan
- Dataset MyAnimeList 2020
- Dataset MyAnimeList 2024

### Jumlah Data

| Dataset | Total Data | Sampel Digunakan |
|---|---|---|
| Dataset 2020 | ±192.112 review | 5000 review |
| Dataset 2024 | 7448 review | 5000 review |

---

## Metodologi Penelitian

Tahapan penelitian pada project ini meliputi:

1. Pengumpulan dataset
2. Pelabelan sentimen
3. *Text preprocessing*
4. Transformasi fitur menggunakan metode *TF-IDF*
5. Pelatihan model klasifikasi
6. Pengujian model pada dataset temporal berbeda
7. Evaluasi performa model
8. Analisis *concept drift*

---

## Text Preprocessing

Tahapan *preprocessing* yang digunakan pada penelitian ini meliputi:

- *Case Folding*
- *Remove Punctuation*
- *Remove Number*
- *Remove Whitespace*
- *Stopword Removal*

Hasil akhir *preprocessing* digunakan untuk proses transformasi fitur menggunakan metode *TF-IDF*.

---

## Algoritma yang Digunakan

### Naïve Bayes
Algoritma klasifikasi probabilistik yang bekerja berdasarkan Teorema Bayes dan efektif digunakan pada klasifikasi teks berdimensi tinggi.

### K-Nearest Neighbor (KNN)
Algoritma klasifikasi berbasis jarak yang bekerja dengan mencari tetangga terdekat berdasarkan tingkat kemiripan fitur data.

---

## Evaluasi Model

Evaluasi model dilakukan menggunakan beberapa metrik berikut:

- *Accuracy*
- *Precision*
- *Recall*
- *F1-Score*
- *Confusion Matrix*

---

## Hasil Penelitian

### Pengujian Dataset 2020

| Model | Accuracy |
|---|---|
| Naïve Bayes | 76.1% |
| KNN | 68.8% |

Naïve Bayes menunjukkan performa lebih baik pada dataset *baseline* karena lebih efektif dalam menangani data teks berbasis *TF-IDF*.

---

### Pengujian Dataset 2024

| Model | Accuracy |
|---|---|
| Naïve Bayes | 61.7% |
| KNN | 61.94% |

Kedua model mengalami penurunan performa ketika diuji menggunakan dataset temporal yang lebih baru.

---

## Analisis Concept Drift

| Model | Dataset 2020 | Dataset 2024 | Penurunan |
|---|---|---|---|
| Naïve Bayes | 76.1% | 61.7% | 14.4% |
| KNN | 68.8% | 61.94% | 6.86% |

Hasil penelitian menunjukkan bahwa algoritma *KNN* memiliki stabilitas yang lebih baik terhadap perubahan distribusi data temporal dibandingkan Naïve Bayes. Namun, Naïve Bayes masih unggul dalam performa awal pada data teks berbasis *TF-IDF*.

---

## Tools dan Library

Project ini dikembangkan menggunakan:

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Struktur Project

```bash
dataset/
├── dataset_2020.csv
├── dataset_2024.jsonl

notebook/
├── concept_drift_analysis.ipynb

results/
├── accuracy_comparison.png
├── cm_visualization2020.png
├── cm_visualization2024.png

README.md
```

---

## Cara Menjalankan Project

### 1. Clone Repository

```bash
git clone https://github.com/r1enc/Concept-Drift-MyAnimeList.git
```

### 2. Install Dependency

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

### 3. Jalankan Jupyter Notebook

```bash
jupyter notebook
```

### 4. Buka Notebook

```bash
concept_drift_analysis.ipynb
```

---

## Kesimpulan

Penelitian ini menunjukkan bahwa perubahan distribusi data temporal pada ulasan anime dapat memengaruhi performa model klasifikasi sentimen. Naïve Bayes memberikan performa awal yang lebih tinggi pada dataset *baseline*, sedangkan *KNN* menunjukkan stabilitas yang lebih baik terhadap *concept drift* karena mengalami penurunan performa yang lebih kecil.

---

## Author

Wildan Ariel Heradi

---

## License

Project ini dibuat untuk kebutuhan penelitian akademik dan pembelajaran.