# EDA Survei Penggunaan Media Sosial

Proyek Exploratory Data Analysis (EDA) terhadap data survei penggunaan media sosial, dikerjakan secara berkelompok (Kelompok 11 Beginner) dalam program Junior Data Science di VINIX Seven Aurum (MSIB Batch 3). Proyek terdiri dari dua tahap: pembersihan data dan eksplorasi data.

## Tujuan
Memahami pola penggunaan media sosial responden dan dampak yang mereka rasakan, seperti gangguan produktivitas, kesulitan mengontrol diri, dan FOMO.

## Data
- Data mentah: 118 responden dan 17 variabel.
- Data bersih: 117 responden dan 17 variabel, terdiri dari 7 variabel skala persepsi (1-5) dan 10 variabel kategorikal (jenis kelamin, pekerjaan, platform, durasi penggunaan, dan lainnya).
- Data tidak memuat nama atau kontak responden.

## Isi repositori
| File | Keterangan |
| --- | --- |
| `01_cleaning_data_survei_medsos.ipynb` | Profiling data, deteksi masalah data, dan penanganannya |
| `02_eda_survei_medsos.ipynb` | Analisis frekuensi, distribusi, hubungan, perbandingan, dan hipotesis |
| `Survei_Medsos.csv` | Dataset mentah hasil survei (118 responden) |
| `Survei_Medsos_Bersih.csv` | Dataset hasil pembersihan (117 responden) |

## Tahap 1: Pembersihan data
- Memeriksa missing values, duplikasi, nilai tidak konsisten, dan outlier (boxplot).
- Menemukan 1 missing value pada kolom `Kesulitan_Melepaskan_Diri`. Karena jumlahnya kurang dari 5%, baris tersebut dihapus.
- Tidak ada data duplikat.
- Menyeragamkan penulisan nilai pada kolom `Jenis_Kelamin` ("Laki-laki" menjadi "Laki-Laki").
- Outlier pada skala 1-5 dipertahankan karena mencerminkan jawaban nyata responden, bukan kesalahan data.

## Tahap 2: Eksplorasi data
Analisis dibagi menjadi lima bagian: informasi dasar, frekuensi, distribusi, hubungan antar variabel, dan perbandingan antar kelompok, menggunakan bar chart, histogram, grouped barplot, dan boxplot. Hasilnya dirangkum dalam delapan hipotesis.

## Temuan utama
- **Responden:** 61 perempuan dan 56 laki-laki. Sebanyak 110 dari 117 responden adalah pelajar/mahasiswa.
- **Platform yang paling sering dipakai:** Instagram (43) dan WhatsApp (42), jauh di atas LINE (15), Twitter (12), dan Facebook (5).
- **Durasi harian:** kategori terbanyak adalah > 3 jam (34 responden), > 1 jam (32), dan > 2 jam (31).
- **Gangguan produktivitas:** rata-rata skor 3,46 dari 5, dan sebagian besar responden memberi skor 3-4.
- **Hubungan durasi dan dampak:** responden dengan durasi lebih lama cenderung punya skor FOMO, "tidak sadar waktu", dan "tidak bisa kontrol diri" lebih tinggi, meski selisihnya tidak besar.
- **Perbandingan gender:** pola durasi penggunaan laki-laki dan perempuan mirip.

## Keterbatasan
- Sampel didominasi pelajar/mahasiswa (sekitar 94%), jadi hasil belum mewakili kelompok lain.
- Hubungan antar variabel bersifat deskriptif (visual), belum diuji secara statistik, dan tidak menunjukkan sebab-akibat.
- Kategori durasi harian (> 1 jam, > 2 jam, > 3 jam) tumpang tindih, sehingga perlu dibuat lebih tegas pada survei berikutnya.

## Teknologi
Python, Google Colab, pandas, NumPy, Matplotlib, Seaborn

## Cara menjalankan
1. Unduh seluruh isi repositori ke satu folder.
2. Buka `cleaning_data_survei_medsos.ipynb` untuk melihat proses pembersihan. Notebook ini membaca `Survei_Medsos.csv` dan menghasilkan `Survei_Medsos_Bersih.csv`.
3. Buka `eda_survei_medsos.ipynb`, yang membaca `Survei_Medsos_Bersih.csv`, lalu jalankan sel secara berurutan.
4. Di Google Colab, unggah file CSV terlebih dahulu ke sesi sebelum menjalankan notebook.

## Tim
Kelompok 11 Beginner, VINIX Seven Aurum (MSIB Batch 3): Ilham Suryanulloh dan rekan satu kelompok.
