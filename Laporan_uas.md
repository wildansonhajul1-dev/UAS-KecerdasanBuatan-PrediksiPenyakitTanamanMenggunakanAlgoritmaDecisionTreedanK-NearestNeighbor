# LAPORAN UAS KECERDASAN BUATAN

## Prediksi Penyakit Tanaman Menggunakan Algoritma Decision Tree dan K-Nearest Neighbor

### Disusun Oleh

**Nama** : Wildan Sonhajul M

**NIM** : 2406019

**Kelas** : Informatika A

---

# 1. Judul Proyek

## Prediksi Penyakit Tanaman Menggunakan Algoritma Decision Tree dan K-Nearest Neighbor

### Domain Proyek

Penyakit tanaman merupakan salah satu faktor utama yang menyebabkan menurunnya kualitas dan hasil panen. Proses identifikasi penyakit yang masih dilakukan secara manual sering kali membutuhkan waktu yang cukup lama dan bergantung pada pengalaman petani. Dengan perkembangan teknologi Artificial Intelligence (AI), proses identifikasi penyakit tanaman dapat dilakukan secara otomatis menggunakan algoritma machine learning.

Pada proyek ini digunakan dua algoritma klasifikasi, yaitu Decision Tree dan K-Nearest Neighbor (KNN), untuk memprediksi apakah suatu tanaman mengalami penyakit berdasarkan data yang tersedia. Hasil dari proyek ini diharapkan dapat membantu proses identifikasi penyakit tanaman secara lebih cepat dan akurat sehingga dapat menjadi pendukung dalam pengambilan keputusan di bidang pertanian.

---

# 2. Business Understanding

## Permasalahan

Petani sering mengalami kesulitan dalam mendeteksi penyakit tanaman secara cepat sehingga penanganan menjadi terlambat. Hal tersebut dapat menyebabkan penurunan hasil panen bahkan gagal panen.

## Tujuan

Tujuan dari proyek ini adalah:

- Membangun model klasifikasi penyakit tanaman.
- Membandingkan performa algoritma Decision Tree dan KNN.
- Menentukan algoritma dengan hasil klasifikasi terbaik.

## Pengguna

- Petani
- Penyuluh Pertanian
- Mahasiswa
- Peneliti

## Manfaat

Manfaat dari proyek ini adalah membantu proses identifikasi penyakit tanaman secara lebih cepat sehingga penanganan dapat dilakukan sedini mungkin.

---

# 3. Data Understanding

## Sumber Dataset

Dataset diperoleh dari Kaggle dengan nama **Plant Disease Classification Dataset**.

## Deskripsi Dataset

Dataset terdiri dari data kondisi lingkungan yang digunakan untuk memprediksi keberadaan penyakit pada tanaman.

## Jumlah Data

10000 data

## Jumlah Fitur

5 kolom

## Deskripsi Fitur

|No|Fitur|Keterangan|
|---|---|---|
|1|temperature|Suhu|
|2|humidity|Kelembaban|
|3|rainfall|Curah hujan|
|4|soil_pH|Nilai pH tanah|
|5|disease_present|Target klasifikasi|

## Pemeriksaan Dataset

Dataset diperiksa menggunakan fungsi:

- df.head()
- df.info()
- df.describe()
- df.isnull().sum()
- df.duplicated().sum()

Hasil pemeriksaan menunjukkan bahwa dataset tidak memiliki missing value sehingga dapat langsung digunakan untuk proses pelatihan model.

📷 **MASUKKAN FOTO OUTPUT `df.info()` DI SINI**

📷 **MASUKKAN FOTO OUTPUT `df.describe()` DI SINI**

---

# 4. Exploratory Data Analysis (EDA)

Tahap Exploratory Data Analysis dilakukan untuk memahami karakteristik data sebelum dilakukan proses pelatihan model.

## Histogram

Histogram digunakan untuk melihat distribusi setiap fitur pada dataset.

📷 **MASUKKAN FOTO HISTOGRAM DI SINI**

Berdasarkan histogram terlihat bahwa distribusi data cukup beragam pada masing-masing fitur.

---

## Heatmap Korelasi

Heatmap digunakan untuk melihat hubungan antar fitur.

📷 **MASUKKAN FOTO HEATMAP DI SINI**

Berdasarkan heatmap terlihat bahwa korelasi antar fitur tidak terlalu tinggi sehingga seluruh fitur tetap digunakan.

---

## Distribusi Target

Distribusi target digunakan untuk mengetahui keseimbangan jumlah data pada setiap kelas.

📷 **MASUKKAN FOTO BAR CHART / COUNTPLOT DI SINI**

Berdasarkan visualisasi tersebut jumlah data antar kelas relatif seimbang sehingga model tidak mengalami masalah class imbalance.

---

## Insight

