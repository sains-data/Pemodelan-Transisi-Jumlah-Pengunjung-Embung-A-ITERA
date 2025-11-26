# ANALISIS RANTAI MARKOV - POLA KERAMAIAN PENGUNJUNG DI EMBUNG A INSTITUT TEKNOLOGI SUMATERA
## Penulis
RA - Kelompok 3
- Pandra Insani Putra Azwar	(121450137)
- Lia Alyani			(121450138)
- Muhammad Bayu Syuhada	(122450007)
- Kemas Veriandra Ramadhan	(122450016)

Proyek ini menganalisis pola keramaian pengunjung embung A ITERA menggunakan metode Rantai Markov untuk memprediksi tingkat keramaian di waktu mendatang.

## Dataset

File: `data_pemstok.csv`

Data berisi pencatatan jumlah pengunjung embung pada berbagai waktu dengan interval 10 menit, mencakup informasi tanggal, waktu, hari ke-, dan jumlah orang.

## Metodologi

### 1. Definisi State

Data jumlah pengunjung dikategorikan menjadi 3 state berdasarkan quantile (tertile):

| State | Rentang Jumlah Orang | Kategori |
|-------|---------------------|----------|
| Sepi | 12 - 34 orang | Pengunjung sedikit |
| Sedang | 35 - 54 orang | Keramaian normal |
| Ramai | 55 - 71 orang | Pengunjung padat |

### 2. Matriks Transisi

Probabilitas perpindahan antar state:

- **Dari Sepi**: 60% tetap sepi, 20% ke sedang, 20% ke ramai
- **Dari Sedang**: 16.7% ke sepi, 50% tetap, 33.3% ke ramai
- **Dari Ramai**: 33.3% ke sepi, 16.7% ke sedang, 50% tetap ramai

Berikut tampilan beberapa visualisasi probabilitas perpindahan state:

**Heatmap**: Matriks probabilitas transisi antar state
![Heatmap Matriks Transisi](foto/heatmap.png)

**Diagram Transisi**: Diagram transisi rantai Markov dengan bobot probabilitas
![Diagram Transisi](foto/diagram.png)
### 3. Distribusi Stasioner

Dalam jangka panjang, proporsi waktu untuk setiap kondisi:
- **Sepi**: 39%
- **Sedang**: 27%
- **Ramai**: 34%

### 4. Karakteristik Rantai

- Semua state saling terhubung (communicating)
- Bersifat aperiodik (tidak ada siklus tetap)
- State recurrent positif



## LAMPIRAN VIDEO
Klik link di bawah untuk melihat video hasil tugas besar kami:

[Video Tubes Pemstok Kelompok 3 RA](bit.ly/VideoTubesPemstok3RA)


