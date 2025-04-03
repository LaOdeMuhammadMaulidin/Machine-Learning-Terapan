# Laporan Proyek Machine Learning - La Ode Muhammad Maulidin

## Domain Proyek

Pada saat ini, penyakit stroke menjadi penyakit yang bisa berpotensi menyebabkan kematian. Di seluruh dunia, jumlah kasus stroke terus meningkat, dan memahami faktor-faktor yang mempengaruhi resiko kematian pada pasien stroke adalah langkah penting dalam penanganan dan perawatan yang lebih baik. Stroke adalah tanda-tanda klinis yang terjadi secara cepat atau mendadak berupa defisit fokal (atau global) pada fungsi otak, dengan gejala yang berlangsung selama 24 jam atau lebih atau menyebabkan kematian, tanpa penyebab yang jelas selain penyebab vaskuler (WHO). Menurut data World Health Organization (WHO) diperkirakan 17,5 juta orang meninggal dunia akibat penyakit kardiovaskular dengan 6,7 juta orang meninggal akibat stroke, yaitu urutan kedua tertinggi mengakibatkan kematian setelah penyakit jantung koroner. 

dengan perkembangan teknologi yang semakin pesat kita dapat dengan mudah mengetahui resiko terkena stroke dengan beberapa gejala yang di alami. salah satu metode tersebut adalah machine learning yang merupakan proses belajar komputer tanpa harus di program secara eksplisit. dengan adanya ML kita dapat mengetahui serta mengklasifikasikan apakah kita beresiko stroke atau tidak
  
