# Poverty Classification Indonesia

---

## Anggota Kelompok

* Elok Elysia Dewi (103132400013)
* Lintang Anissa Hakim (103132400040)
* Ken Rayana Ilma Madani (103132430008)

---

## Deskripsi Proyek

Proyek ini bertujuan untuk mengklasifikasikan tingkat kemiskinan pada berbagai Kabupaten/Kota di Indonesia menggunakan algoritma Machine Learning. Model dibangun untuk memprediksi **Klasifikasi Kemiskinan** berdasarkan berbagai indikator sosial dan ekonomi seperti tingkat kemiskinan, pendidikan, kesehatan, sanitasi, pengeluaran per kapita, dan ketenagakerjaan.

---

## Dataset

Dataset yang digunakan adalah **poverty_classification.csv** yang diperoleh dari Kaggle dan berisi indikator sosial ekonomi kabupaten/kota di Indonesia.

**Sumber Dataset:**

* Kaggle – *https://www.kaggle.com/datasets/ermila/klasifikasi-tingkat-kemiskinan-di-indonesia*

Dataset memiliki 999 baris data dengan 13 atribut. Setelah proses data cleaning, sebanyak 485 baris kosong dihapus sehingga tersisa **514 data** yang digunakan dalam proses pemodelan.

### Fitur Dataset

* Provinsi
* Kab/Kota
* Persentase Penduduk Miskin (P0)
* Rata-rata Lama Sekolah Penduduk 15+
* Pengeluaran per Kapita Disesuaikan
* Indeks Pembangunan Manusia (IPM)
* Umur Harapan Hidup
* Persentase Rumah Tangga dengan Sanitasi Layak
* Persentase Rumah Tangga dengan Akses Air Minum Layak
* Tingkat Pengangguran Terbuka
* Tingkat Partisipasi Angkatan Kerja

**Target:**

* Klasifikasi Kemiskinan

---

## Tahapan Preprocessing

Tahapan preprocessing yang dilakukan meliputi:

* Menghapus data yang memiliki missing value menggunakan `dropna()`.
* Mengubah format angka dari koma (`,`) menjadi titik (`.`).
* Mengubah tipe data numerik menjadi `float`.
* Memisahkan fitur (`X`) dan target (`y`).
* Membagi data menjadi data latih (80%) dan data uji (20%) menggunakan `train_test_split()`.
* Melakukan standardisasi data menggunakan `StandardScaler` untuk Logistic Regression dan Gaussian Naive Bayes.

---

## Algoritma yang Digunakan

Penelitian ini membandingkan tiga algoritma klasifikasi:

* Logistic Regression
* Decision Tree
* Gaussian Naive Bayes

Evaluasi model dilakukan menggunakan:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

---

## Cara Menjalankan Program

1. Clone repository ini.
2. Install seluruh library yang terdapat pada `requirements.txt`.

```bash
pip install -r requirements.txt
```

3. Buka notebook `Poverty_Classification.ipynb`.
4. Jalankan seluruh cell secara berurutan.
5. Model akan melakukan preprocessing, pelatihan, evaluasi, dan menampilkan hasil perbandingan ketiga algoritma.

---

## Hasil Evaluasi

| Model                |   Accuracy |  Precision |      Recall |   F1-Score |
| -------------------- | ---------: | ---------: | ----------: | ---------: |
| Decision Tree        | **99.03%** | **92.31%** | **100.00%** | **96.00%** |
| Logistic Regression  |     97.09% |     84.62% |      91.67% |     88.00% |
| Gaussian Naive Bayes |     96.12% |     75.00% |     100.00% |     85.71% |

### Model Terbaik

Berdasarkan hasil evaluasi, **Decision Tree** merupakan algoritma dengan performa terbaik karena memperoleh Accuracy, Precision, Recall, dan F1-Score tertinggi dibandingkan algoritma lainnya.

---

## Kesimpulan

Penelitian ini berhasil membangun model klasifikasi tingkat kemiskinan menggunakan tiga algoritma Machine Learning, yaitu Logistic Regression, Decision Tree, dan Gaussian Naive Bayes.

Seluruh model menunjukkan performa yang baik, namun **Decision Tree** memberikan hasil terbaik dengan Accuracy sebesar **99,03%**, Precision sebesar **92,31%**, Recall sebesar **100%**, dan F1-Score sebesar **96,00%**. Oleh karena itu, Decision Tree dipilih sebagai model yang paling efektif untuk mengklasifikasikan tingkat kemiskinan berdasarkan dataset yang digunakan.

---
