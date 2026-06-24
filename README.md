# Project-Machine-Learning-kelompok-A
## 📌 Deskripsi Proyek
Proyek ini mengimplementasikan alur kerja *Machine Learning* ujung-ke-ujung (*End-to-End*) untuk memprediksi tingkat pendapatan individu. Masalah ini dirumuskan ke dalam bentuk **Klasifikasi Biner** ($\le50\text{K}$ USD vs $>50\text{K}$ USD per tahun) berdasarkan karakteristik sosio-demografi individu. 

Fokus utama proyek ini terletak pada **kebenaran metodologi**, seperti penanganan kualitas data mentah yang aman dari kebocoran informasi (*data leakage*), penyelesaian masalah ketidakseimbangan kelas (*class imbalance*), serta optimasi model agar menghasilkan prediksi yang adil, objektif, dan bebas dari *overfitting*.

# Nama Anggota Kelompok: 
1. Carrisa Putri Arabella			  (K1D024019)
2. Faricha Cahya Metia 			    (K1D024023)
3. Fatihaturrohmah       		  	(K1D024035)
4. Aditya Febrio Setiawan	 	    (K1D024036)
5. Andhika Pradana Rahma Dhany	(K1D024038)

---

## 📊 Sumber Dataset
Dataset yang digunakan dalam proyek ini adalah **Adult Census Income Dataset**
* **Karakteristik Data:** Memiliki **48.842 baris data** (*instances*) dan **14 fitur prediktor** dengan tipe data campuran (kategorikal dan integer).
* **Target Prediksi:** Menentukan apakah pendapatan seseorang melebihi $50.000 per tahun ($>50\text{K}$ USD vs $\le50\text{K}$ USD).
* **Tautan Resmi Sumber Data:**
  * **UCI ML Repository:** [Adult Dataset - UCI](https://archive.ics.uci.edu/dataset/2/adult)
  * **Kaggle Mirror:** [Adult Census Income - Kaggle](https://www.kaggle.com/datasets/uciml/adult-census-income)
* **Fitur Utama:** Usia (*age*), tingkat pendidikan (*education*), status pernikahan (*marital-status*), jenis pekerjaan (*occupation*), jam kerja per minggu (*hours-per-week*), dll.
