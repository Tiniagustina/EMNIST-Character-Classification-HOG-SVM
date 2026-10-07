# 🔤 Handwritten Character Classification using HOG & SVM (EMNIST Dataset)

Repositori ini berisi implementasi *Machine Learning Pipeline* end-to-end untuk mengklasifikasikan karakter tulisan tangan (huruf A-Z) berdasarkan dataset **EMNIST (Extended MNIST)**. Proyek ini menggabungkan teknik ekstraksi fitur visual **HOG (Histogram of Oriented Gradients)** dan klasifikasi **Support Vector Machine (SVM)** yang dioptimasi menggunakan *Grid Search CV*.

[![Watch Video Presentation](https://img.shields.io/badge/YouTube-Watch%20Demo-red?style=for-the-badge&logo=youtube)](https://youtu.be/OeGW-ET5LAM)

---

## 🛠️ Machine Learning Pipeline

### 1. Data Preparation
* **Dataset:** EMNIST Letters (Huruf A-Z).
* **Sampling:** 2.600 sampel data yang seimbang (100 sampel per kelas huruf dari A hingga Z) untuk memastikan efisiensi komputasi dan performa model yang stabil.

### 2. Feature Extraction (HOG)
Mengekstraksi fitur visual karakter tulisan tangan menggunakan algoritma **Histogram of Oriented Gradients (HOG)** dengan konfigurasi parameter:
* `orientations`: 9
* `pixels_per_cell`: (8, 8)
* `cells_per_block`: (2, 2)

### 3. Classification & Hyperparameter Tuning
* **Model Base:** Support Vector Machine (SVM).
* **Optimization:** *Grid Search* dengan *K-Fold Cross Validation* untuk menemukan kombinasi nilai `C`, `gamma`, dan `kernel` yang paling optimal.

### 4. Model Evaluation & Results
Model dievaluasi menggunakan data uji (*testing data*) untuk mengukur kestabilan prediksi:
* **Metrik Utama:** Accuracy, Precision, Recall, dan F1-Score.
* **Confusion Matrix:** Prediksi terdistribusi secara konsisten di sepanjang garis diagonal utama, menunjukkan misklasifikasi yang sangat minim antar-karakter.

---

## 📸 Demo & Penjelasan Video
Penjelasan rinci mengenai alur pemrosesan kode, ekstraksi fitur HOG, *tuning* SVM, hingga analisis *Confusion Matrix* dapat dilihat pada video berikut:
▶️ **[Nonton Video Penjelasan Proyek di YouTube](https://youtu.be/OeGW-ET5LAM)**

---

## 🚀 Cara Menjalankan Kode (How to Run)

1. **Clone Repositori Ini:**
   ```bash
   git clone [https://github.com/Tiniagustina/EMNIST-Character-Classification-HOG-SVM.git](https://github.com/Tiniagustina/EMNIST-Character-Classification-HOG-SVM.git)
   cd EMNIST-Character-Classification-HOG-SVM
