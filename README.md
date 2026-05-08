# UTS Penambangan Data dan Analisis Bisnis

## Prediksi kualitas wine menggunakan machine learning Random Forest Classifier.

Nama         : Aphrodiva Delovi

NIM          : 2404220038

Program Studi: Statistika dan Sains Data

Mata Kuliah  : Penambangan Data dan Analisis Bisnis


## Import Library

Library yang digunakan meliputi pandas dan numpy untuk pengolahan data, serta library dari scikit-learn untuk proses machine learning seperti pembagian data, scaling, pembuatan model, dan evaluasi model.


## Load Dataset

Dataset training dan testing dibaca menggunakan pandas. Dataset training digunakan untuk melatih model, sedangkan dataset testing digunakan untuk melakukan prediksi kualitas wine.


## Eksplorasi Data

Tahap ini dilakukan untuk melihat struktur dataset, jumlah variabel, tipe data, serta beberapa data awal.

Interpretasi: Berdasarkan hasil eksplorasi data, dataset terdiri dari beberapa variabel numerik yang menggambarkan karakteristik kimiawi wine, seperti acidity, chlorides, alcohol, dan sulphates. Variabel target yang diprediksi adalah `quality`. Seluruh variabel memiliki tipe data numerik sehingga dapat langsung digunakan pada proses machine learning tanpa perlu encoding tambahan.


## Pengecekan Missing Value

Pengecekan missing value dilakukan untuk memastikan tidak terdapat data kosong yang dapat memengaruhi performa model.

Interpretasi: Hasil pengecekan menunjukkan bahwa seluruh variabel memiliki jumlah missing value sebesar 0. Hal ini menunjukkan bahwa dataset berada dalam kondisi baik dan tidak memerlukan proses imputasi maupun penghapusan data.


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

Interpretasi:

### Accuracy
Hasil evaluasi menunjukkan bahwa model Random Forest Classifier memperoleh nilai accuracy sebesar 61,63%. Hal ini berarti model mampu memprediksi kualitas wine dengan benar sebanyak sekitar 61% dari total data validation. Nilai accuracy tersebut menunjukkan bahwa model memiliki performa yang cukup baik dalam mengenali pola hubungan antara karakteristik kimiawi wine dengan kualitasnya, meskipun masih terdapat beberapa kesalahan klasifikasi pada beberapa kelas kualitas wine.

### Classification Report
Berdasarkan classification report, model memiliki performa yang cukup baik pada kelas kualitas wine 5 dan 6, yang terlihat dari nilai precision, recall, dan f1-score yang relatif lebih tinggi dibandingkan kelas lainnya.

Pada kelas quality 5, model memperoleh recall sebesar 67%, yang menunjukkan bahwa sebagian besar data dengan kualitas 5 berhasil dikenali dengan baik oleh model. Sementara pada kelas quality 6, model memperoleh recall sebesar 68%, yang menunjukkan kemampuan model yang cukup baik dalam mendeteksi kelas tersebut.

Namun, model masih mengalami kesulitan dalam memprediksi kelas quality 4 dan 8. Hal ini terlihat dari nilai precision dan recall yang bernilai 0. Kondisi tersebut kemungkinan disebabkan oleh jumlah data pada kelas tersebut yang sangat sedikit sehingga model kurang mampu mempelajari pola datanya dengan baik.

Nilai weighted average f1-score sebesar 60% menunjukkan bahwa secara keseluruhan model memiliki performa klasifikasi yang cukup baik pada seluruh kelas kualitas wine.

### Confusion Matrix
Berdasarkan confusion matrix, sebagian besar prediksi benar berada pada diagonal utama, terutama pada kelas quality 5 dan 6. Hal ini menunjukkan bahwa model cukup baik dalam mengenali kedua kelas tersebut.

Pada kelas quality 5, model berhasil memprediksi benar sebanyak 45 data dari total 67 data. Sedangkan pada kelas quality 6, model berhasil memprediksi benar sebanyak 53 data dari total 78 data.

Namun, masih terdapat beberapa kesalahan klasifikasi antar kelas yang berdekatan, terutama antara quality 5 dan 6. Hal ini menunjukkan bahwa karakteristik kimiawi pada kedua kelas memiliki kemiripan sehingga model mengalami kesulitan dalam membedakannya secara sempurna.

Selain itu, model tidak berhasil memprediksi dengan benar kelas quality 4 dan 8 karena jumlah data pada kelas tersebut sangat sedikit dibandingkan kelas lainnya.


## Prediksi Data Testing

Model yang telah dilatih digunakan untuk memprediksi nilai quality pada dataset testing.

Interpretasi: Hasil prediksi menunjukkan estimasi kualitas wine berdasarkan karakteristik kimiawi yang dimiliki masing-masing sampel pada dataset testing.


## Menyimpan Hasil Prediksi

Hasil prediksi disimpan dalam format CSV yang berisi kolom Id dan quality sesuai format yang diminta.


## Kesimpulan

Model Random Forest Classifier berhasil digunakan untuk memprediksi kualitas wine berdasarkan karakteristik kimiawi yang terdapat pada dataset. Berdasarkan hasil evaluasi, model menunjukkan performa yang cukup baik dalam melakukan klasifikasi kualitas wine.
