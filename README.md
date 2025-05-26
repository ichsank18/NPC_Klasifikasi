# NPC_Klasifikasi

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
- **XGBoost (Extreme Gradient Boosting)**: algoritma ensemble yang dikenal karena akurasinya tinggi dan efisiensi tinggi dalam berbagai kompetisi ML.
- **MLPClassifier (Multi-Layer Perceptron)**: model neural network sederhana yang mampu mempelajari pola nonlinear dalam data.

Perbandingan performa keduanya akan memberikan wawasan tentang model mana yang lebih optimal untuk diterapkan dalam sistem deteksi dini penyakit diabetes.


## 🛠️ Metodologi

Langkah-langkah dalam penelitian ini meliputi:

1. **Pengumpulan Data**  
   Dataset yang digunakan berisi data pasien dengan fitur-fitur medis seperti usia, jenis kelamin, kadar gula darah, kolesterol, indeks massa tubuh (BMI), dll.

2. **Preprocessing**  
   - Encoding variabel kategorik seperti `Gender` dan `CLASS`
   - Standardisasi fitur numerik menggunakan `StandardScaler`
   - Split data menjadi data latih dan uji dengan rasio 80:20

3. **Pemodelan**  
   - Model 1: `XGBoostClassifier` dari library `xgboost`
   - Model 2: `MLPClassifier` dari library `sklearn.neural_network`

4. **Evaluasi**  
   Metrik evaluasi yang digunakan:
   - **Accuracy**
   - **Precision**
   - **Recall**
   - **F1-score**
   - **Confusion Matrix**