[Prediksi Penyakit Stroke Menggunakan Machine Learning Dengan Algoritma Random Forest](https://e-jurnal.pnl.ac.id/infomedia/article/view/5199 ) 

## Business Understanding


### Problem Statements

Beradasarkan latar belakang di atas didapatkan rincian masalah:
- Bagaimana melakukan preprocessing untuk membuat model machine learning yang baik?
- Bagaimana melakukan evaluasi terhadap model ML yang telah di buat menggunakan model random forest?

### Goals

Menjelaskan tujuan dari pernyataan masalah:
- untuk melakukan preprocessing untuk membuat model machine learning yang baik
- Untuk melakukan evaluasi terhadap model ML yang telah di buat menggunakan model random forest


    ### Solution statements
    - Menghapus Colom yang tidak dibtuhkan yaitu presentasi resiko diabetes
    - melakukan cleaning data dengan menghilangkan missing value yang ada dan menghapus duplikat dari data
    - melakukan splitt data dengan rasio 80% data training dan 20% data testing 
    - melakukan evaluasi dengan confussion matriks

## Data Understanding

 Dataset ini di dapatkan di [Kaggle] https://www.kaggle.com/datasets/mahatiratusher/stroke-risk-prediction-dataset-v2 
 ![img](https://github.com/user-attachments/assets/5dbead7e-47c9-4ada-8bac-b4bd7c69aa5d)
### Variabel-variabel pada dataset adalah sebagai berikut:
- age : merupakan variabel yang menampilkan umur seseorang.
- gender : merupakan variabel yang menampilkan jenis kelamin seseorang.
- chest pain : merupakan variabel yang menunjukan apakah seseorang mengalami sakit pada dada atau tidak.
- high_blood_pressure:  merupakan variabel apakah tekanan darah tinggi atau tidak
- irregular_heartbeat : merupakan variabel apakah detak jantung tidak normal atau normal
- shortness_of_breath : merupakan variabel apakah bernafas dengan baik atau tidak
- fatigue_weakness    : merupakan variabel apakah sering lelah atau tidak
- dizziness : merupakan variabel apakah sering pusing atau tidak
- swelling_edema : merupakan variabel apakah mengalami pembengkakkan edema atau tidak
- neck_jaw_pain : merupakan variabel apakah mnderita sakit pada rahang atau tidak
- excessive_sweating : merupakan variabel apakah bekeringat berlebih atau tidak
- persistent_cough merupakan variabel apakah menderita batuk atau tidak
- nausea_vomiting: merupakan variabel apakah menderita mual dan mutah atau tidak
- chest_discomfort: merupakan variabel apakah dada merasa nyaman atau tidak
- cold_hands_feet: merupakan variabel apakah tangan dan kaki dingin atau tidak
- snoring_sleep_apnea: merupakan variabel apakah mendengkur saat tidur atau tidak
- anxiety_doom: merupakan variabel apakah mengalami kecemasan berlebih atau tidak
- stroke_risk_percentage: merupakan presentasi dari resiko stroke
- at_risk: merupakan variabel apakah beresiko stroke atau tidak

## Data Preparation
Berikut adalah tahapan-tahapan dalam melakukan pra-pemrosesan data:
- Meload Dataset ke dalam sebuah Dataframe menggunakan pandas
- menghapus kolom yang tidak digunakan dan kali ini yang di hapus adalah kolom stroke_risk_percentage
- ``` df.info()``` digunakan untuk mengecek tipe kolom pada dataset
- ```df.isna().sum()``` digunakan untuk mengecek apakah ada kolom yg kosong, dan ketika ada missing value maka di atasi dengan   ``` df.dropna(inplace=True)``` 
- ```df.describe()``` digunakan utk mendapatkan info mengenai dataset terhadap nilai rata-rata, median, banyaknya data, nilai Q1 hingga Q3 dan lain-lain
- melakukan pengecekan duplikat dengan ```df.duplicated().sum()``` dan penghapusan duplikat dengan ```df.drop_duplicates(inplace=True)```
- Melakukan mapping terhadap kolom diagnosis dari type object ke numerik agar bisa dibaca mesin. Dimana pada kolom age Male  diubah ke nilai 1 female diubah ke nilai 0
- Melakukan pengecekkan distribusi kelas target serta membagi data menjadi data latih dan data test dengan rasio 80 banding 20% serta melihat penyebaran data test dan data latih
![img](https://github.com/user-attachments/assets/27d65e3c-ead1-4371-a470-ce28dcbead0a)

## Modeling
Pada tahap ini dilakukan pembuatan model ML random forest dengan kroteria sebagai berikut : 
!(https://github.com/user-attachments/assets/efd4213d-6bc5-46cb-8cdd-02ef532333ab)

pada gambar di atas model random forest dibangun dengan n estimator 100 serta random state 1


## Evaluation
Pada proyek ini, model yang dikembangkan adalah kasus klasifikasi dan menggunakan metriks akurasi, f1-score, recall dan precision. Berikut hasil pengukuran model yang dipilih yaitu model yang menggunakan algoritma Random Forest
![Metriks Evaluasi](https://github.com/user-attachments/assets/60211e3c-9ab6-48f8-9592-0d10bf9cf8c0)

-Akurasi Akurasi merupakan metrik untuk menghitung persentase dari total data yang diidentifikasi dan dinilai benar. Rumus akurasi sebagai berikut : ``` AKURASI = (TP + TN) / (TP+FP+FN+TN)```
* _True Positive_ (TP):
    Kasus dimana model merupakan data positif yang diprediksi benar. Contohnya, pasien menderita stroke (class 1) dan dari model yang dibuat memprediksi pasien tersebut menderita stroke (class 1).
    * _True Negative_ (TN):
    Kasus dimana model merupakan data negatif yang diprediksi benar. Contohnya, pasien tidak menderita stroke (class 2) dan dari model yang dibuat memprediksi pasien tersebut tidak menderita stroke (class 2).
    * _False Positive_ (FP) - **Type I Error** :
    Kasus dimana model merupakan data negatif namun diprediksi sebagai data positif. Contohnya, pasien tidak menderita stroke (class 2) tetapi dari model yang telah memprediksi pasien tersebut menderita stroke (class 1).
    * _False Negative_ (FN) - **Type II Error** :
    Kasus dimana model merupakan data negatif namun diprediksi sebagai data positif. Contohnya, pasien tidak menderita stroke (class 2) tetapi dari model yang telah memprediksi pasien tersebut menderita stroke (class 1).
* _Precision_
    _Precision_ merupakan metrik untuk memprediksi benar positif dari keseluruhan hasil yang diprediksi positf. Rumus _precision_ sebagai berikut: ``` PRECISION = TP / (TP+FP)```
  _Recall_
    _Recall_ merupakan metrik untuk memprediksi benar positif dibandingkan dengan keseluruhan data yang benar positif. Rumus _precision_ sebagai berikut: ``` RECALL = TP / (TP+FN)```
  f1-score_
    _f1-score_ merupakan metrik untuk perbandingan rata-rata precision dan recall yang dibobotkan. Rumus _f1-score_ sebagai berikut: ``` F1 SCORE = 2 * (RECALL * PRECISION) / (RECALL + PRECISION) ```


