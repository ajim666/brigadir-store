# 📚 PANDUAN LENGKAP WEBSITE BRIGADIR

## 🎯 STRUKTUR WEBSITE

Website ini terdiri dari **5 halaman HTML**:

```
📁 Website BRIGADIR/
├── 📄 index-main.html      → Halaman Utama
├── 📄 activities.html      → Semua Kegiatan
├── 📄 products.html        → Semua Produk Sewa
├── 📄 product-detail.html  → Detail Produk + WhatsApp
└── 📄 products.csv         → Data Produk
```

---

## 🏠 HALAMAN UTAMA (index-main.html)

### Fitur:
✅ **Header** - Logo BRIGADIR + Navigasi
✅ **Hero Slideshow** - Background foto auto-ganti setiap 4 detik
✅ **Section Activities** - Tampil 3 kegiatan + tombol "All Activity"
✅ **Section Products** - Tampil 6 produk + tombol "Show All Products"
✅ **Section About** - Tentang BRIGADIR
✅ **Footer** - Informasi kontak

### Hero Slideshow:
- **Judul**: "BRIGADIR"
- **Tagline**: "Bersama Membangun Prestasi" (bisa diganti)
- **Background**: Auto-ganti 3 foto setiap 4 detik

**CARA GANTI FOTO SLIDESHOW:**

1. Buka `index-main.html`
2. Cari bagian ini (sekitar baris 250-254):

```html
.slide:nth-child(1) {
    background: linear-gradient(135deg, #1a1a1a 0%, #2d2d2d 100%);
}
```

3. Ganti dengan foto asli:

```html
.slide:nth-child(1) {
    background-image: url('foto-brigadir-1.jpg');
    background-size: cover;
    background-position: center;
}

.slide:nth-child(2) {
    background-image: url('foto-brigadir-2.jpg');
    background-size: cover;
    background-position: center;
}

.slide:nth-child(3) {
    background-image: url('foto-brigadir-3.jpg');
    background-size: cover;
    background-position: center;
}
```

**CARA GANTI TAGLINE:**

Cari baris:
```html
<p class="hero-tagline">Bersama Membangun Prestasi</p>
```

Ganti dengan tagline Anda (3-5 kata):
```html
<p class="hero-tagline">Generasi Unggul Berkarakter</p>
```

---

## 🎯 HALAMAN ACTIVITIES (activities.html)

### Fitur:
- Menampilkan **semua kegiatan** BRIGADIR
- Grid layout responsive
- Setiap card: Foto + Tanggal + Judul + Deskripsi

**CARA TAMBAH KEGIATAN:**

1. Buka `activities.html`
2. Copy template ini:

```html
<div class="activity-card">
    <div class="activity-image">📸</div>
    <div class="activity-content">
        <div class="activity-date">Bulan Tahun</div>
        <h3 class="activity-title">Judul Kegiatan</h3>
        <p class="activity-description">Deskripsi kegiatan...</p>
    </div>
</div>
```

3. Ganti emoji dengan foto:

```html
<div class="activity-image">
    <img src="foto-kegiatan.jpg" alt="Judul Kegiatan">
</div>
```

---

## 🛒 HALAMAN PRODUCTS (products.html)

### Fitur:
- Membaca data dari **products.csv**
- Menampilkan **semua produk** sewa
- Auto-format harga ke Rupiah

**Halaman ini OTOMATIS membaca dari CSV!**

---

## 📦 HALAMAN PRODUCT DETAIL (product-detail.html)

### Fitur:
✅ Foto produk besar
✅ Nama, kategori, harga
✅ Rating & reviews
✅ Deskripsi lengkap
✅ Detail produk (tabel)
✅ **Tombol WhatsApp** (paling penting!)

### ⚠️ PENTING - SETTING NOMOR WHATSAPP:

1. Buka `product-detail.html`
2. Cari baris ini (sekitar baris 384):

```javascript
const WHATSAPP_NUMBER = '6281234567890'; // GANTI INI!
```

3. Ganti dengan nomor WhatsApp persewaan Anda:

```javascript
const WHATSAPP_NUMBER = '6281234567890'; // Format: 628xxx (tanpa +)
```

**Format Nomor:**
- ✅ Benar: `6281234567890`
- ❌ Salah: `+6281234567890`
- ❌ Salah: `081234567890`

---

## 📊 FILE products.csv

### Format CSV:

```csv
id,category,name,description,price,image,rating,reviews
1,Sound System,Speaker Aktif 15 inch,Speaker berkualitas dengan suara jernih,100000,🔊,5,45
2,Tenda,Tenda Pesta 5x5m,Tenda untuk acara outdoor,250000,⛺,5,32
```

### Penjelasan Kolom:

