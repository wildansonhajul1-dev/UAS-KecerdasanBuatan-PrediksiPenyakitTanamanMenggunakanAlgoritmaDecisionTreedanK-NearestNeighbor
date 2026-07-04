# LAPORAN UAS KECERDASAN BUATAN

## Prediksi Penyakit Tanaman Menggunakan Algoritma Decision Tree dan K-Nearest Neighbor

### Disusun Oleh

**Nama** : Wildan Sonhajul M
**NIM** : 2406019
**Nama** : Rise Kartika
**NIM**  : 2406009


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

Dataset diperoleh dari Kaggle dengan nama **Plant Disease Classification Dataset**. yang diperoleh dari Kaggle.

Link Dataset:
https://www.kaggle.com/datasets/turakut/plant-disease-classification?utm_source=chatgpt.com

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

<img width="373" height="210" alt="image" src="https://github.com/user-attachments/assets/8bc02ac6-3d91-436d-9a63-8ed620345446" />


<img width="552" height="262" alt="image" src="https://github.com/user-attachments/assets/105ed72f-6440-4576-a7e0-f93d36386b4c" />


---

# 4. Exploratory Data Analysis (EDA)

Tahap Exploratory Data Analysis dilakukan untuk memahami karakteristik data sebelum dilakukan proses pelatihan model.

## Histogram

Histogram digunakan untuk melihat distribusi setiap fitur pada dataset.

<img width="698" height="543" alt="image" src="https://github.com/user-attachments/assets/80ab3764-db50-43db-a504-f7e76e8a0c33" />


Berdasarkan histogram terlihat bahwa distribusi data cukup beragam pada masing-masing fitur.

---

## Heatmap Korelasi

Heatmap digunakan untuk melihat hubungan antar fitur.

<img width="499" height="425" alt="image" src="https://github.com/user-attachments/assets/f63c4e78-5e84-44d6-a2c1-6677a645909f" />


Berdasarkan heatmap terlihat bahwa korelasi antar fitur tidak terlalu tinggi sehingga seluruh fitur tetap digunakan.

---

## Distribusi Target

Distribusi target digunakan untuk mengetahui keseimbangan jumlah data pada setiap kelas.

<img width="455" height="313" alt="image" src="https://github.com/user-attachments/assets/03d5fabf-ee86-41e9-8ae1-8ecde7d306de" />


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


---

# 6. Modeling

Pada penelitian ini digunakan dua algoritma machine learning yaitu Decision Tree dan K-Nearest Neighbor.

## Decision Tree

Decision Tree merupakan algoritma klasifikasi yang bekerja dengan membentuk pohon keputusan berdasarkan atribut yang paling berpengaruh terhadap target.

### Hasil

Accuracy Decision Tree: 0.772

<img width="413" height="358" alt="image" src="https://github.com/user-attachments/assets/dca41bcc-94b7-4a7d-9d00-5b280e43d676" />


<img width="359" height="146" alt="image" src="https://github.com/user-attachments/assets/c98305ac-7971-4ec5-b2d3-b163cf6d718f" />


---

## K-Nearest Neighbor (KNN)

KNN merupakan algoritma klasifikasi yang menentukan kelas berdasarkan kedekatan jarak antar data.

### Hasil

Accuracy KNN: 0.8325

<img width="427" height="360" alt="image" src="https://github.com/user-attachments/assets/cdb561a0-09cb-4f65-9d34-bf00590b0028" />


<img width="366" height="144" alt="image" src="https://github.com/user-attachments/assets/57d4824b-8f43-49a8-9e6b-02f730c25d90" />


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
|Decision Tree|0.772|
|KNN|0.8325|

<img width="451" height="347" alt="image" src="https://github.com/user-attachments/assets/8af142f3-1efc-4c84-aced-bc240d03bcac" />


### Analisis

Berdasarkan hasil pengujian, kedua algoritma mampu melakukan klasifikasi penyakit tanaman dengan baik. Perbedaan nilai akurasi dipengaruhi oleh karakteristik data serta parameter yang digunakan pada masing-masing algoritma.

---

# 8. Kesimpulan

