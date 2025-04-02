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
- Jawaban pernyataan masalah 1
- Jawaban pernyataan masalah 2


    ### Solution statements
    - Menghapus Colom yang tidak dibtuhkan yaitu presentasi resiko diabetes
    - melakukan cleaning data dengan menghilangkan missing value yang ada dan menghapus duplikat dari data
    - melakukan splitt data dengan rasio 80% data training dan 20% data testing 
    - melakukan evaluasi dengan confussion matriks
