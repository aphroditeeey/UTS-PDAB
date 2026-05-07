# UTS Penambangan Data dan Analisis Bisnis

## Prediksi kualitas wine menggunakan machine learning Random Forest Classifier.

Nama         : Aphrodiva Delovi

NIM          : 2404220038

Mata Kuliah  : Penambangan Data dan Analisis Bisnis


## Import Library

Library yang digunakan meliputi pandas dan numpy untuk pengolahan data, serta library dari scikit-learn untuk proses machine learning seperti pembagian data, scaling, pembuatan model, dan evaluasi model.


## Load Dataset

Dataset training dan testing dibaca menggunakan pandas. Dataset training digunakan untuk melatih model, sedangkan dataset testing digunakan untuk melakukan prediksi kualitas wine.


## Eksplorasi Data

Tahap ini dilakukan untuk melihat struktur dataset, jumlah variabel, tipe data, serta beberapa data awal.


## Pengecekan Missing Value

Pengecekan missing value dilakukan untuk memastikan tidak terdapat data kosong yang dapat memengaruhi performa model.


## Pengecekan Missing Value

Pengecekan missing value dilakukan untuk memastikan tidak terdapat data kosong yang dapat memengaruhi performa model.

Interpretasi: Berdasarkan hasil pengecekan, seluruh variabel memiliki jumlah missing value sebesar 0. Hal ini menunjukkan bahwa dataset sudah bersih sehingga tidak diperlukan penanganan missing value lebih lanjut.


## Pemisahan Fitur dan Target

Variabel `quality` digunakan sebagai target prediksi, sedangkan variabel lainnya digunakan sebagai fitur. Kolom `Id` tidak digunakan dalam pemodelan karena hanya berfungsi sebagai identitas data.


## Pembagian Data Training dan Validation

Dataset training dibagi menjadi data training dan validation dengan proporsi 80:20. Pembagian ini dilakukan untuk mengevaluasi performa model pada data yang belum pernah dilihat sebelumnya.


## Feature Scaling

Standardisasi dilakukan menggunakan StandardScaler agar setiap fitur memiliki skala yang sebanding sehingga membantu meningkatkan performa model machine learning.


## Pembuatan Model Random Forest

Model Random Forest Classifier digunakan karena mampu menangani data numerik dengan baik dan memiliki performa yang cukup stabil pada kasus klasifikasi.


## Evaluasi Model

Evaluasi dilakukan menggunakan accuracy score, classification report, dan confusion matrix untuk mengetahui performa model dalam melakukan klasifikasi kualitas wine.

Interpretasi: Nilai accuracy menunjukkan tingkat ketepatan model dalam memprediksi kualitas wine. Semakin tinggi nilai accuracy, maka performa model semakin baik dalam melakukan klasifikasi.


## Prediksi Data Testing

Model yang telah dilatih digunakan untuk memprediksi nilai quality pada dataset testing.


## Menyimpan Hasil Prediksi

Hasil prediksi disimpan dalam format CSV yang berisi kolom Id dan quality sesuai format yang diminta.


## Kesimpulan

Model Random Forest Classifier berhasil digunakan untuk memprediksi kualitas wine berdasarkan karakteristik kimiawi yang terdapat pada dataset. Berdasarkan hasil evaluasi, model menunjukkan performa yang cukup baik dalam melakukan klasifikasi kualitas wine.
