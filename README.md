# Business Statistics and Data Visualization

**Statistika Bisnis dan Visualisasi Data** · Program Studi S1 Bisnis Digital · [Nama Perguruan Tinggi]

Repositori ini berisi materi perkuliahan: slide, notebook hands-on (Google Colab), dataset latihan, dan tugas mingguan. RPS mata kuliah ini disusun dengan pendekatan *Outcome Based Education* (OBE).

| | |
|---|---|
| **Kode MK** | [BD-xxx] |
| **Bobot** | 3 SKS (2 teori + 1 praktikum) |
| **Semester** | 3 (Ganjil) 2026/2027 |
| **Prasyarat** | Matematika Bisnis; Pengantar Bisnis Digital |
| **Dosen pengampu** | [Nama dosen] · [email] |
| **LMS kelas** | [tautan LMS] |

---

## Daftar isi

- [Capaian pembelajaran](#capaian-pembelajaran)
- [Struktur repositori](#struktur-repositori)
- [Jadwal 16 pertemuan](#jadwal-16-pertemuan)
- [Pertemuan 1 — Data dalam Bisnis Digital](#pertemuan-1--data-dalam-bisnis-digital)
- [Pertemuan 2 — Data Wrangling & EDA](#pertemuan-2--data-wrangling--eda)
- [Cara menjalankan notebook](#cara-menjalankan-notebook)
- [Penilaian](#penilaian)
- [Referensi](#referensi)
- [Catatan untuk dosen](#catatan-untuk-dosen)

---

## Capaian pembelajaran

| Kode | Capaian Pembelajaran Mata Kuliah (CPMK) | Bobot |
|---|---|---|
| CPMK-1 | Menjelaskan peran statistika dan data dalam bisnis digital serta menerapkan prinsip etika data | 10% |
| CPMK-2 | Mendeskripsikan data bisnis dengan statistika deskriptif dan probabilitas | 17% |
| CPMK-3 | Menganalisis pertanyaan bisnis dengan statistika inferensial (estimasi, uji hipotesis, A/B testing) | 21% |
| CPMK-4 | Menganalisis dan mengevaluasi model regresi dan peramalan | 24% |
| CPMK-5 | Merancang dashboard dan *data story* untuk rekomendasi bisnis | 28% |

Rincian CPL, Sub-CPMK, rubrik, dan pemetaan asesmen ada di dokumen RPS (`docs/`).

---

## Struktur repositori

```
.
├── README.md
├── docs/
│   ├── RPS_OBE_Business_Statistics_Data_Visualization.docx
│   └── RPS_Business_Statistics_Data_Visualization.pptx        # presentasi RPS / kontrak kuliah
├── pertemuan-01/
│   └── Pertemuan_1_Data_dalam_Bisnis_Digital.pptx
├── pertemuan-02/
│   ├── Pertemuan_2_Data_Wrangling_EDA.pptx
│   ├── Pertemuan_2_Data_Wrangling_EDA.ipynb                   # hands-on + Tugas 2
│   └── data/
│       ├── transaksi_tokokita_kotor.csv                       # dataset hands-on
│       └── transaksi_tugas2_kotor.csv                         # dataset Tugas 2
└── pertemuan-03/ …
```

---

## Jadwal 16 pertemuan

| Minggu | Topik | Sub-CPMK | Asesmen | Materi |
|:---:|---|:---:|---|:---:|
| 1 | Data dalam bisnis digital: jenis data, skala, sumber data, etika & UU PDP | 1 | Tugas 1: klasifikasi dataset | ✅ |
| 2 | Data wrangling & EDA dengan pandas / Power Query | 2 | Tugas 2: laporan pembersihan data | ✅ |
| 3 | Statistika deskriptif | 3 | Tugas analisis deskriptif UMKM | ⏳ |
| 4 | Probabilitas & teorema Bayes | 4 | Kuis 1 | ⏳ |
| 5 | Distribusi binomial, Poisson, normal | 4 | Tugas kasus distribusi | ⏳ |
| 6 | Sampling & interval kepercayaan | 5 | Tugas estimasi | ⏳ |
| 7 | Uji hipotesis & A/B testing | 6 | Laporan A/B test | ⏳ |
| 8 | **Ujian Tengah Semester** | 1–6 | UTS (20%) | — |
| 9 | ANOVA & chi-square | 7 | Tugas segmentasi | ⏳ |
| 10 | Korelasi & regresi linier sederhana | 8 | Tugas regresi | ⏳ |
| 11 | Regresi berganda + penetapan topik proyek | 8 | Laporan model | ⏳ |
| 12 | Deret waktu & peramalan | 9 | Tugas forecasting | ⏳ |
| 13 | Prinsip visualisasi data | 10 | Makeover visualisasi | ⏳ |
| 14 | Dashboard & KPI bisnis digital | 11 | Progres dashboard | ⏳ |
| 15 | Data storytelling & presentasi proyek | 8, 9, 11, 12 | Proyek akhir (20%) | ⏳ |
| 16 | **Ujian Akhir Semester** | 7–11 | UAS (15%) | — |

✅ tersedia · ⏳ menyusul

---

## Pertemuan 1 — Data dalam Bisnis Digital

> **Sub-CPMK-1** · C2, A3 · bobot 5%

<!-- TODO: lengkapi bagian ini (tautan slide, file Tugas 1, tenggat) -->

**Materi:** kontrak kuliah · peran statistika dalam bisnis digital · statistika deskriptif vs inferensial · empat tingkat analitik · jenis data dan skala pengukuran (NOIR) · struktur data · sumber data digital · kualitas data · etika data dan UU No. 27 Tahun 2022 tentang Pelindungan Data Pribadi.

**File:**
- [`Pertemuan_1_Data_dalam_Bisnis_Digital.pptx`](pertemuan-01/Pertemuan_1_Data_dalam_Bisnis_Digital.pptx)

**Praktikum (170 menit):** eksplorasi dataset e-commerce di Excel / Google Sheets: filter, sort, pivot table, dan grafik pertama.

**Tugas 1 (individu) — Klasifikasi dataset e-commerce**
1. Pilih satu dataset e-commerce dari Kaggle (minimal 8 kolom, 500 baris).
2. Buat tabel klasifikasi: nama kolom, jenis data, skala, dan alasan.
3. Identifikasi minimal tiga masalah kualitas data.
4. Tandai kolom yang termasuk data pribadi menurut UU PDP dan usulkan cara menyamarkannya.
5. Tulis dua pertanyaan bisnis yang bisa dijawab dengan dataset tersebut.

*Format:* PDF maks. 3 halaman + file dataset · *Tenggat:* sebelum Pertemuan 2 · [tautan pengumpulan]

---

## Pertemuan 2 — Data Wrangling & EDA

> **Sub-CPMK-2** · C3, P3 · bobot 5%

**Materi:** alur enam langkah data wrangling (*import → inspect → clean → transform → explore → save*) · Google Colab dan DataFrame pandas · duplikat · tipe data · label kategori · missing value · nilai tidak valid · outlier (metode IQR) · kolom turunan dan transformasi log · EDA · cleaning log · alternatif dengan Excel Power Query.

**File:**
- [`Pertemuan_2_Data_Wrangling_EDA.pptx`](pertemuan-02/Pertemuan_2_Data_Wrangling_EDA.pptx)
- [`Pertemuan_2_Data_Wrangling_EDA.ipynb`](pertemuan-02/Pertemuan_2_Data_Wrangling_EDA.ipynb) &nbsp; [![Buka di Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/USERNAME/REPO/blob/main/pertemuan-02/Pertemuan_2_Data_Wrangling_EDA.ipynb)

> Ganti `USERNAME/REPO` pada tautan Colab dengan nama akun dan repositori GitHub Anda.

### Isi notebook hands-on

| Bagian | Isi | Waktu |
|:---:|---|:---:|
| 0 | Persiapan & memuat data | 10' |
| 1 | Mengenali data: `shape`, `info`, `describe`, `value_counts`, `isna` | 20' |
| 2 | Membersihkan data: duplikat, tipe data, label, missing value, nilai tidak valid, outlier | 70' |
| 3 | Transformasi: `total`, `bulan`, `hari`, `akhir_pekan`, `kelompok_belanja`, `log_total` | 20' |
| 4 | EDA: ringkasan per kategori, kota, waktu, metode bayar, heatmap | 35' |
| 5 | Menyimpan data bersih & *cleaning log* | 5' |
| 6 | Tugas 2 (5 soal) | di rumah |

### Dataset

Kedua dataset **fiktif** dan dibuat khusus untuk latihan. Masalah kualitas data sengaja disisipkan.

| File | Baris | Periode | Kegunaan |
|---|:---:|---|---|
| `transaksi_tokokita_kotor.csv` | 1.537 | Agu–Sep 2026 | Hands-on di kelas |
| `transaksi_tugas2_kotor.csv` | 1.230 | Jul–Sep 2026 | Tugas 2 |

| Kolom | Keterangan |
|---|---|
| `order_id` | ID pesanan |
| `tanggal` | Tanggal pesanan (dua format: `YYYY-MM-DD` dan `DD/MM/YYYY`) |
| `id_pelanggan` | ID pelanggan (sudah dipseudonimkan) |
| `kota` | Kota pembeli (label tidak seragam, ada yang kosong) |
| `kategori` | Fashion, Elektronik, Kecantikan, Rumah Tangga, Makanan |
| `harga` | Harga satuan (sebagian berformat teks `Rp 149.500`) |
| `jumlah` | Jumlah unit dibeli |
| `metode_bayar` | E-Wallet, COD, Transfer Bank, Kartu Kredit (label tidak seragam) |
| `rating` | Rating 1–5 (ada yang kosong dan tidak valid) |
| `ongkir` | Ongkos kirim (hanya di dataset Tugas 2) |

### Tugas 2 (individu) — Laporan Praktikum Pembersihan Data Transaksi

Bobot **3% nilai akhir** · kerjakan di bagian 6 notebook dengan dataset `transaksi_tugas2_kotor.csv`.

| No | Soal | Bobot |
|:---:|---|:---:|
| 1 | **Profil data.** Laporkan ukuran data, tipe tiap kolom, serta jumlah dan persentase data kosong. Sebutkan kolom yang tipenya salah dan jelaskan mengapa. | 15% |
| 2 | **Duplikat & label.** Hapus duplikat persis, lalu seragamkan `kota` dan `metode_bayar`. Laporkan baris yang dihapus serta nilai unik sebelum dan sesudah. | 20% |
| 3 | **Tipe data & missing value.** Ubah `harga` menjadi angka dan `tanggal` menjadi tipe tanggal. Tangani data kosong setiap kolom dan jelaskan alasan strategi Anda. | 20% |
| 4 | **Nilai tidak valid & outlier.** Terapkan aturan validasi `rating` dan `jumlah`. Deteksi outlier `harga` dengan IQR per kategori; bedakan kesalahan dan yang nyata, lalu jelaskan tindakan. | 25% |
| 5 | **EDA & insight.** Buat `total = harga × jumlah + ongkir`, tiga visualisasi berbeda jenis, tiga insight (temuan + angka + implikasi), dan cleaning log lengkap. | 20% |

**Kriteria umum:** kode berjalan dari awal sampai akhir tanpa error · setiap keputusan pembersihan dijelaskan di sel teks · angka yang dilaporkan sama dengan output kode.

*Format:* `.ipynb` + PDF (*File → Print*) · *Tenggat:* sebelum Pertemuan 3 · [tautan pengumpulan]

---

## Cara menjalankan notebook

### Google Colab (disarankan)
1. Klik tombol **Buka di Colab** pada pertemuan terkait, atau buka [colab.research.google.com](https://colab.research.google.com) lalu *File → Upload notebook*.
2. Unggah file CSV melalui panel **Files** (ikon folder di kiri), atau jalankan sel pemuat data dan pilih file ketika diminta.
3. Jalankan sel dari atas ke bawah dengan **Shift + Enter**. Jika muncul error yang aneh: *Runtime → Restart and run all*.

### Lokal (Jupyter)
```bash
python -m venv .venv
source .venv/bin/activate          # Windows: .venv\Scripts\activate
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook
```
Letakkan file CSV di folder yang sama dengan notebook.

---

## Penilaian

| Komponen | Bobot |
|---|:---:|
| Tugas, praktikum, kuis | 45% |
| Ujian Tengah Semester (minggu 8) | 20% |
| Proyek akhir kelompok (minggu 15) | 20% |
| Ujian Akhir Semester (minggu 16) | 15% |

Syarat mengikuti UAS: kehadiran minimal 75%. Asesmen berbasis *case method* dan proyek berbobot 59% dari nilai akhir.

**Kebijakan penggunaan AI:** boleh dipakai untuk belajar dan memeriksa kode, tetapi wajib diungkapkan, dan Anda harus memahami setiap baris yang dikumpulkan.

---

## Referensi

**Utama**
1. Anderson, D. R., Sweeney, D. J., Williams, T. A., dkk. (2020). *Statistics for Business and Economics* (14th ed.). Cengage Learning.
2. Levine, D. M., Szabat, K. A., & Stephan, D. F. (2021). *Statistics for Managers Using Microsoft Excel* (9th ed.). Pearson.
3. Knaflic, C. N. (2015). *Storytelling with Data*. Wiley.

**Pendukung**
- McKinney, W. (2022). *Python for Data Analysis* (3rd ed.). O'Reilly.
- Wilke, C. O. (2019). *Fundamentals of Data Visualization*. O'Reilly.
- Hyndman, R. J., & Athanasopoulos, G. (2021). *Forecasting: Principles and Practice* (3rd ed.). OTexts.
- Few, S. (2013). *Information Dashboard Design* (2nd ed.). Analytics Press.
- Undang-Undang Republik Indonesia Nomor 27 Tahun 2022 tentang Pelindungan Data Pribadi.

---

## Catatan untuk dosen

- **Kunci jawaban** (mis. `Kunci_Jawaban_Tugas_2.ipynb`) jangan diunggah ke repositori publik. Simpan di folder terpisah, lalu tambahkan ke `.gitignore`:
  ```
  kunci/
  *Kunci_Jawaban*
  ```
- Semua angka di slide Pertemuan 2 dihitung dari hasil menjalankan notebook hands-on, sehingga sama dengan output yang dilihat mahasiswa.
- Isian bertanda `[ ]` (nama dosen, kode MK, tautan LMS, tenggat) perlu disesuaikan.

---

*Terakhir diperbarui: Oktober 2026 · Materi untuk keperluan pendidikan. Seluruh dataset latihan bersifat fiktif.*
