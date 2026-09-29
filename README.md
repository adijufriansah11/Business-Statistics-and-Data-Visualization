# Pertemuan 1 · Data dalam Bisnis Digital

**Mata kuliah:** Business Statistics and Data Visualization
**Program studi:** S1 Bisnis Digital
**Minggu:** 1 · **Sub-CPMK-1** (C2 · A3)
**Dosen pengampu:** [Nama Dosen Pengampu]

Repositori ini berisi slide Pertemuan 1 yang bisa dibuka langsung di browser, beserta notebook hands-on. Notebook adalah versi Python (Google Colab) dari praktikum lab *"Eksplorasi dataset e-commerce"* pada Pertemuan 1. Langkahnya sama dengan praktikum di spreadsheet: membuka data, mengenali jenis kolom, memfilter, meringkas dengan pivot table, dan membuat grafik pertama. Notebook ini juga berisi latihan kualitas data dan pseudonimisasi data pribadi sesuai UU No. 27 Tahun 2022 tentang Pelindungan Data Pribadi.

---

## Tujuan pembelajaran

Setelah menyelesaikan notebook ini, mahasiswa mampu:

1. **Menjelaskan peran statistika** dalam pengambilan keputusan bisnis digital (C2).
2. **Mengklasifikasikan data** menurut jenis (kategorik/numerik) dan skala pengukuran NOIR (C2).
3. **Mengenali sumber data digital** serta menilai kualitasnya (C2).
4. **Menerapkan prinsip etika data** sesuai UU PDP (A3).

---

## Isi file

| File | Keterangan |
|---|---|
| `index.html` | Penampil slide online (untuk GitHub Pages) |
| `slides/` | Gambar 30 slide (`slide-01.webp` … `slide-30.webp`) dan `cover.jpg` untuk pratinjau tautan |
| `Pertemuan_1_Data_dalam_Bisnis_Digital.pptx` | File slide asli |
| `Pertemuan_1_Hands_on_Data_Bisnis_Digital.ipynb` | Notebook praktikum utama |
| `README.md` | Panduan ini |
| `.nojekyll` | Agar GitHub Pages menyajikan file apa adanya |
| `dataset_ecommerce.xlsx` / `.csv` | *Dibuat otomatis* saat sel bagian 2.1 notebook dijalankan (tidak perlu diunggah) |

---

## Slide online (GitHub Pages)

`index.html` menampilkan slide Pertemuan 1 di browser, di laptop maupun ponsel.

**Cara pakai:**
- **Pindah slide:** tombol panah ← → , klik sisi kiri/kanan slide, atau geser di ponsel
- **Layar penuh:** tombol **F** atau ikon layar penuh (cocok untuk presentasi di kelas)
- **Semua slide:** tombol **G** atau ikon kotak-kotak
- **Tautan ke slide tertentu:** tambahkan `#nomor` di akhir alamat, misalnya `.../#17` untuk latihan cepat
- **Menu Materi:** unduh `.pptx`, buka notebook di Colab, atau unduh `.ipynb`

**Langkah mengonlinekan:**
1. Buat repositori baru di GitHub (misalnya `bsdv-pertemuan-1`), atur sebagai **Public**.
2. Unggah **seluruh isi folder** (bukan foldernya) ke repositori: **Add file → Upload files**, seret semua file dan folder `slides/`, lalu **Commit changes**.
3. Buka **Settings → Pages**. Pada *Source* pilih **Deploy from a branch**, *Branch* pilih **main** dan folder **/ (root)**, lalu **Save**.
4. Tunggu 1–2 menit. Situs tersedia di `https://USERNAME.github.io/NAMA-REPOSITORI/`.
5. Agar tombol **Buka hands-on di Colab** langsung berfungsi, edit `index.html` dan ganti tiga baris ini:
   ```js
   const GITHUB_USER = "USERNAME-GITHUB";
   const GITHUB_REPO = "NAMA-REPOSITORI";
   const GITHUB_BRANCH = "main";
   ```
   Tautan Colab-nya menjadi `https://colab.research.google.com/github/USERNAME/NAMA-REPOSITORI/blob/main/Pertemuan_1_Hands_on_Data_Bisnis_Digital.ipynb`, yang juga bisa dibagikan langsung ke mahasiswa.

**Memperbarui slide:** jika `.pptx` diubah, ekspor ulang tiap slide sebagai gambar (PowerPoint: **File → Export → PNG**, pilih *All slides*), ubah ke 1920×1080, beri nama `slide-01.webp` dst. (atau `.png`, lalu sesuaikan ekstensi pada baris `const src = ...` di `index.html`). Jika jumlah atau judul slide berubah, sesuaikan juga daftar `SLIDES` di `index.html`.

---

## Cara menjalankan

