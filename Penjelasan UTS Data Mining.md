# DATA-MINING_UTS_04TPLP024
Nama: Muhamad Pahri, Nim: 231011400999, Kelas: 04TPLP024, Matkul: Data Mining

Penjelasan Uts Data Mining

Judul Proyek:
Klasifikasi Serangan DDoS menggunakan Algoritma Decision Tree

Deskripsi Singkat:
Dalam proyek ini, dilakukan analisis dan klasifikasi data serangan DDoS menggunakan algoritma Decision Tree Classifier dari pustaka Scikit-learn. Dataset yang digunakan terdiri dari dua jenis serangan DDoS, yaitu ICMP Flood dan UDP Flood, yang digabungkan untuk membentuk satu dataset besar.

Langkah-langkah yang dilakukan:

Ekstraksi Dataset:
File ZIP berisi dataset diekstrak menggunakan modul zipfile.
Dataset utama yang digunakan adalah DDoS ICMP Flood.csv dan DDoS UDP Flood.csv.

Penggabungan Data:
Dataset DDoS ICMP Flood.csv dibaca dua kali dan digabung dengan DDoS UDP Flood.csv menggunakan pd.concat() untuk membentuk hasilgabung.

Seleksi Fitur dan Label:
Fitur diambil dari kolom ke-7 sampai ke-75.
Label diambil dari kolom ke-83.

Pemodelan:
Data dibagi menjadi data latih dan uji dengan proporsi 80:20 menggunakan train_test_split().
Model klasifikasi dibangun menggunakan DecisionTreeClassifier dengan kriteria entropy dan metode split acak.

Evaluasi Model:
Prediksi dilakukan terhadap data uji.
Akurasi model dihitung menggunakan accuracy_score.
Visualisasi pohon keputusan dilakukan dengan tree.plot_tree().
Evaluasi lebih lanjut dilakukan dengan menampilkan confusion matrix menggunakan seaborn.heatmap().

Eksplorasi Data Tambahan:
Dataset yang telah digabung juga dibagi menjadi dua bagian secara horizontal (kiri dan kanan) berdasarkan jumlah kolom untuk analisis visual atau pemahaman data lebih lanjut.

Output Utama:
Akurasi model klasifikasi
Visualisasi decision tree
Confusion matrix antar kelas (Benign, DDoS ICMP, DDoS UDP)
