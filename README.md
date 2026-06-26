# Prediksi Indeks Ketahanan Pangan (IKP) Menggunakan Machine Learning Regresi

## Deskripsi Project

Project ini bertujuan untuk membangun model machine learning regresi yang dapat memprediksi nilai Indeks Ketahanan Pangan (IKP) pada tingkat kabupaten/kota di Indonesia.

Prediksi dilakukan berdasarkan indikator sosial-ekonomi, kesehatan, pendidikan, dan infrastruktur yang berkaitan dengan ketahanan pangan. Project ini menggunakan dataset FSVA Indonesia tahun 2021–2024 dengan target berupa nilai IKP.

Metode yang digunakan dalam project ini mengikuti alur CRISP-DM, yaitu:

1. Business Understanding
2. Data Understanding
3. Data Preparation
4. Modeling
5. Evaluation
6. Deployment atau dokumentasi hasil

Model yang digunakan dan dibandingkan dalam project ini adalah:

1. Baseline Model atau Dummy Regressor
2. Linear Regression
3. Random Forest Regressor
4. Gradient Boosting Regressor
5. Gradient Boosting Regressor dengan Hyperparameter Tuning

## Anggota Tim

Project ini dikerjakan oleh Kelompok G - Machine Learning.

1. Nailah Khusnul M.S (K1D024049)
2. Anneke Alya Shantika (K1D024056)
3. Riani Kurnia Agustina (K1D024059)
4. Pandu Atini Estikandari (K1D024061)

## Sumber Dataset

Dataset yang digunakan berasal dari FSVA (Food Security and Vulnerability Atlas) Indonesia yang diterbitkan oleh Badan Pangan Nasional (Bapanas) bersama World Food Programme (WFP) Indonesia.

Sumber dataset:

https://www.badanpangan.go.id

Dataset yang digunakan mencakup data ketahanan pangan tingkat kabupaten/kota di Indonesia pada periode 2021 sampai 2024.

## Informasi Dataset

Informasi umum dataset yang digunakan adalah sebagai berikut:

1. Sumber data: FSVA, Badan Pangan Nasional dan WFP Indonesia
2. Periode data: 2021, 2022, 2023, dan 2024
3. Jumlah observasi: 2.056 baris
4. Jumlah wilayah: 514 kabupaten/kota
5. Jumlah provinsi: 34 provinsi
6. Jumlah kolom: 17 kolom
7. Variabel target: IKP
8. Jenis permasalahan: Regresi
9. Rentang target: 0 sampai 100

## Data Dictionary

Dataset terdiri dari beberapa variabel berikut:

1. `Tahun`

   Tahun pengamatan data, yaitu 2021 sampai 2024.

2. `Sumber_File`

   Nama file sumber data. Kolom ini tidak digunakan dalam pemodelan.

3. `Wilayah`

   Nama kabupaten/kota. Kolom ini digunakan sebagai fitur kategorik dan diproses menggunakan encoding.

4. `Provinsi`

   Nama provinsi dari setiap kabupaten/kota. Kolom ini tidak digunakan dalam pemodelan utama.

5. `NCPR`

   Normalized Caloric Poverty Ratio, yaitu indikator yang berkaitan dengan kecukupan konsumsi kalori.

6. `Kemiskinan (%)`

   Persentase penduduk miskin pada suatu wilayah.

7. `Pengeluaran Pangan (%)`

   Persentase pengeluaran masyarakat untuk kebutuhan pangan.

8. `Tanpa Listrik (%)`

   Persentase rumah tangga yang tidak memiliki akses listrik.

9. `Tanpa Air Bersih (%)`

   Persentase rumah tangga yang tidak memiliki akses air bersih.

10. `Lama Sekolah Perempuan`

    Rata-rata lama sekolah perempuan.

11. `Rasio Tenaga Kesehatan`

    Rasio jumlah tenaga kesehatan terhadap jumlah penduduk.

