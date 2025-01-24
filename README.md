# Analisis Kualitas Udara

### Tujuan Analisis

File ini berisi terkait analisis data kualitas udara.

---

## Struktur Notebook

### 1. Import Library

Notebook ini memulai dengan mengimpor library penting yang digunakan untuk proses analisis atau pemodelan:

python

# Contoh import library

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

## Data Wrangling

### 1. Gathering Data

Proses ini memuat dataset yang akan digunakan untuk analisis.

python

# Contoh memuat dataset

data_aoti = pd.read_csv('/content/PRSA_Data_Aotizhongxin_20130301-20170228.csv')
data_aoti.head()

_Contoh:_

![Alt Text](https://raw.githubusercontent.com/iqkyu5566/datascience/refs/heads/main/img/1.png)

### 3. Data Cleaning dan Explorasi

Bagian ini melibatkan pembersihan data dan eksplorasi awal.

python

# Contoh cleaning data

data = data.dropna()
data.info()

### 4. Analisis Data

Bagian ini mencakup analisis atau pengolahan lebih lanjut pada data.

python

# Contoh analisis sederhana

plt.hist(data["column_name"])
plt.show()

### 5. Pertanyaan Analisis Bisnis

Pada notebook ini mencakup lima pertanyaan terkait analisis bisnis yang berhubungan dengan data:

1. Apa tren utama yang dapat diidentifikasi dari data?
2. Bagaimana performa setiap kategori/kelompok dalam dataset?
3. Apakah ada pola musiman atau temporal yang terlihat?
4. Faktor apa yang paling memengaruhi metrik utama?
5. Apa rekomendasi utama berdasarkan hasil analisis?

Jawaban Pertanyaan

1. Apa tren utama yang dapat diidentifikasi dari data?

Musim dingin cenderung memiliki tingkat polusi yang lebih tinggi, mungkin karena penggunaan bahan bakar pemanas atau kondisi atmosfer yang meningkatkan penahanan polutan di kota gucheng.

2. Bagaimana performa setiap kategori/kelompok dalam dataset?
   ![Alt Text](https://raw.githubusercontent.com/iqkyu5566/datascience/refs/heads/main/img/2.png)
   kondisi berangin(WSPM) memainkan peran penting dalam mengurangi konsentrasi polutan. di kota Aotizhongxin
3. Apakah ada pola musiman atau temporal yang terlihat?
   ![Alt Text](https://raw.githubusercontent.com/iqkyu5566/datascience/refs/heads/main/img/3.png)
   kota Dongsi memiliki polusi PM2.5 terbanyak shingga butuh penanganan yang lebih di banding kota lain

4. Faktor apa yang paling memengaruhi metrik utama?
   ![Alt Text](https://raw.githubusercontent.com/iqkyu5566/datascience/refs/heads/main/img/4.png)
   kadar PM2.5 menurun signifikan dari pukul 0.00 sampai sekitar pukul 16:00 dan naik secara signifikan dari pukul sekitar pukul 16:00 sampai puku 24:00 dikota guanyuan. hal ini butuh d cari tahu apa hal yang membuat naik signifikan dari jam 16:00 keatas

### 6. Kesimpulan dan Rekomendasi

#### Kesimpulan

Tingkat polusi udara di Beijing bervariasi secara signifikan antar stasiun pemantauan, waktu (harian dan musiman), dan dipengaruhi oleh faktor cuaca.

Stasiun pemantauan di Dongsi memiliki tingkat polusi PM2.5 tertinggi dan membutuhkan perhatian khusus.

Kondisi berangin berkontribusi pada penurunan tingkat PM2.5.

Musim dingin cenderung memiliki tingkat polusi yang lebih tinggi.

Aktivitas manusia mungkin berkontribusi pada pola harian PM2.5.

Manual grouping berdasarkan rata-rata PM2.5 dapat membantu dalam mengkategorikan stasiun pemantauan berdasarkan tingkat keparahan polusi.

#### Saran

Perlu dilakukan investigasi lebih lanjut untuk memahami faktor-faktor spesifik yang berkontribusi terhadap polusi udara di setiap stasiun pemantauan.

Strategi pengurangan polusi udara harus disesuaikan dengan karakteristik setiap kelompok stasiun pemantauan.

Pemantauan dan analisis data polusi udara secara terus-menerus penting untuk mengevaluasi efektivitas strategi pengurangan polusi.

Data polusi udara dapat diintegrasikan dengan data lain, seperti data lalu lintas atau data industri, untuk mendapatkan pemahaman yang lebih komprehensif tentang sumber polusi.

---
