# Pembelajaran Mesin IF3012
# NPC_Klasifikasi
## Perbandingan Efektivitas Algoritma XGBoost dan MLP pada Klasifikasi Penyakit Diabetes
## Dosen Pengampu : Andika Setiawan, S.Kom., M.Cs.
## Asisten Dosen : M. Rizki Alfaina
## Anggota Kelompok : 

| No. | Nama                             | NIM        |
|-----|----------------------------------|------------|
| 1   | Mychael Daniel N.                | 122140104  |
| 2   | Reynaldi Cristian Simamora       | 122140116  |
| 3   | Ichsan Kuntadi Baskara           | 122140117  |
| 4   | Fajrul Ramadhana Aqsa            | 122140118  |
| 5   | Lois Novel E. Gurning            | 122140098  |
| 6   | Febriani Nawang Wulan S.         | 122140071  |
| 7   | Lucky Immanuel Sitanggang        | 122140179  |

## 🎯 Tujuan Penelitian

Penelitian ini bertujuan untuk membandingkan efektivitas dua algoritma machine learning, yaitu **Extreme Gradient Boosting (XGBoost)** dan **Multi-Layer Perceptron (MLPClassifier)**, dalam melakukan **klasifikasi penyakit diabetes** berdasarkan data klinis pasien.

Secara khusus, penelitian ini memiliki beberapa tujuan berikut:

1. **Menganalisis** performa model XGBoost dan MLP dalam mengklasifikasikan pasien ke dalam kategori diabetes atau non-diabetes.
2. **Mengukur** efektivitas masing-masing model menggunakan metrik evaluasi seperti akurasi, precision, recall, dan f1-score.
3. **Menentukan** model yang paling optimal untuk diterapkan pada sistem pendukung keputusan medis dalam konteks prediksi diabetes.
4. **Mengevaluasi** keandalan model melalui teknik visualisasi seperti confusion matrix dan (jika diterapkan) ROC curve.

Diharapkan hasil dari penelitian ini dapat menjadi acuan dalam pengembangan sistem deteksi dini diabetes yang berbasis kecerdasan buatan.

## 📚 Latar Belakang

Diabetes merupakan salah satu penyakit kronis yang memiliki prevalensi tinggi secara global, termasuk di Indonesia. Deteksi dini terhadap penyakit ini sangat penting untuk mencegah komplikasi serius seperti gagal ginjal, penyakit jantung, dan neuropati.

Dengan semakin berkembangnya teknologi dan ketersediaan data medis, penerapan algoritma machine learning dapat membantu dalam proses klasifikasi dan prediksi risiko diabetes. Namun, berbagai algoritma memiliki keunggulan dan kelemahan masing-masing.

Penelitian ini fokus pada dua algoritma populer, yaitu:
- **XGBoost (Extreme Gradient Boosting)**: merupakan algoritma boosting berbasis pohon keputusan yang bekerja secara iteratif dengan membangun model baru untuk memperbaiki kesalahan prediksi model sebelumnya. Setiap pohon fokus pada data yang sulit diklasifikasikan oleh pohon sebelumnya, dan hasil akhir merupakan gabungan dari seluruh pohon. XGBoost menggunakan teknik regularisasi untuk mencegah overfitting serta memiliki optimisasi paralel dan penanganan missing value yang efisien.
- **MLPClassifier (Multi-Layer Perceptron)**: adalah jaringan saraf berlapis-lapis yang terdiri dari input layer, satu atau lebih hidden layer, dan output layer. Data diproses secara bertahap melalui lapisan-lapisan ini menggunakan fungsi aktivasi nonlinear seperti ReLU atau sigmoid. Model belajar dengan menyesuaikan bobot melalui proses backpropagation dan optimisasi gradien untuk meminimalkan loss function, sehingga mampu menangkap hubungan kompleks antar fitur dalam data.
Perbandingan performa keduanya akan memberikan wawasan tentang model mana yang lebih optimal untuk diterapkan dalam sistem deteksi dini penyakit diabetes.


## 🛠️ Metodologi

Langkah-langkah dalam penelitian ini meliputi:

1. **Pengumpulan Data**  
   Dataset yang digunakan berisi data pasien dengan fitur-fitur medis seperti id, no urut pasien, jenis kelamin, usia, kadar urea, kadar kreatinin, hemoglobin terglikasi, kolesterol, trigliserida, hdl, ldl, vldl, dan indeks massa tubuh. Total jumlah data ada sebanyak 1000 dan 14 kolom yang disebut di atas. Diambil dari data rumah sakit Al-Kindy Teaching Hospital.

2. **Preprocessing**
   - Penghapusan label seperti `ID`, dan `No_Pation`.
   - Penghapusan data duplikat selain kolom `CLASS`
   - Encoding variabel kategorik seperti `Gender` dan `CLASS`
   - Pemisahan kelas fitur dan target
   - Standardisasi fitur numerik menggunakan `StandardScaler`
   - Split data menjadi data latih dan uji dengan rasio 80:20
   - Dan operasi SMOTE untuk data training untuk keseimbangan data

4. **Pemodelan**  
   - Model 1: `XGBoostClassifier` dari library `xgboost`
   - Model 2: `MLPClassifier` dari library `sklearn.neural_network`

5. **Evaluasi**  
   Metrik evaluasi yang digunakan:
   - **Accuracy**
   - **Precision**
   - **Recall**
   - **F1-score**
   - **Confusion Matrix**
  
## 🚀 Hasil Akhir
1. Dari Metode XGBoost di dapat akurasi trainingnya 100%. Dan data testing mendapatkan hasil 98.80%.
2. Dari metode MLPClassifier didapat akurasi trainingnya 97.78%, dan data testingnya 95.21%.

| Model         | Akurasi Training | Akurasi Testing |
|---------------|------------------|-----------------|
| XGBoost       | 100%             | 98.80%          |
| MLPClassifier | 97.78%           | 95.21%          |

XGBoost lebih unggul dibandingkan MLPClassifier karena lebih cocok untuk data tabular seperti fitur medis, memiliki kemampuan menangani missing value dan outlier, serta dilengkapi dengan regularisasi dan mekanisme boosting yang mencegah overfitting. Selain itu, XGBoost lebih mudah dituning dan memberikan hasil yang lebih stabil pada data tidak seimbang, sementara MLP lebih sensitif terhadap parameter dan cenderung kurang optimal untuk klasifikasi data tabular.
