# Capstone-Project-IBM
# Student Performance Analysis

## Project Overview
Proyek ini menganalisis dataset publik tentang performa akademik siswa dengan tujuan untuk memahami faktor-faktor yang memengaruhi nilai akhir siswa (`G3`).  
Beberapa faktor yang dianalisis meliputi:
- Konsumsi alkohol harian (`Dalc`)
- Konsumsi alkohol di akhir pekan (`Walc`)
- Pendidikan orang tua (`Medu`, `Fedu`)
- Dukungan keluarga (`famsup`)

## Dataset
  Sumber data:
  https://www.kaggle.com/datasets/uciml/student-alcohol-consumption

## Analysis Process
1. Data Cleaning  
   - Menghapus kolom yang tidak relevan  
   - Mengubah variabel kategori menjadi biner (`famsup` → `famsup_bin`)  

2. Descriptive Statistics  
   - Rata-rata nilai akhir siswa (`G3`)  
   - Standar deviasi untuk melihat sebaran nilai  

3. Correlation Analysis (Spearman) 
   - Mengukur hubungan antara faktor-faktor dengan `G3`  
   - Cocok digunakan karena banyak variabel ordinal  

4. Group Analysis  
   - Rata-rata nilai akhir berdasarkan `Dalc` (konsumsi alkohol)  
   - Rata-rata nilai akhir berdasarkan `Medu` (pendidikan ibu)  

## Key Results
- Rata-rata nilai akhir (G3): 10.42 (std 4.58)  
- Korelasi Spearman dengan G3:
  - `Medu` (pendidikan ibu): 0.225 (positif)  
  - `Dalc` (alkohol harian): -0.121 (negatif)  
  - `Walc` (alkohol akhir pekan): -0.104 (negatif)  
  - `Fedu` (pendidikan ayah): 0.170 (positif lemah)  
  - `famsup_bin`: -0.050 (tidak signifikan)  

- **Rata-rata nilai per kategori:**  
  - Semakin tinggi `Dalc`, cenderung nilai lebih rendah.  
  - Semakin tinggi `Medu`, cenderung nilai lebih tinggi.  

## Insights & Findings
1. Pendidikan ibu (Medu) memiliki pengaruh positif yang cukup kuat terhadap nilai siswa.  
2. Konsumsi alkohol (Dalc & Walc) cenderung berdampak negatif pada performa akademik.  
3. Dukungan keluarga (famsup) tidak menunjukkan dampak yang signifikan.  

## Recommendations
- Sekolah: Adakan program edukasi tentang dampak konsumsi alkohol pada siswa.  
- Orang tua: Dorong keterlibatan orang tua dalam pendidikan anak, terutama dari keluarga dengan pendidikan rendah.  
- Policy makers: Pertimbangkan kebijakan pendukung bagi keluarga dengan latar belakang pendidikan rendah.  

##  AI Support
Proses analisis dibantu dengan AI untuk:
- Menyusun pipeline analisis data  
- Menghasilkan insight dari hasil statistik  
- Membuat visualisasi dan ringkasan yang mudah dipahami  