12. `Angka Harapan Hidup`

    Angka harapan hidup saat lahir.

13. `Stunting (%)`

    Persentase prevalensi stunting pada balita.

14. `IKP`

    Indeks Ketahanan Pangan. Kolom ini digunakan sebagai variabel target.

15. `IKP Ranking`

    Ranking berdasarkan nilai IKP. Kolom ini dihapus karena berpotensi menyebabkan data leakage.

16. `Komposit`

    Skor komposit komponen IKP. Kolom ini dihapus karena berpotensi menyebabkan data leakage.

17. `Kategori`

    Kategori ketahanan pangan. Kolom ini tidak digunakan dalam pemodelan utama.

## Tujuan Project

Tujuan dari project ini adalah:

1. Menganalisis karakteristik dataset FSVA Indonesia tahun 2021 sampai 2024.
2. Melakukan Exploratory Data Analysis (EDA) untuk memahami distribusi data dan hubungan antarvariabel.
3. Melakukan preprocessing data agar dataset siap digunakan dalam pemodelan.
4. Membangun model machine learning regresi untuk memprediksi nilai IKP.
5. Membandingkan performa beberapa model regresi.
6. Melakukan hyperparameter tuning pada model terbaik.
7. Mengidentifikasi fitur yang paling berpengaruh terhadap prediksi IKP.
8. Menyusun ringkasan hasil model sebagai dasar interpretasi ketahanan pangan.

## Tahapan Project

Tahapan yang dilakukan dalam project ini adalah sebagai berikut:

1. Import library yang dibutuhkan.
2. Load dataset FSVA Indonesia 2021–2024.
3. Melakukan eksplorasi data awal.
4. Melakukan analisis statistik deskriptif.
5. Memeriksa missing values.
6. Memeriksa data duplikat.
7. Menganalisis distribusi variabel target IKP.
8. Menganalisis distribusi fitur numerik.
9. Melakukan analisis korelasi antarvariabel.
10. Melakukan uji korelasi Spearman.
11. Mendeteksi dan menangani outlier.
12. Menghapus kolom yang berpotensi menyebabkan data leakage.
13. Melakukan encoding pada variabel kategorik.
14. Melakukan feature scaling.
15. Melakukan feature engineering.
16. Membagi data menjadi data training dan testing.
17. Melatih beberapa model regresi.
18. Mengevaluasi performa model.
19. Melakukan hyperparameter tuning.
20. Menganalisis feature importance.
21. Menyusun kesimpulan hasil model.

## Preprocessing Data

Tahapan preprocessing yang dilakukan meliputi:

1. Pemeriksaan Missing Values

   Hasil pemeriksaan menunjukkan bahwa tidak terdapat missing values pada dataset.

2. Pemeriksaan Data Duplikat

   Hasil pemeriksaan menunjukkan bahwa tidak terdapat data duplikat.

3. Penanganan Outlier

   Outlier dideteksi menggunakan metode IQR atau Interquartile Range. Outlier pada fitur numerik ditangani menggunakan metode winsorizing atau capping.

4. Penghapusan Kolom Data Leakage

   Kolom `IKP Ranking` dan `Komposit` dihapus karena memiliki hubungan langsung dengan target IKP dan dapat menyebabkan data leakage.

5. Encoding

   Kolom `Wilayah` yang berbentuk kategorik diubah menjadi bentuk numerik menggunakan Label Encoding.

6. Feature Scaling

   Feature scaling dilakukan menggunakan StandardScaler agar skala antarfitur menjadi sebanding.

7. Feature Engineering

   Dibuat tiga fitur baru, yaitu:

   - `Kemiskinan_Stunting`
   - `AHH_Sekolah`
   - `Air_Listrik`

## Feature Engineering

Fitur tambahan yang dibuat dalam project ini adalah:

