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
* **Target Prediksi:** Menentukan apakah pendapatan seseorang melebihi 50.000 per tahun ($>50\text{K}$ USD vs $\le50\text{K}$ USD).
* **Tautan Resmi Sumber Data:**
  * **UCI ML Repository:** [Adult Dataset - UCI](https://archive.ics.uci.edu/dataset/2/adult)
  * **Kaggle Mirror:** [Adult Census Income - Kaggle](https://www.kaggle.com/datasets/uciml/adult-census-income)
* **Fitur Utama:** Usia (*age*), tingkat pendidikan (*education*), status pernikahan (*marital-status*), jenis pekerjaan (*occupation*), jam kerja per minggu (*hours-per-week*), dll.

## Cara Menjalankan
## 🚀 Cara Menjalankan

[cite_start]Proyek ini dirancang agar dapat dijalankan ulang secara konsisten (*reproducible*)[cite: 24]. Ikuti langkah-langkah berikut untuk mengeksekusi kodingan:

### 1. Instalasi Library
[cite_start]Pastikan Python sudah terinstal. Buka Command Prompt atau Terminal, lalu instal pustaka yang diperlukan menggunakan file `requirements.txt` dengan perintah:
```bash
pip install -r requirements.txt
### 2. Persiapan Data
Unduh dataset Adult Census Income.
## 3. Menjalankan Kode via Jupyter Notebook
## 4. Alternatif via Google Colab

## Ringkasan Hasil
## 📈 Ringkasan Hasil

### 1. Temuan Utama EDA & Feature Importance
* Berdasarkan analisis *Feature Importance* dan SHAP, karakteristik yang paling dominan membedakan tingkat pendapatan individu ($\le50\text{K}$ dan $>50\text{K}$) adalah **relationship**, **education.num** (tingkat pendidikan), **marital.status**, **capital.gain**, serta **hours.per.week** (jam kerja per minggu).

### 2. Prapemrosesan & Mitigasi Bias
* **Prapemrosesan Data:** Penanganan *missing value* menggunakan imputasi modus, menghapus data duplikat, mempertahankan *outlier* yang merepresentasikan kondisi nyata, menerapkan *label encoding* untuk variabel kategorikal, serta melakukan standardisasi pada fitur numerik. Seluruh proses ini dilakukan secara aman guna menghindari *data leakage*.
* **Penanganan Class Imbalance:** Menggunakan metode **SMOTE** yang diterapkan **hanya pada data latih (training set)** setelah proses *train-test split* agar distribusi kelas menjadi seimbang tanpa memicu kebocoran data.

### 3. Perbandingan Performa Model
Berikut adalah ringkasan hasil performa dari model-model yang diuji setelah melalui seluruh rangkaian *workflow*:

| Algoritma | Accuracy | Precision (>50K) | Recall | F1-Score | ROC-AUC |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Logistic Regression** | *Lihat Notebook* | *Lihat Notebook* | *Lihat Notebook* | *Lihat Notebook* | *Lihat Notebook* |
| **Random Forest** | *Lihat Notebook* | *Lihat Notebook* | *Lihat Notebook* | *Lihat Notebook* | *Lihat Notebook* |
| **XGBoost Default (Terbaik)** | **85,22%** | **0,68** | **0,73** | **0,70** | **0,9097** |

### 4. Kesimpulan Model Terbaik
Berdasarkan hasil pengujian, **XGBoost Default** dipilih sebagai model terbaik karena terbukti memberikan kemampuan klasifikasi yang sangat baik pada dataset *Adult Census Income*, mengungguli performa *Logistic Regression* dan *Random Forest*. Model ini berhasil mengenali kelas minoritas ($>50\text{K}$) dengan optimal berkat penanganan *class imbalance* dan prapemrosesan yang tepat tanpa risiko kebocoran informasi.
