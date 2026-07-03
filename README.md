# 🏠 AsetKu — Inventaris Rumah Tangga

Aplikasi pencatatan aset rumah tangga berbasis web dengan **antarmuka modern, animasi premium, dan 10 tema warna**. Dirancang untuk membantu Anda mencatat, mengelola, dan memantau semua barang berharga di rumah dengan mudah dan menyenangkan.

<p align="center">
  <img src="https://img.shields.io/badge/version-2.0-orange" alt="Version">
  <img src="https://img.shields.io/badge/HTML-5-orange" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS-3-blue" alt="CSS3">
  <img src="https://img.shields.io/badge/JavaScript-ES6-yellow" alt="JavaScript">
  <img src="https://img.shields.io/badge/license-MIT-green" alt="License">
  <img src="https://img.shields.io/badge/platform-web-lightgrey" alt="Platform">
</p>

---

## ✨ Fitur Unggulan

| Fitur | Keterangan |
|-------|------------|
| 📊 **Dashboard Interaktif** | Total aset, total nilai, rata-rata, dan transaksi dalam satu tampilan. Dilengkapi 8 jenis grafik (Bar, Area, Doughnut, Radar, Polar, H-Bar, Line, Bubble) yang bisa dipilih sesuai selera. |
| 📦 **Manajemen Aset** | Tambah, edit, hapus aset dengan kode, SN, nama, kategori, kondisi, harga beli, harga jual, stok, dan tanggal masuk. Pencarian dan filter kategori memudahkan navigasi. |
| 🤝 **Jual / Beli** | Catat penjualan (aset otomatis terhapus) atau pembelian (aset otomatis bertambah) dengan riwayat transaksi lengkap. |
| 🎨 **10 Tema Warna** | Industrial, Hi-Tech, Islami, Gaming, Moonlight, Forest, Sunset, Ocean, Lavender, Monochrome. Ganti tema kapan saja! |
| 🌓 **Dark / Light Mode** | Tampilan gelap atau terang sesuai preferensi Anda. Tersimpan otomatis di browser. |
| 🏷️ **Manajemen Kategori** | Tambah atau hapus kategori sesuai kebutuhan rumah tangga Anda. |
| 💾 **Backup & Restore** | Export data ke file `.cfg` atau import kembali. Juga tersedia export/import Excel untuk aset. |
| 📱 **Responsif** | Tampilan optimal di desktop, tablet, dan smartphone. |
| ✨ **Animasi Premium** | Transisi spring, staggered entry, ripple effect, partikel interaktif, dan berbagai efek halus yang membuat pengalaman pengguna terasa premium. |

---

## 🚀 Demo & Penggunaan

### 📥 Instalasi

Karena aplikasi ini adalah **single-file HTML**, Anda hanya perlu:

1. **Unduh** file `index.html`
2. **Buka** dengan browser modern (Chrome, Firefox, Edge, Safari)
3. **Mulai gunakan** — semua data disimpan di `localStorage` browser Anda.

> **Catatan:** Tidak perlu server, tidak perlu instalasi, tidak perlu koneksi internet (kecuali untuk loading font & library Chart.js/XLSX).

### 🖥️ Cara Penggunaan

#### Dashboard
- Lihat ringkasan aset dan nilai total
- Pilih jenis grafik dengan mengklik tombol di atas grafik
- Pantau aktivitas terbaru di panel notifikasi

#### Aset
- Klik **"Tambah Aset"** untuk menambahkan barang baru
- Gunakan **pencarian** dan **filter kategori** untuk menemukan aset dengan cepat
- Klik ikon **edit (✏️)** untuk mengubah data, **hapus (🗑️)** untuk menghapus, atau **jual (🤝)** untuk langsung menjual

#### Jual / Beli
- **Jual Aset:** Pilih aset, tentukan harga jual dan pembeli, lalu klik "Jual Aset" — aset otomatis terhapus dari inventaris
- **Beli Aset:** Isi nama, kategori, harga, dan kondisi, lalu klik "Tambah Aset" — aset otomatis masuk ke inventaris
- Riwayat transaksi tersimpan dan ditampilkan di bagian bawah

#### Pengaturan
- **Tampilan:** Pilih Dark/Light mode dan 10 tema warna
- **Nama Aplikasi:** Ubah sesuai keinginan
- **Kategori:** Tambah atau hapus kategori
- **Data & Backup:** Export/import data, reset semua data

---

## 🎨 Tema Warna

| Tema | Warna Aksen | Preview |
|------|-------------|---------|
| **Industrial** (Default) | 🟠 Orange | `#f97316` |
| **Hi-Tech** | 🔵 Cyan | `#00d4ff` |
| **Islami** | 🟢 Green | `#2e7d32` |
| **Gaming** | 🟣 Neon Purple | `#a855f7` |
| **Moonlight** | 🔵 Soft Blue | `#60a5fa` |
| **Forest** | 🟢 Hijau Daun | `#22c55e` |
| **Sunset** | 🔴 Merah | `#f43f5e` |
| **Ocean** | 🔵 Biru Laut | `#0ea5e9` |
| **Lavender** | 🟣 Ungu Lembut | `#a78bfa` |
| **Monochrome** | ⚪ Abu-abu | `#94a3b8` |

---

## 🛠️ Teknologi

| Teknologi | Fungsi |
|-----------|--------|
| **HTML5** | Struktur aplikasi |
| **CSS3** | Styling, tema, animasi, glassmorphism |
| **JavaScript (ES6)** | Logika aplikasi, interaktivitas |
| **Chart.js** | Visualisasi grafik interaktif |
| **XLSX (SheetJS)** | Export/import file Excel |
| **Font Awesome** | Ikon vektor |
| **Google Fonts (Inter)** | Tipografi modern |
| **localStorage** | Penyimpanan data offline |

---

## 📁 Struktur Data

Aplikasi menyimpan data di `localStorage` dengan struktur:

```json
{
  "assets": [...],
  "transactions": [...],
  "settings": {
    "ownerName": "Pemilik Rumah",
    "appName": "AsetKu",
    "defaultTheme": "dark",
    "colorTheme": "industrial",
    "categories": ["elektronik", "perabotan", "kendaraan", "peralatan", "lainnya"]
  },
  "assetCounter": 0,
  "transactionCounter": 0
}
