# META REPLIKA — Halaman Mesin Pencari FRISKA

Folder ini berisi replika tampilan halaman utama mesin pencari Google yang dibuat dengan HTML, CSS, dan JavaScript. Logonya diganti menjadi **FRISKA** untuk penggunaan pribadi. Proyek ini adalah bagian dari Tugas Kuliah AI.

## Isi Folder

| File | Keterangan |
|------|------------|
| `google-search.html` | Halaman mesin pencari: semua HTML, CSS, dan JavaScript ada dalam satu file. |
| `metakonten.html` | Replika dashboard Metakonten (tema gelap): sidebar, ringkasan pipeline konten, form "Tentang Akun Kamu" (penonton, akun, referensi), Fokus Hari Ini, dan Timeline Mendatang. Bisa tambah/hapus akun, hitung karakter, dan tombol Save. |
| `README.md` | File ini, berisi penjelasan isi folder. |

## Cara Membuka

Klik dua kali `google-search.html`, atau buka lewat Terminal:

```bash
open google-search.html
```

Tidak perlu instalasi, server, atau koneksi khusus. Internet hanya dibutuhkan saat menjalankan pencarian.

## Fitur

- **Logo FRISKA** dengan warna khas Google (biru, merah, kuning, biru, hijau, merah).
- **Kotak pencarian** dengan ikon kaca pembesar, mikrofon, kamera, dan tombol ✕ untuk menghapus isian.
- **Saran pencarian otomatis (autocomplete)** dari daftar contoh. Bisa dipilih dengan tombol panah ↑ ↓, dan ditutup dengan Esc.
- **Tombol "Google Search"** menjalankan pencarian sungguhan di google.com.
- **Tombol "Saya Lagi Beruntung"** langsung membuka hasil pencarian teratas.
- **Header** berisi link Gmail dan Gambar, ikon aplikasi, dan tombol Login (hanya tampilan).
- **Deretan logo Google Workspace** di bawah kotak pencarian: Drive, Docs, Sheets, Slides, Forms, Gmail, Calendar, Meet, Chat, Sites, dan Gemini. Setiap logo adalah tautan yang membuka produknya di tab baru. Logo digambar ulang secara sederhana dengan SVG, tanpa file gambar.
- **Footer** dan pilihan bahasa seperti Google versi Indonesia.
- **Responsif**: tampilan menyesuaikan layar HP.

## Cara Kerja Singkat

1. **HTML** menyusun struktur halaman: header, logo, form pencarian, dan footer.
2. **CSS** mengatur tampilan, misalnya warna logo, kotak pencarian membulat, bayangan saat disorot, dan tata letak untuk layar kecil.
3. **JavaScript** mengatur interaksi:
   - Menyaring daftar `samples` sesuai teks yang diketik, lalu menampilkannya sebagai saran.
   - Navigasi saran dengan keyboard dan klik.
   - Mengirim kata kunci ke `https://www.google.com/search?q=...` saat pencarian dijalankan.

## Cara Mengubah

- **Mengganti tulisan logo:** cari bagian `<div class="logo">` lalu ubah huruf di dalam setiap `<span>`. Warnanya diatur oleh kelas `b` (biru), `r` (merah), `y` (kuning), dan `g` (hijau).
- **Mengubah daftar saran:** edit array `samples` di bagian `<script>`.
- **Menambah atau menghapus logo Workspace:** cari `<section class="workspace">`. Setiap produk adalah satu blok `<a class="app">` yang berisi SVG dan nama produk.
- **Mengganti judul tab browser:** ubah isi `<title>`.