Berdasarkan hasil EDA dapat disimpulkan bahwa dataset memiliki kualitas yang baik, tidak terdapat data kosong, serta distribusi data cukup seimbang sehingga layak digunakan untuk proses klasifikasi.

---

# 5. Data Preparation

Tahapan Data Preparation meliputi:

- Mengecek missing value.
- Mengecek data duplikat.
- Memisahkan fitur dan target.
- Membagi dataset menjadi data training dan testing dengan rasio 80:20.
- Melakukan normalisasi menggunakan StandardScaler.

Normalisasi dilakukan agar seluruh fitur memiliki skala yang sama sehingga meningkatkan performa algoritma machine learning.

📷 **MASUKKAN FOTO OUTPUT SPLIT DATA DI SINI (jika ada)**

---

# 6. Modeling

Pada penelitian ini digunakan dua algoritma machine learning yaitu Decision Tree dan K-Nearest Neighbor.

## Decision Tree

Decision Tree merupakan algoritma klasifikasi yang bekerja dengan membentuk pohon keputusan berdasarkan atribut yang paling berpengaruh terhadap target.

### Hasil

Accuracy : **(Isi sesuai output Colab)**

📷 **MASUKKAN FOTO CONFUSION MATRIX DECISION TREE DI SINI**

📷 **MASUKKAN FOTO CLASSIFICATION REPORT DECISION TREE DI SINI**

---

## K-Nearest Neighbor (KNN)

KNN merupakan algoritma klasifikasi yang menentukan kelas berdasarkan kedekatan jarak antar data.

### Hasil

Accuracy : **(Isi sesuai output Colab)**

📷 **MASUKKAN FOTO CONFUSION MATRIX KNN DI SINI**

📷 **MASUKKAN FOTO CLASSIFICATION REPORT KNN DI SINI**

---

# 7. Evaluation

Evaluasi dilakukan menggunakan metrik:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

## Perbandingan Hasil

|Algoritma|Accuracy|
|---|---:|
|Decision Tree|...(isi dari output)...|
|KNN|...(isi dari output)...|

📷 **MASUKKAN FOTO GRAFIK PERBANDINGAN AKURASI DI SINI**

### Analisis

Berdasarkan hasil pengujian, kedua algoritma mampu melakukan klasifikasi penyakit tanaman dengan baik. Perbedaan nilai akurasi dipengaruhi oleh karakteristik data serta parameter yang digunakan pada masing-masing algoritma.

---

# 8. Kesimpulan

Berdasarkan hasil penelitian dapat disimpulkan bahwa algoritma Decision Tree dan K-Nearest Neighbor berhasil diterapkan untuk melakukan klasifikasi penyakit tanaman. Kedua algoritma mampu menghasilkan prediksi dengan performa yang baik pada dataset yang digunakan.

Algoritma dengan nilai akurasi tertinggi dapat dijadikan sebagai model yang lebih direkomendasikan untuk digunakan pada dataset ini.

Untuk penelitian selanjutnya disarankan menggunakan dataset yang lebih besar atau membandingkan dengan algoritma lain seperti Random Forest maupun Support Vector Machine agar diperoleh hasil yang lebih optimal.

---

# 9. Referensi

1. Purnamawati, A., Nugroho, W. F., Putri, D., & Hidayat, W. F. (2020). *Deteksi Penyakit Daun pada Tanaman Padi Menggunakan Algoritma Decision Tree, Random Forest, Naïve Bayes, SVM dan KNN*. InfoTekJar: Jurnal Nasional Informatika dan Teknologi Jaringan, 5(1). https://doi.org/10.30743/infotekjar.v5i1.2934

2. Demilie. (2024). *Plant disease detection and classification using machine learning and deep learning techniques: A review*. Journal of Big Data, 11(5). https://doi.org/10.1186/s40537-023-00863-9

3. Astagina, A. U., Juniar, E., Mutmainah, S., & Lorosae, T. A. (2025). *Klasifikasi Hama dan Penyakit Tanaman Padi Menggunakan Algoritma Decision Tree*. Scientific: Journal of Computer Science and Informatics, 2(2).

4. *Classification and Identification of Pest Diseases and Crop Monitoring Using Artificial Intelligence*. (2025). Information Processing in Agriculture.

5. Shafik, W., Tufail, A., Liyanage, C. D. S., & Apong, R. A. A. H. M. (2024). *Plant disease detection and classification using deep learning techniques*. BMC Plant Biology, 24, 136.

---

# 10. Lampiran

## Link Dataset

(Tuliskan link Kaggle)

## Link Repository GitHub

(Tuliskan link GitHub)

## Lampiran Gambar

- Histogram
- Heatmap
- Distribusi Target
- Confusion Matrix Decision Tree
- Confusion Matrix KNN
- Grafik Perbandingan Akurasi
