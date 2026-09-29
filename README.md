# Website SMA Taman Madya Jetis

Situs statis satu halaman untuk SMA Taman Madya Jetis, Yogyakarta.
Dibuat dengan HTML, CSS, dan JavaScript murni — tanpa framework, tanpa build step.

## Struktur

```
index.html        isi halaman
css/styles.css    semua tampilan
js/main.js        menu mobile, animasi scroll, embed Instagram
img/              gambar (termasuk hero-bg.jpg)
```

## Menjalankan di komputer sendiri

- **Live Server (VS Code):** klik kanan `index.html` → *Open with Live Server*
- **Tanpa VS Code:** jalankan dari folder ini
  ```
  python -m http.server 8899
  ```
  lalu buka `http://localhost:8899/`

## Cara update berita

1. Buka Instagram sekolah, buka posting yang mau ditampilkan
2. Tekan tombol `...` di pojok posting → **Copy Link**
3. Tempel link itu ke `data-instgrm-permalink` di dalam `index.html`
4. Commit & push (atau upload ulang ke hosting)

Posting terbaru ditaruh paling atas. Foto, caption, dan jumlah suka diambil
langsung dari Instagram, jadi selalu yang terbaru.

## Update foto latar beranda

Ganti berkas `img/hero-bg.jpg` (rasio 16:9, lebar minimal 1600 px), lalu
commit. Tidak perlu sentuh CSS.

## Deploy

Sudah dikonfigurasi otomatis oleh [Vercel](https://vercel.com).
Tiap kali ada push ke branch utama, Vercel otomatis deploy ulang.
