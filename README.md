# Project-Analisa-Big-Data-023-264

### Nama Anggota
#### 1. Luthfiya Indah Fithriani (202110370311023)
#### 2. Tarissa Rizky Salsabiila Uwar (202110370311264)


# EDA Hotel Booking Insights 

## 🌟 Pendahuluan

### 📌 Mengapa Penting?
Pernahkah Anda memesan hotel dan bertanya-tanya bagaimana memilih jenis hotel yang paling sesuai dengan kebutuhan Anda? Dalam industri perhotelan, memahami preferensi pelanggan dalam memilih tipe hotel adalah kunci untuk meningkatkan pengalaman menginap. Pemilihan tipe hotel juga dipengaruhi oleh berbagai faktor seperti harga, lokasi, fasilitas, dan tujuan perjalanan. Kami hadir dengan solusi berbasis data untuk menjawab pertanyaan ini dan membantu hotel memahami preferensi pelanggan mereka dengan lebih baik.

### 🛠️ Rencana Solusi Kami
Kami menggunakan dataset "Hotel Booking Demand" untuk menggali wawasan dari data reservasi hotel. Analisis kami berfokus pada:
- 🏨 Mengidentifikasi faktor-faktor yang memengaruhi pemilihan jenis hotel.
- ⏳ Mengungkap tren durasi menginap.
- 🛎️ Menggali preferensi pelanggan berdasarkan pola reservasi.

Kami akan memanfaatkan eksplorasi data mendalam, pembersihan data, dan visualisasi menarik untuk menyajikan temuan yang relevan dan actionable.

### 💡 Pendekatan yang Kami Gunakan
Dengan mengandalkan teknik Exploratory Data Analysis (EDA), kami memvisualisasikan data untuk mengungkap hubungan tersembunyi dan tren penting. Dari heatmap korelasi hingga grafik musiman, setiap langkah dirancang untuk memberikan wawasan yang bermanfaat. Data preprocessing juga dilakukan dengan hati-hati untuk memastikan hasil yang berkualitas.

### ✅ Apa Manfaatnya Bagi Anda?
Hasil analisis ini memberikan kekuatan kepada hotel untuk:
- 🎯 Menyusun strategi pemasaran yang lebih tepat.
- 😊 Meningkatkan kepuasan pelanggan dengan menawarkan jenis hotel yang sesuai.
- 🚀 Mengoptimalkan pendapatan melalui segmentasi pelanggan yang lebih baik.

Inilah langkah pertama menuju pengelolaan hotel yang lebih cerdas!

---

## 📦 Package yang Diperlukan

Proyek ini menggunakan pustaka Python berikut. Instal di lingkungan Anda:

```bash
pip install pandas numpy matplotlib seaborn gdown
```

Pustaka ini memastikan penanganan, analisis, dan visualisasi data berjalan lancar:
- `pandas`: Manipulasi dan pembersihan data.
- `numpy`: Operasi numerik.
- `matplotlib` & `seaborn`: Membuat visualisasi yang menarik.
- `gdown`: Mengunduh dataset langsung dari Google Drive.

**Tips:** Gunakan lingkungan virtual seperti `venv` atau `conda` untuk menjaga kebersihan lingkungan kerja.

---

## 📂 Persiapan Data

### 🌐 Sumber Data
Kami menggunakan dataset "Hotel Booking Demand" dari [GitHub TidyTuesday](https://raw.githubusercontent.com/rfordatascience/tidytuesday/main/data/2020/2020-02-11/hotels.csv). Data ini adalah harta karun bagi mereka yang ingin memahami dunia perhotelan lebih dalam.

### 📊 Tentang Dataset
Dataset ini mencakup 119,390 entri dengan 32 kolom. Adapun beberapa fitur yang kami gunakan adalah:

| **Variabel**        | **Deskripsi**                |
|---------------------|------------------------------|
| `Hotel`             | Tipe Hotel (City Hotel dan Resort Hotel)                |
| `Is Canceled`       | Nilai yang menunjukkan apakah pemesanan dibatalkan (1) atau tidak (0)           |
| `Lead Time`         | Jumlah hari yang berlalu antara tanggal pemesanan dan kedatangan     |
| `arrival_date_year` | Tahun kedatangan            |
| `stays_in_weekend_nights`       | Jumlah malam akhir pekan (Sabtu atau Minggu) yang tamu menginap atau pesan untuk menginap di hotel     |
| `stays_in_week_nights`         | Jumlah malam minggu (Senin hingga Jumat) tamu menginap atau memesan untuk menginap di hotel      |
| `booking_changes` | Jumlah perubahan/perubahan yang dilakukan pada pemesanan sejak pemesanan dimasukkan di PMS hingga saat check-in atau pembatalan             |
| `arrival_date_day_of_month`       | Tanggal kedatangan hari      |
| `arrival_date_month`              | Bulan kedatangan      |
| `customer_type`                   | Jenis pemesanan, dengan asumsi salah satu dari empat kategori: Kontrak - bila pemesanan memiliki penjatahan atau jenis kontrak lain yang terkait dengannya; Grup – ketika pemesanan dikaitkan dengan grup; Sementara – ketika pemesanan bukan merupakan bagian dari grup atau kontrak, dan tidak terkait dengan pemesanan sementara lainnya; Pihak sementara – ketika pemesanan bersifat sementara, namun dikaitkan dengan setidaknya pemesanan sementara lainnya      |
| `is_repeated_guest`               | Nilai yang menunjukkan apakah nama pemesanan berasal dari tamu berulang (1) atau tidak (0)      |
| `children`       | Jumlah anak       |
| `babies`       | Jumlah bayi       |


### 🧹 Preperocessing Data
1. Handling missing value.
2. Handling duplicate data.
---
