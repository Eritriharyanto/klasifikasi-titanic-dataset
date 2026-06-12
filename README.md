# Titanic Survival Classification

Link : https://www.kaggle.com/datasets/yasserh/titanic-dataset/data 

## Deskripsi Proyek

Proyek ini bertujuan untuk memprediksi kemungkinan keselamatan penumpang Titanic menggunakan teknik Machine Learning berdasarkan karakteristik penumpang seperti jenis kelamin, usia, kelas tiket, tarif perjalanan, dan informasi lainnya.

Dataset yang digunakan adalah Titanic Dataset yang berisi data historis penumpang kapal Titanic.

---

## Tahapan Analisis

### 1. Exploratory Data Analysis (EDA)

Tahap EDA dilakukan untuk memahami karakteristik dataset, meliputi:

* Melihat ukuran dataset
* Informasi tipe data
* Statistik deskriptif
* Analisis missing value
* Visualisasi distribusi data
* Analisis keseimbangan target (Survived)
* Korelasi antar fitur numerik

---

### 2. Missing Value Handling

Beberapa fitur memiliki nilai yang hilang dan ditangani dengan:

* Age → Median
* Embarked → Modus
* Cabin → Diisi dengan kategori "Unknown"

---

### 3. Feature Engineering

Fitur baru dibuat untuk meningkatkan performa model:

* Title (diambil dari nama penumpang)
* CabinDeck (huruf pertama pada Cabin)
* TicketFreq (frekuensi tiket)
* FamilySize
* IsAlone

---

### 4. Data Cleaning

Proses pembersihan data meliputi:

* Penggabungan kategori Title yang jarang muncul
* Penyederhanaan kategori tertentu
* Penghapusan fitur yang tidak digunakan

Kolom yang dihapus:

* Name
* Ticket
* Cabin
* PassengerId

---

### 5. Encoding

Fitur kategorikal dikonversi menjadi numerik menggunakan Label Encoding:

* Sex
* Embarked
* Title
* CabinDeck

---

### 6. Train Test Split

Dataset dibagi menjadi:

* 80% Data Training
* 20% Data Testing

Menggunakan stratifikasi terhadap target Survived.

---

### 7. Standardisasi Data

StandardScaler digunakan khusus untuk model yang sensitif terhadap skala fitur seperti Logistic Regression.

---

## Algoritma Machine Learning

Model yang digunakan:

1. Logistic Regression
2. Random Forest
3. XGBoost
4. LightGBM
5. CatBoost

---

## Evaluasi Model

Metode evaluasi yang digunakan:

* Accuracy Score
* Cross Validation (5-Fold)
* Confusion Matrix
* ROC Curve
* AUC Score
* Feature Importance

---

## Visualisasi

Visualisasi yang dibuat meliputi:

* Missing Value Heatmap
* Distribusi Target
* Distribusi Fitur Numerik
* Correlation Heatmap
* Perbandingan Akurasi Model
* Confusion Matrix
* Feature Importance
* ROC Curve

---

## Library yang Digunakan

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* XGBoost
* LightGBM
* CatBoost

---

## Struktur Proyek

```text
.
├── titanic.ipynb
├── Titanic-Dataset.csv
└── README.md
```

---

## Tujuan

Membangun model klasifikasi yang mampu memprediksi apakah seorang penumpang Titanic akan selamat atau tidak berdasarkan karakteristik yang dimiliki.
