# capstonemodul3-dyandra - Daegu Apartment Market Price Prediction
Proyek ini bertujuan untuk memprediksi harga pasar apartemen di Daegu, Korea Selatan, berdasarkan fitur-fitur properti dan lingkungan menggunakan algoritma **Random Forest Regression**.

---

## File Tersedia
- Jupyter Notebook berisikan exploratory data analysis, data pre-processing, dan modeling.
- Model yang disimpan menggunakan pickle

---

## Latar Belakang
Harga apartemen dipengaruhi oleh banyak faktor, seperti ukuran, lokasi, dan fasilitas. Dengan memanfaatkan data historis, kita dapat membangun model machine learning untuk memperkirakan harga properti secara akurat, sehingga membantu pembeli, penjual, atau investor dalam mengambil keputusan.

---

## Dataset
Dataset yang digunakan memuat informasi apartemen di Daegu beserta harga pasarnya.  
Fitur-fitur utama yang digunakan dalam model:

| **Nama Kolom** | **Keterangan** |
| --- | --- |
| Hallway Type | Apartment type |
| TimeToSubway | Waktu yang dibutuhkan untuk ke stasiun subway terdekat |
| SubwayStation | Nama stasiun subway terdekat |
| N_FacilitiesNearBy(ETC) | Jumlah fasilitas dekat apartemen |
| N_FacilitiesNearBy(PublicOffice) | Jumlah fasilitas kantor publik dekat apartemen |
| N_SchoolNearBy(University) | Jumlah universitas dekat apartemen |
| N_Parkinglot(Basement) | Jumlah parkir yang tersedia |
| YearBuilt | Tahun pembangunan apartemen |
| N_FacilitiesInApt | Jumlah fasilitas di dalam apartemen |
| Size(sqft) | Luas apartemen (in square feet) |
| SalePrice | Harga apartemen (Won) |

---

## Isi

1. **Exploratory Data Analysis (EDA)**  
   - Analisis distribusi harga  
   - Korelasi antar fitur  

2. **Preprocessing Data**
   - Pembersihan data (null values dan outlier treatment)
   - Pemilihan fitur dan target

4. **Modeling**
   - Encoding untuk fitur object/kategorikal   
   - Pemisahan data menjadi train dan test set
   - Pembuatan pipeline step proses dari encoding, standarisasi skala data, hingga regressor
   - Menggunakan **RandomForestRegressor** dari scikit-learn  
   - Hyperparameter tuning dengan `RandomizedSearchCV`  

6. **Evaluasi Model**
   - Evaluasi menggunakan metrik **RMSE**, **MAE**, **R²**, **Adjusted R²**, dan **MAPE**
   - Perbandingan prediksi vs harga aktual  
   - Analisis feature importances

---

## Hasil Model

- **Test RMSE**: 41,686
- **MAE**: 32,623
- **R² Score**: 0.840171
- **Adjusted R² Score**: 0.838153
- **MAPE**: 17.88%

**Feature importances**:

| Fitur | Importance |
|-------|------------|
| HallwayType_terraced | 0.390565 |
| Size(sqf) | 0.390565 |
| YearBuilt | 0.093948 |
| N_Parkinglot(Basement) | 0.042827 |
| N_FacilitiesNearBy(ETC) | 0.023685 |

---

## Dokumentasi Video Presentasi

Video presentasi alur proyek dapat diakses melalui tautan berikut:
https://drive.google.com/file/d/1mukzMZ0889CgTJ-4D_9VV1fj15A5c8Ey/view?usp=sharing
