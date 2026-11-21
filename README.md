# Kennnskieez — Portfolio 2026

Portofolio pribadi satu file. Semua CSS, markup, dan JavaScript ada di `index.html`.

**Live:** https://sixkennn-collab.github.io

## Stack

- HTML/CSS/JS murni, tanpa build step.
- GSAP 3.12.5 + ScrollTrigger, Lenis 1.1.13 (via CDN).
- WebGL fragment shader untuk hero, dengan fallback canvas partikel.
- Font: Archivo, Instrument Serif, JetBrains Mono, Noto Serif JP (Google Fonts).

## Struktur

```
index.html    seluruh situs (satu file)
img/          foto patung (zeus, hercules, apollo) + foto About
favicon.svg   ikon tab
favicon.ico   fallback browser lama
.nojekyll     mematikan pemrosesan Jekyll di GitHub Pages
```

## Menambah atau mengganti konten

| Yang mau diubah | Cari di `index.html` |
|---|---|
| Nama di hero | `<h1 class="name" aria-label="...">` — tiap huruf ada di `<span class="ch-in">`, jumlahnya harus tetap pas per baris |
| Tagline & deskripsi | `.tagline` dan `.hero-side p` |
| Project | `<article class="card">` di dalam `<div class="stack">` |
| Keahlian | `<li class="cap">` di section `.caps-sec` |
| Email | `<span class="email" id="email">` |
| Foto About | `<img id="me" data-src="...">` |
| Foto patung | atribut `src` dan `data-u` pada `.god` |

## Catatan

- Foto patung (Zeus, Heracles, Apollo) dan foto About sekarang file lokal di `img/`, bukan hotlink. Ukuran 714×1280, ~165 KB per file.
- Frame patung rasio 3:4 sementara fotonya 9:16, jadi gambar dipotong. Fokus crop diatur lewat `object-position: 50% 20%` di `.god-i img` — geser angka itu kalau mau menampilkan bagian lain.
- Situs butuh koneksi internet karena GSAP dan font dimuat dari CDN. Gambar sudah tidak.
- `localStorage.motion` menyimpan pilihan tombol Motion on/off.

## Deploy

Push ke branch `main`. GitHub Pages menyajikan langsung dari root branch tersebut.
