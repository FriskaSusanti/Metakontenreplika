# META REPLIKA — Halaman Mesin Pencari FRISKA

Folder ini berisi replika halaman mesin pencari bergaya Bing yang dibuat dengan HTML, CSS, dan JavaScript. Logonya diganti menjadi **FRISKA** untuk penggunaan pribadi. Proyek ini adalah bagian dari Tugas Kuliah AI.

## Isi Folder

| File | Keterangan |
|------|------------|
| `google-search.html` | Halaman mesin pencari bergaya Bing: semua HTML, CSS, dan JavaScript ada dalam satu file. |
| `metakonten.html` | Replika dashboard Metakonten (tema gelap): sidebar, ringkasan pipeline konten, form "Tentang Akun Kamu" (penonton, akun, referensi), Fokus Hari Ini, dan Timeline Mendatang. Bisa tambah/hapus akun, hitung karakter, dan tombol Save. |
| `README.md` | File ini, berisi penjelasan isi folder. |

## Cara Membuka

Klik dua kali `google-search.html`, atau buka lewat Terminal:

```bash
open google-search.html
```

Tidak perlu instalasi, server, atau koneksi khusus. Internet hanya dibutuhkan saat menjalankan pencarian.

## Fitur

- **Latar pemandangan** (langit senja, gunung, danau) yang digambar dengan gradien CSS, tanpa file gambar.
- **Logo FRISKA** dengan ikon pita berwarna toska.
- **Kotak pencarian** lebar dan membulat, dengan ikon cari dengan gambar, mikrofon, tombol kaca pembesar, dan tombol ✕ untuk menghapus isian.
- **Saran pencarian otomatis (autocomplete)** dari daftar contoh. Bisa dipilih dengan tombol panah ↑ ↓, dan ditutup dengan Esc.
- **Pencarian sungguhan** dikirim ke bing.com.
- **Header** berisi tab Copilot, Gambar, Video, Peta, dan Berita (membuka bagian Bing yang sesuai), poin hadiah, tombol Masuk, dan menu (hanya tampilan).
- **Tombol cepat** di bawah kotak pencarian: Tanya Copilot, Gambar, Berita, Peta.
- **Kartu berita** contoh dengan tab Untuk Anda / Teknologi / Pendidikan, info cuaca, dan keterangan foto latar.
- **Footer** transparan berisi tautan Privasi, Ketentuan, Iklan, Bantuan, dan Umpan Balik.
- **Responsif**: tampilan menyesuaikan layar HP.

## Cara Kerja Singkat

1. **HTML** menyusun struktur halaman: header, logo, form pencarian, dan footer.
2. **CSS** mengatur tampilan, misalnya warna logo, kotak pencarian membulat, bayangan saat disorot, dan tata letak untuk layar kecil.
3. **JavaScript** mengatur interaksi:
   - Menyaring daftar `samples` sesuai teks yang diketik, lalu menampilkannya sebagai saran.
   - Navigasi saran dengan keyboard dan klik.
   - Mengirim kata kunci ke `https://www.bing.com/search?q=...` saat pencarian dijalankan.

## Cara Mengubah

- **Mengganti tulisan logo:** cari bagian `<div class="logo">` lalu ubah teks `FRISKA` di dalamnya.
- **Mengubah daftar saran:** edit array `samples` di bagian `<script>`.
- **Mengubah kartu berita:** cari `<section class="feed">`. Setiap kartu adalah satu blok `<a class="card">`.
- **Mengganti latar:** ubah `background-image` pada `body` di bagian `<style>`.
- **Mengganti judul tab browser:** ubah isi `<title>`.
