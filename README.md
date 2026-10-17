# Visualisasi Data Peminjaman Buku Perpustakaan

## Deskripsi Proyek

Proyek ini mengolah dan memvisualisasikan data peminjaman buku
perpustakaan menggunakan Python melalui **Google Colab**. Hasil
visualisasi digunakan untuk membantu memahami pola peminjaman,
perbandingan penerbit, serta distribusi kelompok usia buku.

## Tujuan

-   Memahami karakteristik dataset peminjaman buku.
-   Mengolah data agar siap dianalisis dan divisualisasikan.
-   Menyajikan informasi melalui beberapa jenis grafik.
-   Mengamati pola peminjaman berdasarkan waktu, penerbit, program
    studi, dan kelompok usia buku.

## Dataset

Dataset berisi informasi anggota, buku, dan aktivitas peminjaman.
Kolomnya meliputi:

`No`, `ID Anggota`, `Nama Anggota`, `Program Studi`, `Kode Buku`,
`Judul Buku`, `Penerbit`, `Tahun Terbit`, `Tanggal Pinjam`, `Status`,
`Lama Pinjam (Hari)`, `Kategori Buku`, `Usia Buku`,
`Kelompok Usia Buku` dan `Nama Bulan Pinjam`.

**Catatan:** Unggah file dataset ke Google Colab saat notebook
dijalankan, atau simpan di Google Drive lalu hubungkan Drive jika
diperlukan.

## Jenis Visualisasi

1.  **Line Chart (Grafik Garis):** menampilkan perubahan jumlah
    peminjaman dari waktu ke waktu.
2.  **Bar Chart (Diagram Batang):** membandingkan jumlah peminjaman
    berdasarkan penerbit.
3.  **Heatmap:** memperlihatkan jumlah peminjaman berdasarkan program
    studi dan judul buku.
4.  **Pie Chart (Diagram Lingkaran):** menunjukkan proporsi peminjaman
    berdasarkan kelompok usia buku.

## Teknologi yang Digunakan

-   **Google Colab** sebagai lingkungan penulisan dan eksekusi notebook
    Python berbasis cloud.
-   **Python** sebagai bahasa pemrograman.
-   **Pandas** untuk pengolahan dan analisis data.
-   **Matplotlib** untuk pembuatan grafik.
-   **Seaborn** untuk heatmap, jika digunakan.

## Persiapan dan Cara Menjalankan

1.  Buka [Google Colab](https://colab.research.google.com/).

2.  Buat notebook baru atau buka notebook proyek.

3.  Unggah dataset melalui panel **Files** di Google Colab, atau gunakan
    Google Drive.

4.  Impor pustaka yang diperlukan. Pandas dan Matplotlib umumnya sudah
    tersedia di Colab; jika diperlukan, instal pustaka tambahan dengan:

    ``` python
    !pip install seaborn openpyxl
    ```

5.  Jalankan sel kode secara berurutan dari atas ke bawah.

6.  Pastikan nama file dan lokasi dataset pada kode sesuai dengan file
    yang diunggah.

7.  Amati grafik yang dihasilkan di bawah sel kode masing-masing.

## Contoh Kode Membaca Dataset di Google Colab

Untuk file Excel yang diunggah langsung ke sesi Colab:

``` python
import pandas as pd
import matplotlib.pyplot as plt

from google.colab import files
uploaded = files.upload()

nama_file = next(iter(uploaded))
dataset = pd.read_excel(nama_file)

dataset.head()
```

Jika dataset berupa CSV, gunakan `pd.read_csv(nama_file)` sebagai
pengganti `pd.read_excel(nama_file)`.

## Jenis Hasil yang Diharapkan

-   Grafik perubahan jumlah peminjaman berdasarkan waktu.
-   Diagram perbandingan peminjaman berdasarkan penerbit.
-   Heatmap hubungan program studi dan judul buku.
-   Diagram proporsi peminjaman berdasarkan kelompok usia buku.

## Pengembangan Selanjutnya

Proyek dapat dikembangkan dengan menambahkan filter bulan atau program
studi, menangani data kosong dan duplikat secara lebih menyeluruh, serta
membuat dashboard interaktif.

## Penulis

-   **Nama:** Farma Ardan Dinata Yusana Putra
-   **NIM:** 2418061
-   **Program Studi:** Teknik Informatika
-   **Institusi:** Institut Teknologi Nasional Malang
