# Project-Analisa-Big-Data-023-264

### Nama Anggota
#### 1. Luthfiya Indah Fithriani (202110370311023)
#### 2. Tarissa Rizky Salsabiila Uwar (202110370311264)

# README: Hotel Booking Insights 

![Hotel Booking Visualization](https://www.example.com/hotel-booking-image.png)  

## 🌟 1. Pendahuluan

### 📌 1.1 Mengapa Penting?
Pernahkah Anda memesan hotel dan bertanya-tanya bagaimana memilih jenis hotel yang paling sesuai dengan kebutuhan Anda? Dalam industri perhotelan, memahami preferensi pelanggan dalam memilih tipe hotel adalah kunci untuk meningkatkan pengalaman menginap. Pemilihan tipe hotel juga dipengaruhi oleh berbagai faktor seperti harga, lokasi, fasilitas, dan tujuan perjalanan. Kami hadir dengan solusi berbasis data untuk menjawab pertanyaan ini dan membantu hotel memahami preferensi pelanggan mereka dengan lebih baik.

### 🛠️ 1.2 Rencana Solusi Kami
Kami menggunakan dataset "Hotel Booking Demand" untuk menggali wawasan dari data reservasi hotel. Analisis kami berfokus pada:
- 🏨 Mengidentifikasi faktor-faktor yang memengaruhi pemilihan jenis hotel.
- ⏳ Mengungkap tren durasi menginap.
- 🛎️ Menggali preferensi pelanggan berdasarkan pola reservasi.

Kami akan memanfaatkan eksplorasi data mendalam, pembersihan data, dan visualisasi menarik untuk menyajikan temuan yang relevan dan actionable.

### 💡 1.3 Pendekatan yang Kami Gunakan
Dengan mengandalkan teknik Exploratory Data Analysis (EDA), kami memvisualisasikan data untuk mengungkap hubungan tersembunyi dan tren penting. Dari heatmap korelasi hingga grafik musiman, setiap langkah dirancang untuk memberikan wawasan yang bermanfaat. Data preprocessing juga dilakukan dengan hati-hati untuk memastikan hasil yang berkualitas.

### ✅ 1.4 Apa Manfaatnya Bagi Anda?
Hasil analisis ini memberikan kekuatan kepada hotel untuk:
- 🎯 Menyusun strategi pemasaran yang lebih tepat.
- 😊 Meningkatkan kepuasan pelanggan dengan menawarkan jenis hotel yang sesuai.
- 🚀 Mengoptimalkan pendapatan melalui segmentasi pelanggan yang lebih baik.

Inilah langkah pertama menuju pengelolaan hotel yang lebih cerdas!

---

## 🛠️ 2. Package yang Diperlukan

### 📦 2.1 Daftar Paket Python
Pastikan Anda menginstal paket berikut sebelum menjalankan analisis ini:

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
gdown
```

### 🔕 2.2 Pesan dan Peringatan
Kami telah menghilangkan semua peringatan yang tidak relevan agar pengalaman membaca Anda lebih nyaman.

---

## 📂 3. Data Preparation

### 🔗 3.1 Sumber Data
Dataset ini berasal dari [Kaggle: Hotel Booking Demand Dataset](https://www.kaggle.com/jessemostipak/hotel-booking-demand). Data ini adalah harta karun bagi mereka yang ingin memahami dunia perhotelan lebih dalam.

### 📋 3.2 Apa Isi Dataset?
Dataset ini mencakup 119,390 entri dengan 32 kolom. Beberapa sorotan:
- **Jenis Hotel**: City Hotel dan Resort Hotel.
- **Lead Time**: Berapa lama sebelum kedatangan reservasi dibuat.
- **Tarif Harian Rata-rata**: Harga yang dibayar pelanggan.
- **Durasi Menginap**: Lama waktu tamu menginap di hotel.

### 🧹 3.3 Langkah Pembersihan Data
Kami melakukan langkah berikut:
- Mengisi nilai hilang di kolom `children` dengan nilai 0.
- Menghapus baris dengan data hilang kritis.
- Menstandarkan tipe data untuk konsistensi.

### 📊 3.4 Gambaran Dataset Akhir
Dataset bersih kami siap dianalisis! Berikut tampilan ringkasnya:

| hotel       | lead_time | adr  | country |
|-------------|-----------|------|---------|
| Resort Hotel| 342       | 0.0  | PRT     |
| Resort Hotel| 737       | 0.0  | GBR     |

### 🔍 3.5 Info Variabel Penting
- **Hotel**: 2 kategori (Resort, City).
- **Tarif Harian**: Rentang 0 hingga 5,000 dengan distribusi yang skewed.
- **Durasi Menginap**: Variabel penting dalam menentukan preferensi pelanggan.

---

## 📈 4. Eksplorasi dan Analisis Data

### 🔎 4.1 Menggali Informasi Baru
Kami menciptakan wawasan dengan:
- Mengidentifikasi preferensi jenis hotel berdasarkan tujuan perjalanan.
- Analisis musiman untuk menemukan puncak pemesanan.
- Menghubungkan durasi menginap dengan pemilihan jenis hotel.

### 🖼️ 4.2 Visualisasi Menarik
1. **Heatmap Korelasi**:
   Memvisualisasikan hubungan antar variabel utama seperti `lead_time` dan `adr`.

   ![Heatmap](https://www.example.com/heatmap.png)

2. **Grafik Musiman**:
   Menampilkan distribusi pemesanan per bulan untuk mengidentifikasi pola musiman.

3. **Histogram ADR**:
   Mengungkap distribusi tarif harian berdasarkan jenis hotel.

### ⭐ 4.3 Temuan Utama
- Hotel Kota lebih sering dipilih oleh tamu bisnis karena lokasinya yang strategis.
- Hotel Resor lebih diminati untuk liburan keluarga karena fasilitas dan suasananya.
- Pemesanan dengan lead time yang lebih pendek lebih sering terjadi pada Hotel Kota.

---

## ✨ 5. Rangkuman

### 🔄 5.1 Apa Masalahnya?
Memahami preferensi pelanggan dalam memilih jenis hotel sangat penting untuk meningkatkan pengalaman tamu dan pendapatan hotel.

### 🚀 5.2 Bagaimana Kami Mengatasinya?
Dengan menganalisis dataset "Hotel Booking Demand" menggunakan teknik EDA untuk mengidentifikasi pola dan tren pemilihan hotel.

### 🏆 5.3 Wawasan Utama
- Durasi menginap dan tujuan perjalanan sangat memengaruhi pemilihan jenis hotel.
- Tren musiman membantu mengoptimalkan strategi pemasaran.
- Hotel Resor memiliki peluang untuk meningkatkan lead time melalui promosi awal.

### 🌍 5.4 Implikasi bagi Konsumen
Hotel dapat menggunakan hasil analisis ini untuk:
- Menyusun promosi yang relevan sesuai musim.
- Menawarkan paket yang menarik untuk durasi menginap tertentu.
- Menyesuaikan fasilitas sesuai preferensi pelanggan.

### 🛠️ 5.5 Keterbatasan
- Data terbatas pada periode tertentu dan tidak mencakup faktor eksternal seperti cuaca atau kebijakan ekonomi.
- Penelitian di masa depan dapat memperluas cakupan dengan variabel tambahan.

Dengan analisis ini, mari kita bantu industri perhotelan melangkah ke arah yang lebih baik. 🌟 Temukan wawasan, buat perubahan, dan optimalkan pengalaman pelanggan Anda!