### Opsi A: Google Colab (disarankan)
1. Buka [colab.research.google.com](https://colab.research.google.com) dan masuk dengan akun Google.
2. Pilih **File → Upload notebook**, lalu unggah file `.ipynb`.
3. Jalankan sel dari atas ke bawah dengan `Shift + Enter`, atau **Runtime → Run all**.

Tidak perlu memasang apa pun. Semua library sudah tersedia di Colab.

### Opsi B: Jupyter di komputer sendiri
Pasang Python 3.9 atau lebih baru, lalu:

```bash
pip install pandas numpy matplotlib openpyxl jupyter
jupyter notebook Pertemuan_1_Hands_on_Data_Bisnis_Digital.ipynb
```

---

## Alur notebook

| Bagian | Topik | Kaitan dengan slide | Latihan |
|---|---|---|---|
| 1 | Persiapan library | – | |
| 2 | Membuka dan mengenali dataset | Praktikum langkah 1–2 | |
| 3 | Jenis data dan skala pengukuran (NOIR) | Slide 12–18 | ✏️ Latihan cepat (dicek otomatis) |
| 4 | Filter dan sort | Praktikum langkah 4 | ✏️ Latihan 4 |
| 5 | Pivot table dan grafik batang | Praktikum langkah 5–6 | ✏️ Latihan 5 |
| 6 | Struktur data: cross-section, time series, panel | Slide 15 | |
| 7 | Statistika deskriptif vs inferensial | Slide 8 | |
| 8 | Dari data ke keputusan bisnis | Slide 7, 9 | Diskusi |
| 9 | Memeriksa kualitas data | Slide 22 | ✏️ Latihan 9 |
| 10 | Etika data dan pseudonimisasi | Slide 24–27 | ✏️ Diskusi kasus TokoKita |
| 11 | Latihan mandiri | – | ✏️ 5 soal |
| 12 | Persiapan Tugas 1 | Slide 29 | Alat bantu profil kolom |

Perkiraan waktu: **±170 menit** (sesuai alokasi praktikum lab).

---

## Tentang dataset

Dataset berisi **1.000 pesanan fiktif** dari sebuah toko online selama September 2026. Data dibuat dengan kode memakai *seed* tetap (`2026`), sehingga **hasil semua mahasiswa sama** dan mudah dibahas bersama di kelas.

| Kolom | Isi | Jenis data | Skala |
|---|---|---|---|
| `order_id` | Nomor pesanan | Kategorik | Nominal |
| `tanggal_pesan` | Tanggal pesanan | Numerik | Interval |
| `kategori` | Fashion, Elektronik, Kecantikan, Rumah tangga | Kategorik | Nominal |
| `ukuran` | S, M, L, XL (hanya produk Fashion) | Kategorik | Ordinal |
| `kota` | Kota tujuan pengiriman | Kategorik | Nominal |
| `kode_pos` | Kode pos tujuan | Kategorik | Nominal |
| `metode_bayar` | E-wallet, Transfer bank, COD, dll. | Kategorik | Nominal |
| `harga` | Harga barang (Rp) | Numerik kontinu | Rasio |
| `jumlah` | Jumlah barang dibeli | Numerik diskrit | Rasio |
| `lama_kirim_hari` | Lama pengiriman (hari) | Numerik diskrit | Rasio |
| `rating` | Rating ulasan ★1–5 | Kategorik | Ordinal |

> ⚠️ Tabel di atas adalah **kunci jawaban** latihan bagian 3. Mahasiswa sebaiknya mencoba mengklasifikasikan sendiri terlebih dahulu.

**Memakai dataset dari LMS:** jika dosen membagikan `dataset_ecommerce.xlsx` sendiri, unggah file tersebut ke Colab lalu jalankan mulai bagian 2.2. Nama kolom bisa berbeda, jadi sesuaikan kode setelahnya.

---

## Tugas 1 · Individu

**Tenggat:** sebelum Pertemuan 2 · **Kumpul di:** LMS, folder Tugas 1 · **Format:** PDF maks. 3 halaman + file dataset

1. Pilih satu dataset e-commerce dari Kaggle (minimal **8 kolom** dan **500 baris**).
2. Buat tabel klasifikasi: nama kolom, jenis data, skala, dan alasan.
3. Identifikasi minimal **tiga masalah kualitas data**.
4. Tandai kolom yang termasuk **data pribadi** menurut UU PDP dan usulkan cara menyamarkannya.
5. Tulis **dua pertanyaan bisnis** yang bisa dijawab dengan dataset tersebut.

Bagian 12 notebook menyediakan fungsi `profil_kolom()` dan `cek_kualitas()` untuk membuat draf tabel klasifikasi. **Jenis dan skala data tetap harus ditentukan sendiri beserta alasannya.** Komputer tidak memahami makna kolom (contoh: kode pos terlihat seperti angka, padahal label).

| Komponen penilaian | Bobot |
|---|---|
| Ketepatan klasifikasi | 40% |
| Masalah kualitas data | 25% |
| Identifikasi data pribadi | 20% |
| Pertanyaan bisnis | 15% |

---

## Catatan etika dan penggunaan AI

- Semua nama, nomor HP, alamat, dan data pelanggan di notebook ini **fiktif**.
- Jangan mengunggah data pribadi asli (milik sendiri, keluarga, atau tempat kerja) ke notebook maupun ke layanan publik.
- Sesuai kontrak kuliah, penggunaan AI **boleh** untuk belajar dan memeriksa kode, tetapi **wajib diungkapkan** dan dipahami sendiri.
- Ringkasan pasal UU PDP di notebook bersifat edukatif dan **bukan nasihat hukum**. Rujukan resmi: UU No. 27 Tahun 2022 (JDIH BPK).

---

## Persiapan Pertemuan 2 · Data Wrangling & EDA

- Siapkan akun Google untuk Colab.
- Bawa dataset Tugas 1.
- Baca Anderson dkk., *Statistics for Business and Economics*, bab 1 (*Data and Statistics*).

---

## Masalah umum

| Masalah | Solusi |
|---|---|
| `NameError: name 'df' is not defined` | Sel sebelumnya belum dijalankan. Pilih **Runtime → Run before**. |
| `FileNotFoundError` | File belum diunggah, atau nama file salah ketik. Cek panel folder di kiri Colab. |
| File yang diunggah hilang | Colab menghapus file saat sesi berakhir. Unggah ulang, atau simpan di Google Drive. |
| Hasil berbeda dengan teman | Pastikan sel pembuat dataset (bagian 2.1) tidak diubah dan dijalankan ulang dari awal. |
