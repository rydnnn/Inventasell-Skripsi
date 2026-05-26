# README
# 📦 Inventasell

> Sistem manajemen inventaris dan penjualan berbasis web yang dibangun dengan CodeIgniter 3.

![PHP](https://img.shields.io/badge/PHP-7.4+-777BB4?style=flat&logo=php&logoColor=white)
![CodeIgniter](https://img.shields.io/badge/CodeIgniter-3.x-EF4223?style=flat&logo=codeigniter&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-5.7+-4479A1?style=flat&logo=mysql&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-4-7952B3?style=flat&logo=bootstrap&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-green?style=flat)

---

## 📌 Tentang Project

**Inventasell** adalah aplikasi web untuk mengelola stok barang, transaksi pembelian & penjualan, serta laporan bisnis secara real-time. Dirancang untuk kebutuhan toko atau UMKM yang ingin mengdigitalisasi pencatatan inventaris mereka.

---

## ✨ Fitur

- 🔐 **Autentikasi** — Login multi-level (admin & pegawai)
- 📦 **Data Barang** — Kelola stok, tambah, edit, dan hapus produk
- 👤 **Data Pegawai** — Manajemen data karyawan beserta foto profil
- 🏭 **Data Supplier** — Kelola informasi supplier/vendor
- 🛒 **Pembelian** — Catat transaksi pembelian dari supplier
- 💰 **Penjualan** — Proses transaksi penjualan ke pelanggan
- 📊 **Laporan** — Laporan harian, bulanan, dan tahunan (stok, pembelian, penjualan)
- 🖨️ **Cetak Laporan** — Export laporan ke tampilan print-ready

---

## 🛠️ Tech Stack

| Komponen   | Teknologi                              |
|------------|----------------------------------------|
| Backend    | PHP 7.4+, CodeIgniter 3               |
| Database   | MySQL 5.7+                            |
| Frontend   | Bootstrap 4, jQuery, DataTables       |
| UI Library | Select2, SweetAlert, Font Awesome 4   |
| Server     | Apache / XAMPP / Laragon              |

---

## 🚀 Cara Instalasi

### Prasyarat

- PHP >= 7.4
- MySQL >= 5.7
- Apache web server (XAMPP / Laragon / WAMP)
- Git

### Langkah Instalasi

**1. Clone repository**
```bash
git clone https://github.com/[USERNAME]/inventasell.git
cd inventasell
```

**2. Import database**

- Buka phpMyAdmin (atau MySQL client pilihan lo)
- Buat database baru dengan nama `stok_barang1`
- Import file SQL yang ada di folder `database/` (jika tersedia)

**3. Konfigurasi database**

Salin file konfigurasi contoh:
```bash
cp application/config/database.example.php application/config/database.php
```

Lalu edit `application/config/database.php`:
```php
$db['default'] = array(
    'hostname' => 'localhost',
    'username' => 'root',       // sesuaikan
    'password' => '',           // sesuaikan
    'database' => 'stok_barang1',
    'dbdriver' => 'mysqli',
    // ...
);
```

**4. Konfigurasi base URL**

Edit `application/config/config.php`:
```php
$config['base_url'] = 'http://localhost/inventasell/';
```

**5. Jalankan aplikasi**

Taruh folder project di dalam `htdocs/` (XAMPP) atau `www/` (Laragon), lalu akses:
```
http://localhost/inventasell
```

---

## 🔑 Akun Default

| Role    | Username | Password |
|---------|----------|----------|
| Admin   | admin    | admin    |
| Pegawai | pegawai  | pegawai  |

> ⚠️ Harap ganti password default setelah instalasi pertama.

---

## 📁 Struktur Project

```
inventasell/
├── application/
│   ├── config/          # Konfigurasi CI (database, routes, autoload)
│   ├── controllers/     # Logic utama aplikasi
│   │   ├── Home.php         # Auth & dashboard
│   │   ├── Data_barang.php  # Manajemen produk
│   │   ├── Data_pegawai.php # Manajemen pegawai
│   │   ├── Data_supplier.php
│   │   ├── Pembelian.php
│   │   ├── Penjualan.php
│   │   └── Laporan.php
│   ├── models/          # Interaksi database
│   ├── views/           # Template tampilan (HTML/PHP)
│   │   ├── template/        # Layout utama & navbar
│   │   ├── laporan/         # Halaman laporan
│   │   └── cetak/           # Template cetak
│   └── libraries/       # Library custom
├── assets/
│   ├── css/             # Stylesheet
│   ├── js/              # JavaScript
│   ├── img/             # Gambar statis
│   └── foto/            # Foto upload pegawai
├── system/              # Core CodeIgniter (jangan diubah)
└── index.php
```

---

---

## 🤝 Kontribusi

Pull request sangat diterima! Untuk perubahan besar, silakan buka issue terlebih dahulu untuk mendiskusikan apa yang ingin diubah.

1. Fork repository ini
2. Buat branch fitur baru (`git checkout -b feature/fitur-baru`)
3. Commit perubahan (`git commit -m 'Tambah fitur baru'`)
4. Push ke branch (`git push origin feature/fitur-baru`)
5. Buat Pull Request

---

## 📄 Lisensi

Project ini menggunakan lisensi [MIT](LICENSE).

---

<p align="center">Dibuat dengan ❤️ menggunakan CodeIgniter 3</p>



