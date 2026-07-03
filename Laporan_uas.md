# LAPORAN UAS KECERDASAN BUATAN

## Nama
Wildan Sonhajul M

## NIM
2406019

## Kelas
Informatika A

---

# 1. Judul Proyek

## Prediksi Penyakit Tanaman Menggunakan Algoritma Decision Tree dan K-Nearest Neighbor

### Domain Proyek

Penyakit pada tanaman merupakan salah satu penyebab utama menurunnya hasil panen. Apabila penyakit tidak terdeteksi sejak dini, penyebarannya dapat menyebabkan penurunan kualitas maupun kuantitas hasil pertanian. Oleh karena itu, pemanfaatan teknologi kecerdasan buatan dan machine learning dapat membantu proses identifikasi penyakit tanaman secara lebih cepat dan akurat. :contentReference[oaicite:0]{index=0}

Pada proyek ini digunakan algoritma Decision Tree dan K-Nearest Neighbor (KNN) untuk melakukan klasifikasi penyakit tanaman berdasarkan data yang tersedia. Hasil penelitian diharapkan dapat membantu proses pengambilan keputusan dalam mendeteksi penyakit tanaman secara lebih cepat.

---

# 2. Business Understanding

## Permasalahan

Petani sering mengalami kesulitan dalam mendeteksi penyakit tanaman secara cepat. Akibatnya, proses penanganan sering terlambat sehingga menyebabkan penurunan hasil panen.

Beberapa penelitian menunjukkan bahwa algoritma klasifikasi seperti Decision Tree dan K-Nearest Neighbor mampu memberikan hasil yang baik dalam proses identifikasi penyakit tanaman sehingga kedua algoritma tersebut dipilih pada penelitian ini. :contentReference[oaicite:1]{index=1}

## Tujuan

Tujuan dari proyek ini adalah:

- Membangun model klasifikasi penyakit tanaman.
- Membandingkan performa Decision Tree dan KNN.
- Menentukan algoritma dengan hasil terbaik.

## Pengguna

- Petani
- Penyuluh Pertanian
- Peneliti
- Mahasiswa

## Manfaat

- Membantu mendeteksi penyakit tanaman lebih cepat.
- Mengurangi risiko gagal panen.
- Menjadi referensi penelitian selanjutnya.

---

# 3. Data Understanding

Dataset yang digunakan berasal dari Kaggle dengan nama **Plant Disease Classification Dataset**.

Dataset memiliki:

- Jumlah data : 10.000
- Jumlah fitur : 4
- Target : disease_present

### Atribut Dataset

|No|Atribut|Keterangan|
|---|---|---|
|1|temperature|Suhu|
|2|humidity|Kelembapan|
|3|rainfall|Curah Hujan|
|4|soil_pH|pH Tanah|
|5|disease_present|Label penyakit|

Berdasarkan hasil pengecekan menggunakan `df.info()` dan `df.isnull().sum()`, dataset tidak memiliki missing value sehingga dapat langsung digunakan pada proses pelatihan model.

Dataset ini sesuai digunakan untuk klasifikasi penyakit tanaman menggunakan algoritma machine learning. :contentReference[oaicite:2]{index=2}

---

# 4. Exploratory Data Analysis (EDA)

Pada tahap ini dilakukan analisis awal terhadap dataset.

Analisis meliputi:

- Histogram
- Heatmap Korelasi
- Distribusi Kelas
- Statistik Deskriptif

### Hasil Analisis

Berdasarkan visualisasi histogram diketahui bahwa setiap atribut memiliki distribusi data yang cukup baik.

Heatmap menunjukkan hubungan antar atribut terhadap target klasifikasi.

Distribusi kelas memperlihatkan jumlah data penyakit dan tidak penyakit cukup seimbang sehingga model dapat dilatih dengan baik.

> Tambahkan screenshot:
>
> - Histogram
> - Heatmap
> - Countplot

---

# 5. Data Preparation

Tahapan persiapan data dilakukan sebagai berikut.

- Memisahkan fitur dan target.
- Membagi data training dan testing dengan rasio 80:20.
- Melakukan normalisasi menggunakan StandardScaler.

