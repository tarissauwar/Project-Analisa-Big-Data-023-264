# 💫 EDA Hotel Booking Insights 

### Nama Anggota
#### 1. Luthfiya Indah Fithriani (202110370311023)
#### 2. Tarissa Rizky Salsabiila Uwar (202110370311264)


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

## 📦 Langkah Instalasi

### 1. Clone Repository

```bash
git clone https://github.com/tarissauwar/Project-Analisa-Big-Data-023-264.git
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
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

### 🔍 Wawasan Berdasarkan Fokus Penelitian

#### 🏨 *Faktor-Faktor yang Memengaruhi Pemilihan Jenis Hotel*  
1. *Lokasi dan Kebutuhan Tamu:*
   - *Hotel Kota* lebih banyak dipesan oleh tamu bisnis, terbukti dari tingginya persentase tamu yang tinggal dalam waktu singkat (1-3 malam).  
   - *Hotel Resor* cenderung dipilih untuk liburan keluarga atau pasangan, terutama pada musim panas, ketika banyak tamu menginap selama lebih dari seminggu.

2. *Harga dan Pendapatan Tamu:*
   - Tarif harian rata-rata (ADR) pada hotel resor lebih tinggi, menunjukkan tamu dengan anggaran lebih besar cenderung memilih resor.  
   - Diskon pada musim tertentu di hotel kota menjadi daya tarik bagi tamu dengan anggaran lebih rendah.

3. *Tujuan Perjalanan:*
   - Tamu yang memesan melalui distribution channel seperti agen perjalanan lebih banyak memilih hotel resor.  
   - Sebaliknya, pemesanan langsung ke hotel lebih sering ditemukan pada hotel kota.

---

#### ⏳ *Tren Durasi Menginap*  
1. *Hotel Kota:*  
   - Rata-rata durasi menginap pendek (1-3 malam).  
   - Tren ini lebih terlihat selama hari kerja (weekday), menunjukkan dominasi tamu bisnis atau perjalanan singkat.  

2. *Hotel Resor:*  
   - Durasi menginap lebih panjang (5-10 malam), dengan puncak selama musim panas.  
   - Hal ini mengindikasikan bahwa resor lebih menarik untuk liburan panjang, terutama bagi keluarga.  

3. *Pola Musiman:*  
   - Durasi menginap meningkat signifikan selama musim liburan (Juni-Agustus).  
   - Musim semi dan gugur memiliki rata-rata durasi menginap yang moderat, sedangkan musim dingin menunjukkan durasi paling pendek.

---

#### 🛎️ *Preferensi Pelanggan Berdasarkan Pola Reservasi*  
1. *Musim dan Waktu Pemesanan:*
   - *Hotel Resor*: Tingkat pemesanan meningkat drastis pada musim panas. Sebagian besar tamu memesan beberapa bulan sebelumnya.  
   - *Hotel Kota*: Pemesanan lebih merata sepanjang tahun, dengan banyak reservasi dilakukan mendadak (1-7 hari sebelum check-in).

2. *Jenis Pelanggan:*
   - Pelanggan individu (bukan grup) mendominasi pemesanan di hotel kota.  
   - Pemesanan grup lebih sering ditemukan di hotel resor, khususnya untuk acara seperti liburan keluarga besar atau perusahaan.  

3. *Saluran Reservasi:*
   - Agen perjalanan dan operator tur lebih efektif untuk memasarkan hotel resor.  
   - Pemesanan langsung melalui situs web atau aplikasi lebih banyak digunakan untuk hotel kota.

---

### 🔑 *Kesimpulan Penting:*
- Hotel city dan hotel resor memiliki keunggulan unik yang sesuai dengan kebutuhan tamu tertentu. Hotel city adalah pilihan utama bagi tamu bisnis  singkat yang mengutamakan lokasi strategis dan efisiensi, dengan durasi menginap rata-rata 1-3 malam. Tamu hotel city cenderung memesan langsung dengan waktu reservasi yang mendadak, menjadikannya ideal untuk perjalanan spontan atau urusan mendesak.

- Sebaliknya, hotel resor menarik perhatian tamu dengan anggaran lebih besar yang mencari pengalaman liburan panjang dan berkualitas. Dengan durasi menginap rata-rata 5-10 malam, terutama pada musim panas, resor menjadi pilihan utama bagi keluarga atau pasangan yang mengutamakan kenyamanan dan relaksasi. Sebagian besar tamu resor memesan jauh hari melalui agen perjalanan, menunjukkan pentingnya hubungan strategis dengan operator tur.

- Pola musiman juga menjadi faktor krusial; hotel city memiliki tingkat pemesanan yang stabil sepanjang tahun, sedangkan hotel resor mengalami lonjakan signifikan selama musim liburan. Pemahaman mendalam tentang preferensi tamu, pola reservasi, dan durasi menginap memungkinkan kedua jenis hotel menyesuaikan strategi pemasaran dan layanan secara spesifik untuk memenuhi kebutuhan pasar mereka.
