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
- ```df.describe()``` digunakan utk mendapatkan info mengenai dataset terhadap nilai rata-rata, median, banyaknya data, nilai Q1 hingga Q3 dan lain-lai
## Modeling
Tahapan ini membahas mengenai model machine learning yang digunakan untuk menyelesaikan permasalahan. Anda perlu menjelaskan tahapan dan parameter yang digunakan pada proses pemodelan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan kelebihan dan kekurangan dari setiap algoritma yang digunakan.
- Jika menggunakan satu algoritma pada solution statement, lakukan proses improvement terhadap model dengan hyperparameter tuning. **Jelaskan proses improvement yang dilakukan**.
- Jika menggunakan dua atau lebih algoritma pada solution statement, maka pilih model terbaik sebagai solusi. **Jelaskan mengapa memilih model tersebut sebagai model terbaik**.

## Evaluation
Pada bagian ini anda perlu menyebutkan metrik evaluasi yang digunakan. Lalu anda perlu menjelaskan hasil proyek berdasarkan metrik evaluasi yang digunakan.

Sebagai contoh, Anda memiih kasus klasifikasi dan menggunakan metrik **akurasi, precision, recall, dan F1 score**. Jelaskan mengenai beberapa hal berikut:
- Penjelasan mengenai metrik yang digunakan
- Menjelaskan hasil proyek berdasarkan metrik evaluasi

Ingatlah, metrik evaluasi yang digunakan harus sesuai dengan konteks data, problem statement, dan solusi yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan formula metrik dan bagaimana metrik tersebut bekerja.

**---Ini adalah bagian akhir laporan---**

_Catatan:_
- _Anda dapat menambahkan gambar, kode, atau tabel ke dalam laporan jika diperlukan. Temukan caranya pada contoh dokumen markdown di situs editor [Dillinger](https://dillinger.io/), [Github Guides: Mastering markdown](https://guides.github.com/features/mastering-markdown/), atau sumber lain di internet. Semangat!_
- Jika terdapat penjelasan yang harus menyertakan code snippet, tuliskan dengan sewajarnya. Tidak perlu menuliskan keseluruhan kode project, cukup bagian yang ingin dijelaskan saja.