Berdasarkan hasil penelitian dapat disimpulkan bahwa algoritma Decision Tree dan K-Nearest Neighbor berhasil diterapkan untuk melakukan klasifikasi penyakit tanaman. Kedua algoritma mampu menghasilkan prediksi dengan performa yang baik pada dataset yang digunakan.

Algoritma dengan nilai akurasi tertinggi dapat dijadikan sebagai model yang lebih direkomendasikan untuk digunakan pada dataset ini.

Untuk penelitian selanjutnya disarankan menggunakan dataset yang lebih besar atau membandingkan dengan algoritma lain seperti Random Forest maupun Support Vector Machine agar diperoleh hasil yang lebih optimal.

---

# 9. Referensi

1. Purnamawati, A., Nugroho, W. F., Putri, D., & Hidayat, W. F. (2020). *Deteksi Penyakit Daun pada Tanaman Padi Menggunakan Algoritma Decision Tree, Random Forest, Naïve Bayes, SVM dan KNN*. InfoTekJar: Jurnal Nasional Informatika dan Teknologi Jaringan, 5(1). [https://doi.org/10.30743/infotekjar.v5i1.2934](https://jurnal.uisu.ac.id/index.php/infotekjar/article/view/2934/pdf?utm_source=chatgpt.com)

2. Demilie. (2024). *Plant disease detection and classification using machine learning and deep learning techniques: A review*. Journal of Big Data, 11(5). [https://doi.org/10.1186/s40537-023-00863-9](https://link.springer.com/article/10.1186/s40537-023-00863-9?utm_source=chatgpt.com)

3. Astagina, A. U., Juniar, E., Mutmainah, S., & Lorosae, T. A. (2025). *Klasifikasi Hama dan Penyakit Tanaman Padi Menggunakan Algoritma Decision Tree*. Scientific: Journal of Computer Science and Informatics, 2(2). https://ejurnal.umbima.ac.id/index.php/scientific/article/view/376?utm_source=chatgpt.com

4. *Classification and Identification of Pest Diseases and Crop Monitoring Using Artificial Intelligence*. (2025). Information Processing in Agriculture. https://www.sciencedirect.com/science/article/pii/S2214317324000647?utm_source=chatgpt.com&__cf_chl_f_tk=KzMv1TyE_j1LursZayucrUg9DHxQi1KG08tc_u0.J9s-1783108525-1.0.1.1-Z40BbCPPqZt25U3efD8OmBPI.xTVF8JblneNkcZfv7E

5. Shafik, W., Tufail, A., Liyanage, C. D. S., & Apong, R. A. A. H. M. (2024). *Plant disease detection and classification using deep learning techniques*. BMC Plant Biology, 24, 136.

---

# 10. Lampiran

## Link Dataset
https://www.kaggle.com/datasets/turakut/plant-disease-classification?utm_source=chatgpt.com

## Link Repository GitHub
https://www.kaggle.com/datasets/turakut/plant-disease-classification?utm_source=chatgpt.com

## Lampiran Gambar

- Histogram
  <img width="839" height="682" alt="image" src="https://github.com/user-attachments/assets/707c41b4-9356-49a6-917d-379cec5455a7" />

- Heatmap
  <img width="588" height="532" alt="image" src="https://github.com/user-attachments/assets/b0882d0b-6712-4ce6-a70f-38f28f18a12a" />

- Distribusi Target
  <img width="549" height="393" alt="image" src="https://github.com/user-attachments/assets/198ad701-3888-424e-bec5-00fc6669f108" />

- Confusion Matrix Decision Tree
  <img width="515" height="455" alt="image" src="https://github.com/user-attachments/assets/d7a9a5d8-31c3-446e-b839-14196dce1dc6" />

- Confusion Matrix KNN
  <img width="515" height="455" alt="image" src="https://github.com/user-attachments/assets/40a706f1-7bab-457e-8cf6-6e3a51e5ef8f" />

- Grafik Perbandingan Akurasi
  <img width="567" height="435" alt="image" src="https://github.com/user-attachments/assets/16d15298-3cd3-46cb-a1cd-7b0af59ecd63" />

