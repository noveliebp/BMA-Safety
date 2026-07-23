# Dokumentasi Website PT Berkat Mitra Anugrah

> Dibuat sebagai patokan sebelum redesign. Update file ini setiap kali ada perubahan besar.

---

## 1. Informasi Perusahaan

| Field | Isi |
|---|---|
| Nama | PT Berkat Mitra Anugrah |
| Berdiri | 01 Maret 2012 |
| Bidang | Supplier Safety Equipment, Fire Protection & Uniform |
| Visi | Membangun Hubungan Tanpa Batas |
| Misi | Melayani pelanggan dengan tulus, kepuasan pelanggan tujuan kami, berikan senyuman terbaik |

### Kontak
- Telp: +62 21 3876 4354
- HP: +62 817 9818 766
- HP: +62 878 7629 8909
- Email: limbobby77@rocketmail.com
- Jam Kerja: Senin–Jumat 08:00–17:00

### Alamat
- **Kantor:** Ruko Mutiara Taman Palem Blok D8 No.15-16, Jl. Kamal Raya Outer Ring Road, Cengkareng, Jakarta Barat 11730
- **Toko:** LTC Glodok Lt.UG Blok C19 No.2, Jl. Hayam Wuruk, Mangga Besar, Taman Sari, Jakarta Barat

---

## 2. Struktur File Saat Ini

```
website BMA/
├── index.html          ← satu-satunya file HTML (semua halaman jadi satu)
├── WEBSITE_DOCS.md     ← file ini
└── produk/
    ├── helm.PNG
    ├── jashujan.PNG
    ├── sarungtangan.PNG
    ├── sepatu.PNG
    ├── kacamata.PNG
    ├── harness.PNG
    └── pemadam.PNG
```

### Aset Yang HILANG (belum ada di folder)
| File Direferensikan di HTML | Keterangan |
|---|---|
| `bma.png` | Logo di navbar |
| `BMA.png` | Foto di section About |
| `image.png` s/d `image14.png` | Logo 14 klien di section Our Clients |

---

## 3. Struktur Halaman (Section by Section)

### 3.1 Header / Navbar
- Fixed di atas, background putih
- Logo: gambar `bma.png` + teks "PT BERKAT MITRA ANUGRAH"
- Menu: Home, Our Product, Our Service, Our Client, About Us
- Hamburger menu untuk mobile

### 3.2 Hero Section
- Background: gradient hijau tua → hijau sedang
- Teks utama: *"Your Safety is Our Priority"*
- Sub-teks: tagline Inggris + deskripsi singkat Bahasa Indonesia
- **Tidak ada tombol CTA (Call-to-Action)**

### 3.3 Featured Products (Carousel)
- 3 slide: Safety Helmets, High-Visibility Safety Vests, Industrial Safety Gloves
- Gambar dari picsum.photos (placeholder internet, bukan foto produk asli)
- Konten masih dalam Bahasa Inggris
- Auto-rotate setiap 5 detik

### 3.4 Our Products (Grid)
- 6 produk dengan flip card animation (hover → balik kartu)
- Filter kategori: All, Head Protection, Body Protection, Hand Protection, Foot Protection
- Daftar produk:

| No | Nama | Kategori | Gambar | Harga |
|---|---|---|---|---|
| 1 | Helm Pro Max | head | produk/helm.PNG | $45.99 |
| 2 | Jas Hujan | body | produk/jashujan.PNG | $29.99 |
| 3 | Sarung Tangan | hand | produk/sarungtangan.PNG | $39.99 |
| 4 | Sepatu | foot | produk/sepatu.PNG | $89.99 |
| 5 | Kacamata | head | produk/kacamata.PNG | $34.99 |
| 6 | Safety Harness | body | picsum (placeholder) | $129.99 |

> **Catatan:** Harga dalam USD — perlu diubah ke IDR. Gambar harness belum ada.
> File `pemadam.PNG` ada di folder tapi **belum dipakai** di halaman.

### 3.5 Our Services
- 4 kartu layanan:
  1. Safety Consulting
  2. Training Programs
  3. Equipment Maintenance
  4. Fast Delivery
- Isi teks masih Bahasa Inggris

### 3.6 Our Trusted Clients
- 14 slot logo klien
- **Semua gambar klien hilang** (image.png s/d image14.png tidak ada)
- Section ini tampil kosong/broken saat ini

### 3.7 About Us
- Deskripsi perusahaan dalam Bahasa Indonesia (2 paragraf)
- Kotak Visi & Misi
- Foto perusahaan (`BMA.png`) — **file hilang**

### 3.8 Footer
- Kolom: Contact Us, Business Hours, Alamat Perusahaan, Alamat Toko
- Embed Google Maps (sudah terpasang, link kantor Cengkareng)
- Copyright tercantum "Ali Jaya Komputer" — **perlu diubah ke PT BMA**

---

## 4. Desain & Teknologi Saat Ini

### Color Palette
| Nama | Hex | Dipakai Untuk |
|---|---|---|
| Primary (Hijau Tua) | `#007208` | Navbar, judul, background footer |
| Secondary (Hijau Sedang) | `#008f07` | Gradient hero |
| Accent (Merah) | `#f10000` | Underline hover, harga, icon |
| Text Dark | `#1f2937` | Teks utama |
| Text Light | `#6b7280` | Teks deskripsi |
| Background Light | `#f9fafb` | Background section abu-abu muda |

### Font
- System font stack (tidak ada Google Fonts / custom font)
- `-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, ...`

### Animasi
- CSS `@keyframes`: slideDown (navbar), fadeIn (hero), slideUp (hero text)
- IntersectionObserver: fade-in saat scroll untuk semua `<section>`
- Flip card 3D pada product cards (hover)

### Tech Stack
- **Pure HTML/CSS/JavaScript** — tidak ada framework, tidak ada build tool
- Font Awesome 6.4.0 via CDN (untuk ikon)
- Tidak ada jQuery, tidak ada Bootstrap
- Tidak ada backend / database

### Responsif
- Breakpoint: `max-width: 768px`
- Mobile: hamburger menu, layout berubah jadi 1 kolom

---

## 5. Masalah & Catatan Penting untuk Redesign

### Konten
- [ ] Harga produk masih USD → ganti ke format IDR (Rp)
- [ ] Beberapa teks masih Bahasa Inggris (carousel, services, hero)
- [ ] Footer copyright salah ("Ali Jaya Komputer")
- [ ] Hero tidak punya tombol CTA
- [ ] Produk `pemadam.PNG` ada di folder tapi tidak ditampilkan

### Aset / Gambar
- [ ] Sediakan logo `bma.png` untuk navbar
- [ ] Sediakan foto `BMA.png` untuk section About
- [ ] Sediakan foto/logo 14 klien (`image.png` s/d `image14.png`)
- [ ] Ganti gambar carousel dari picsum ke foto produk asli
- [ ] Tambahkan produk Pemadam (sudah ada fotonya)

### Teknis
- [ ] Satu file HTML sangat besar (~1000+ baris) — pertimbangkan split jika pakai framework
- [ ] Tidak ada halaman detail produk
- [ ] Tidak ada form kontak / WhatsApp button
- [ ] Tidak ada favicon

---

## 6. Rencana Redesign (Isi saat mulai kerja)

> Bagian ini diisi sesuai keputusan desain yang diambil.

- **Framework/Template baru:** _(belum ditentukan)_
- **Warna baru:** _(belum ditentukan)_
- **Font baru:** _(belum ditentukan)_
- **Fitur baru yang ingin ditambahkan:** _(belum ditentukan)_
- **Halaman baru:** _(belum ditentukan)_