1. `Kemiskinan_Stunting`

   Fitur ini merupakan hasil perkalian antara Kemiskinan (%) dan Stunting (%). Fitur ini digunakan untuk merepresentasikan dampak gabungan kemiskinan terhadap kondisi gizi anak.

2. `AHH_Sekolah`

   Fitur ini merupakan hasil perkalian antara Angka Harapan Hidup dan Lama Sekolah Perempuan. Fitur ini digunakan sebagai proksi kualitas hidup dan pendidikan.

3. `Air_Listrik`

   Fitur ini merupakan hasil perkalian antara Tanpa Air Bersih (%) dan Tanpa Listrik (%). Fitur ini digunakan untuk merepresentasikan defisit akses infrastruktur dasar.

Setelah feature engineering, total fitur yang digunakan dalam pemodelan adalah 14 fitur.

## Cara Menjalankan Project

Untuk menjalankan project ini, ikuti langkah-langkah berikut:

1. Clone repository

       git clone https://github.com/annekeshantika-a11y/ml-project-ketahanan-pangan

2. Masuk ke folder project

       cd ml-project-ketahanan-pangan

3. Install library yang dibutuhkan

       pip install pandas numpy matplotlib seaborn scikit-learn scipy

4. Jika terdapat file `requirements.txt`, jalankan perintah berikut:

       pip install -r requirements.txt

5. Jalankan Jupyter Notebook

       jupyter notebook

6. Buka file notebook utama, lalu jalankan cell dari awal sampai akhir.

7. Jika project dijalankan dalam bentuk script Python, gunakan perintah:

       python main.py

## Library yang Digunakan

Library Python yang digunakan dalam project ini antara lain:

1. pandas
2. numpy
3. matplotlib
4. seaborn
5. scikit-learn
6. scipy

## Model yang Digunakan

Model machine learning yang digunakan adalah:

1. Baseline Model

   Baseline model menggunakan DummyRegressor dengan strategi mean. Model ini digunakan sebagai pembanding dasar.

2. Linear Regression

   Linear Regression digunakan sebagai model regresi linear untuk melihat hubungan linear antara fitur dan target IKP.

3. Random Forest Regressor

   Random Forest merupakan model ensemble berbasis bagging yang menggunakan banyak decision tree untuk menghasilkan prediksi yang lebih stabil.

4. Gradient Boosting Regressor

   Gradient Boosting merupakan model ensemble berbasis boosting yang membangun model secara bertahap untuk memperbaiki kesalahan prediksi dari model sebelumnya.

5. Gradient Boosting dengan Hyperparameter Tuning

   Model Gradient Boosting dioptimalkan menggunakan GridSearchCV untuk mendapatkan kombinasi parameter terbaik.

## Hasil Exploratory Data Analysis

Hasil eksplorasi data menunjukkan bahwa dataset memiliki 2.056 observasi dari 514 kabupaten/kota di Indonesia selama periode 2021 sampai 2024.

Karakteristik variabel target IKP adalah:

1. Nilai minimum: 14,14
2. Nilai maksimum: 96,37
3. Mean: 73,38
4. Median: 77,60
5. Standar deviasi: 14,58
6. Skewness: -1,74

Distribusi IKP menunjukkan pola left-skewed atau condong ke kiri. Hal ini menunjukkan bahwa sebagian besar wilayah memiliki nilai IKP relatif tinggi, tetapi masih terdapat beberapa wilayah dengan nilai IKP rendah.

## Hasil Cross-Validation

Evaluasi awal dilakukan menggunakan 5-Fold Cross-Validation pada training set.

Hasil cross-validation:

1. Baseline Model

   CV R² Mean = -0,0021

2. Linear Regression

   CV R² Mean = 0,8293

3. Random Forest

   CV R² Mean = 0,9692

4. Gradient Boosting

   CV R² Mean = 0,9779

Berdasarkan hasil cross-validation, Gradient Boosting memperoleh nilai R² tertinggi dan menunjukkan performa paling stabil dibandingkan model lainnya.

