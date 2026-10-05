# Bank Prompt MAHIR

Bank Prompt MAHIR adalah situs statis untuk membantu guru menyusun prompt pembelajaran Bahasa Indonesia menggunakan kerangka **MAHIR**:

- **M** — Masukkan peran
- **A** — Atur konteks
- **H** — Hasil yang diinginkan
- **I** — Instruksi dan batasan
- **R** — Review dan revisi

Situs dapat digunakan langsung melalui browser tanpa instalasi, akun, server aplikasi, atau basis data.

## Fitur

### Bank Prompt

- 12 prompt siap pakai untuk modul ajar, tujuan pembelajaran, kegiatan, diferensiasi, asesmen, materi, LKPD, audit, revisi, dan refleksi.
- Pencarian berdasarkan judul, kategori, atau isi prompt.
- Filter kategori.
- Tombol **Salin prompt**.
- Placeholder `[seperti ini]` yang mudah ditemukan dan disesuaikan.
- Tampilan responsif serta dukungan mode gelap mengikuti pengaturan perangkat.

### Lembar Kerja Prompt

- Enam latihan menyusun prompt.
- Pemeriksaan otomatis unsur prompt dan saran perbaikan.
- Penghitung jumlah kata dan progres latihan.
- Contoh jawaban untuk setiap kasus.
- Penyimpanan progres secara lokal di browser.

## Privasi dan penyimpanan data

Situs ini tidak memiliki backend, basis data, analitik, formulir daring, atau proses pengiriman data ke server.

- Halaman Bank Prompt tidak menyimpan input pengguna.
- Nama, asal sekolah, dan jawaban pada Lembar Kerja hanya disimpan dalam `localStorage` browser pada perangkat pengguna.
- Data `localStorage` tidak otomatis berpindah ke perangkat atau browser lain.
- Tombol **Kosongkan semua** menghapus jawaban latihan yang tersimpan untuk situs ini.
- Jika pengguna mengunduh hasil latihan, file dibuat dan disimpan pada perangkat pengguna.

Catatan: font dimuat dari Google Fonts ketika perangkat terhubung ke internet. Permintaan font tersebut tidak berisi nama, sekolah, atau jawaban latihan pengguna.

## Menjalankan secara lokal

Tidak diperlukan proses build. Buka `index.html` langsung di browser, atau jalankan server statis sederhana dari direktori proyek.

Contoh menggunakan Python:

```bash
python -m http.server 8000
```

Kemudian buka `http://localhost:8000`.

## Struktur proyek

```text
.
├── index.html
├── Bank Prompt MAHIR.html
├── Lembar Kerja Prompt MAHIR.html
├── Bank_Prompt_MAHIR_Modul_Ajar_Bahasa_Indonesia (1).pdf
├── .gitignore
└── README.md
```

## Deployment dengan GitHub Pages

1. Push proyek ke branch `main` pada repositori GitHub.
2. Buka **Settings → Pages** di repositori.
3. Pada **Build and deployment**, pilih **Deploy from a branch**.
4. Pilih branch `main` dan folder `/ (root)`.
5. Klik **Save** dan tunggu proses deployment selesai.

Setelah aktif, situs biasanya tersedia di:

```text
https://mazpissvisual.github.io/bank-promt/
```

## Memperbarui daftar prompt

Data prompt berada di konstanta `PROMPTS` dalam `Bank Prompt MAHIR.html`. Setiap entri menggunakan struktur:

```javascript
{
  cat: 'Kategori',
  title: 'Judul prompt',
  desc: 'Penjelasan singkat',
  text: `Isi prompt`
}
```

Kategori baru otomatis muncul sebagai tombol filter.

## Teknologi

- HTML
- CSS
- JavaScript tanpa framework
- Google Fonts: Bricolage Grotesque, Atkinson Hyperlegible, dan Caveat

## Kredit

Bank Prompt MAHIR · Havidz Muhammad Iqbal, S.Kom.