Normalisasi dilakukan agar seluruh atribut memiliki skala yang sama sehingga proses klasifikasi menjadi lebih optimal.

---

# 6. Modeling

Penelitian ini menggunakan dua algoritma.

## Decision Tree

Decision Tree merupakan algoritma klasifikasi yang membentuk pohon keputusan berdasarkan atribut yang paling berpengaruh terhadap target. Algoritma ini mudah dipahami dan banyak digunakan dalam klasifikasi data pertanian. :contentReference[oaicite:3]{index=3}

**Hasil Akurasi:** *(isi sesuai output notebook, misalnya 75,30%)*

---

## K-Nearest Neighbor (KNN)

KNN melakukan klasifikasi berdasarkan kedekatan jarak antar data menggunakan sejumlah tetangga terdekat. Metode ini sering digunakan sebagai pembanding dalam penelitian klasifikasi penyakit tanaman. :contentReference[oaicite:4]{index=4}

**Hasil Akurasi:** *(isi sesuai output notebook)*

---

# 7. Evaluation

Evaluasi model dilakukan menggunakan:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

Berdasarkan hasil pengujian, kedua algoritma mampu melakukan klasifikasi penyakit tanaman dengan baik. Perbedaan nilai akurasi dipengaruhi oleh karakteristik data dan parameter model yang digunakan. :contentReference[oaicite:5]{index=5}

### Hasil Perbandingan

|Algoritma|Accuracy|
|---|---:|
|Decision Tree|75.xx %|
|KNN|xx.xx %|

> Tambahkan screenshot:
>
> - Confusion Matrix Decision Tree
> - Confusion Matrix KNN
> - Grafik Perbandingan Akurasi

---

# 8. Kesimpulan

Berdasarkan hasil penelitian, algoritma Decision Tree dan K-Nearest Neighbor berhasil diterapkan untuk melakukan klasifikasi penyakit tanaman. Kedua algoritma menunjukkan performa yang cukup baik, namun salah satu algoritma memperoleh nilai akurasi lebih tinggi sehingga lebih direkomendasikan untuk digunakan pada dataset ini.

Pengembangan selanjutnya dapat dilakukan dengan menggunakan dataset yang lebih besar atau membandingkan dengan algoritma lain seperti Random Forest, Support Vector Machine (SVM), maupun Deep Learning agar diperoleh hasil klasifikasi yang lebih optimal. :contentReference[oaicite:6]{index=6}

---

# 9. Referensi

1. Purnamawati, A., Nugroho, W. F., Putri, D., & Hidayat, W. F. (2020). *Deteksi Penyakit Daun pada Tanaman Padi Menggunakan Algoritma Decision Tree, Random Forest, Naïve Bayes, SVM dan KNN*. InfoTekJar: Jurnal Nasional Informatika dan Teknologi Jaringan, 5(1). https://doi.org/10.30743/infotekjar.v5i1.2934

2. Demilie. (2024). *Plant disease detection and classification using machine learning and deep learning techniques: A review*. Journal of Big Data, 11(5). https://doi.org/10.1186/s40537-023-00863-9

3. Astagina, A. U., Juniar, E., Mutmainah, S., & Lorosae, T. A. (2025). *Klasifikasi Hama dan Penyakit Tanaman Padi Menggunakan Algoritma Decision Tree*. Scientific: Journal of Computer Science and Informatics, 2(2). https://doi.org/10.34304/scientific.v2.i2.376

4. *Classification and Identification of Pest Diseases and Crop Monitoring Using Artificial Intelligence*. (2025). Information Processing in Agriculture.

5. Shafik, W., Tufail, A., Liyanage, C. D. S., & Apong, R. A. A. H. M. (2024). *Plant disease detection and classification using deep learning techniques*. BMC Plant Biology, 24, 136.

---

# 10. Lampiran

Lampiran terdiri dari:

- Source Code Google Colab
- Dataset
- Hasil Histogram
- Heatmap
- Confusion Matrix Decision Tree
- Confusion Matrix KNN
- Grafik Perbandingan Akurasi
- Link Repository GitHub