## Hasil Evaluasi Model

Evaluasi model dilakukan menggunakan metrik MAE, RMSE, MAPE, dan R².

Hasil evaluasi model pada test set adalah:

| Model | MAE | RMSE | MAPE | R² |
|---|---:|---:|---:|---:|
| Baseline | 10,6301 | 14,8091 | 21,67% | -0,0009 |
| Linear Regression | 4,3241 | 6,6115 | 7,91% | 0,8005 |
| Random Forest | 1,6905 | 2,6300 | 3,10% | 0,9668 |
| Gradient Boosting | 1,5779 | 2,3206 | 2,79% | 0,9754 |
| Gradient Boosting Tuned | 1,3232 | 2,2484 | 2,55% | 0,9769 |

Model terbaik adalah Gradient Boosting setelah hyperparameter tuning.

## Hyperparameter Tuning

Hyperparameter tuning dilakukan pada model Gradient Boosting menggunakan GridSearchCV dengan 5-fold cross-validation.

Parameter terbaik yang diperoleh adalah:

1. `n_estimators = 200`
2. `max_depth = 5`
3. `learning_rate = 0,1`
4. `subsample = 0,8`

Setelah tuning, performa model meningkat dari R² sebesar 0,9754 menjadi 0,9769.

## Feature Importance

Berdasarkan hasil feature importance dari model Gradient Boosting setelah tuning, fitur yang paling berpengaruh terhadap prediksi IKP adalah:

1. NCPR
2. Kemiskinan (%)
3. Tanpa Air Bersih (%)
4. Angka Harapan Hidup
5. AHH_Sekolah

Fitur NCPR menjadi fitur paling dominan dalam prediksi IKP karena berkaitan langsung dengan kecukupan konsumsi kalori masyarakat.

## Ringkasan Hasil

Ringkasan hasil dari project ini adalah:

1. Dataset FSVA Indonesia 2021–2024 memiliki kualitas data yang baik karena tidak terdapat missing values dan data duplikat.
2. Distribusi IKP menunjukkan adanya disparitas ketahanan pangan antarwilayah.
3. Model ensemble memiliki performa lebih baik dibandingkan model linear.
4. Gradient Boosting menjadi model terbaik sebelum tuning.
5. Gradient Boosting setelah hyperparameter tuning memberikan performa terbaik secara keseluruhan.
6. Model terbaik menghasilkan nilai R² sebesar 0,9769 dan MAPE sebesar 2,55%.
7. Fitur paling berpengaruh terhadap prediksi IKP adalah NCPR, Kemiskinan (%), dan Tanpa Air Bersih (%).
8. Model tidak menunjukkan indikasi overfitting yang signifikan.

## Kesimpulan

Project ini berhasil membangun model prediksi Indeks Ketahanan Pangan (IKP) menggunakan pendekatan machine learning regresi.

Berdasarkan hasil evaluasi, model Gradient Boosting dengan hyperparameter tuning memberikan performa terbaik dibandingkan model lainnya. Model terbaik menghasilkan nilai R² sebesar 0,9769, MAE sebesar 1,3232, RMSE sebesar 2,2484, dan MAPE sebesar 2,55%.

Hasil tersebut menunjukkan bahwa model mampu memprediksi nilai IKP dengan tingkat akurasi yang sangat baik. Selain itu, hasil feature importance menunjukkan bahwa NCPR merupakan indikator yang paling dominan dalam memengaruhi prediksi IKP.

Model ini dapat digunakan sebagai pendekatan awal untuk membantu analisis ketahanan pangan wilayah, mengidentifikasi daerah yang berisiko, serta mendukung pengambilan keputusan berbasis data dalam bidang ketahanan pangan.

## Repository

Link repository project:

https://github.com/annekeshantika-a11y/ml-project-ketahanan-pangan