| Kolom | Keterangan | Contoh |
|-------|------------|--------|
| `id` | ID unik (1, 2, 3, ...) | 1 |
| `category` | Kategori produk | Sound System |
| `name` | Nama produk | Speaker Aktif 15 inch |
| `description` | Deskripsi singkat | Speaker berkualitas... |
| `price` | Harga per hari (angka tanpa titik) | 100000 |
| `image` | URL foto atau emoji | 🔊 atau https://... |
| `rating` | Rating 1-5 | 5 |
| `reviews` | Jumlah review | 45 |

### CARA TAMBAH PRODUK:

1. Buka `products.csv` dengan Excel/Google Sheets
2. Tambah baris baru:

```
3,Lighting,Lampu PAR LED,Lampu panggung warna-warni,75000,💡,5,28
```

3. Save as CSV
4. Upload ke website

### CARA EDIT PRODUK:

1. Buka CSV
2. Edit kolom yang diinginkan
3. Save as CSV
4. Upload ulang

---

## 🎨 WARNA WEBSITE

Sesuai logo BRIGADIR:
- **Hitam** (#1a1a1a) - Header, footer, tombol
- **Emas** (#f4d03f) - Aksen, border, highlight
- **Abu Terang** (#f8f9fa) - Background
- **Putih** (#ffffff) - Card, konten

---

## 📁 STRUKTUR FILE LENGKAP

```
📁 Website BRIGADIR/
├── 📄 index-main.html
├── 📄 activities.html
├── 📄 products.html
├── 📄 product-detail.html
├── 📄 products.csv
└── 📁 images/ (opsional - untuk foto)
    ├── foto-brigadir-1.jpg
    ├── foto-brigadir-2.jpg
    ├── foto-kegiatan-1.jpg
    └── ...
```

---

## 🚀 CARA UPLOAD KE HOSTING

### Opsi 1: Hosting Gratis

**GitHub Pages:**
1. Buat repository di GitHub
2. Upload semua file
3. Settings → Pages → Deploy
4. Akses di `username.github.io/repo-name`

**Netlify:**
1. Drag & drop folder ke netlify.com
2. Otomatis deploy
3. Dapat domain gratis

### Opsi 2: Hosting Berbayar

1. Beli hosting + domain
2. Login cPanel
3. File Manager → Upload semua file
4. Akses via domain Anda

---

## ⚙️ SETTING YANG PERLU DIGANTI

### 1. Nomor WhatsApp
File: `product-detail.html` baris 384
```javascript
const WHATSAPP_NUMBER = '6281234567890'; // GANTI!
```

### 2. Email Kontak
File: `index-main.html` + `activities.html` + `products.html`
```html
<p>Email: brigadir@school.ac.id</p>
```

### 3. Nomor Telepon
```html
<p>Phone: +62 812 3456 7890</p>
```

### 4. Alamat
```html
<p>Kota Kediri, Jawa Timur</p>
```

### 5. Tagline Hero
File: `index-main.html`
```html
<p class="hero-tagline">Bersama Membangun Prestasi</p>
```

### 6. About Text
File: `index-main.html` (section about)

---

## 📸 CARA GANTI EMOJI DENGAN FOTO

### Untuk Kegiatan:

**Sebelum:**
```html
<div class="activity-image">📸</div>
```

**Sesudah:**
```html
<div class="activity-image">
    <img src="foto-kegiatan.jpg" alt="Bakti Sosial">
</div>
```

### Untuk Produk (di CSV):

**Sebelum:**
```csv
1,Sound System,Speaker,Deskripsi,100000,🔊,5,45
```

**Sesudah:**
```csv
1,Sound System,Speaker,Deskripsi,100000,https://i.imgur.com/gambar.jpg,5,45
```

---

## 🔧 TROUBLESHOOTING

### ❌ Produk tidak muncul
**Solusi:**
- Cek nama file: harus `products.csv`
- Cek format CSV (koma sebagai pemisah)
- Pastikan file di folder yang sama

### ❌ Foto tidak muncul
**Solusi:**
- Cek URL foto bisa diakses
- Atau gunakan path relatif: `images/foto.jpg`

### ❌ WhatsApp tidak berfungsi
**Solusi:**
- Cek format nomor: `628xxx` (tanpa +)
- Test di browser dulu

### ❌ Slideshow tidak ganti
**Solusi:**
- Buka Console (F12) → lihat error
- Pastikan ada 3 div dengan class `slide`

---

## 📱 RESPONSIVE DESIGN

Website sudah **100% responsive** untuk:
- ✅ Desktop (1920px+)
- ✅ Laptop (1366px)
- ✅ Tablet (768px)
- ✅ Mobile (375px)

---

## ✨ FITUR WEBSITE

✅ Design soft & elegant
✅ Warna sesuai logo BRIGADIR
✅ Hero slideshow otomatis
✅ Grid responsive
✅ Hover effects smooth
✅ WhatsApp integration
✅ CSV untuk data produk
✅ SEO friendly
✅ Fast loading

---

## 📞 KONTAK SUPPORT

Jika ada pertanyaan tentang website ini, silakan hubungi developer.

**Selamat menggunakan website BRIGADIR! 🎉**

---

© 2024 BRIGADIR - Website by Claude
