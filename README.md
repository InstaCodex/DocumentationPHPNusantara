# Documentation PHPNusantara

# 📅 Bulan Formatter – PHPNusantara

Library **Bulan** adalah bagian dari ekosistem **PHPNusantara** yang berfungsi untuk mengubah **angka bulan (1–12)** menjadi **nama bulan dalam Bahasa Indonesia**.

Cocok digunakan untuk:
- Aplikasi kasir
- Sistem akademik
- Laporan keuangan
- Aplikasi berbasis tanggal (PHP Native, Laravel, CodeIgniter)

---

## ✨ Fitur

- Konversi angka bulan ke nama bulan Indonesia
- Static method (mudah dipanggil)
- Ringan & tanpa dependency
- Aman dari input tidak valid

---

## 📂 Struktur File

```text
src/
└── App/
    └── Bulan.php
```

## 🚀 Cara Penggunaan PHP Native
```php
require __DIR__ . 'vendor/PHPNusantara/src/App/Bulan.php';

use PHPNusantara\App\Bulan;

echo Bulan::nama(1);
// Output: Januari
```

# 📡 Response Helper – PHPNusantara

Library **Response** adalah helper sederhana untuk **standarisasi response data** (biasanya untuk API / AJAX) dalam bentuk **array asosiatif**.

Cocok digunakan untuk:
- REST API PHP Native
- Laravel Controller
- CodeIgniter Controller
- AJAX / Fetch API
- Backend aplikasi kasir & sistem informasi

---

## ✨ Fitur

- Response sukses (success)
- Response data tidak ditemukan (notFound)
- Response error dengan pesan custom
- Format konsisten & mudah di-encode ke JSON
- Static method (langsung pakai)

---

## 📂 Struktur File

```text
src/
└── App/
    └── Response.php
```

## 🚀 Cara Penggunaan PHP Native
```php
require __DIR__ . 'vendor/PHPNusantara/src/App/Response.php';

use PHPNusantara\App\Response;

$data = [
    'id'   => 1,
    'nama' => 'Budi'
];

echo json_encode(Response::success($data));
 // Output ✅ Success:
    {
      "status": true,
      "message": "pria solo berhasil ditemukan",
      "data": {
        "id": 1,
        "nama": "Budi"
      }
    }
// Output ❌ Not Found:
    {
      "status": false,
      "message": "pria solo tidak ditemukan",
      "data": null
    }
// Output ⚠️ Error:
    {
      "status": false,
      "message": "Terjadi kesalahan",
      "data": null
    }
```
# ⏱️ Waktu Relatif – PHPNusantara

Library **WaktuRelatif** digunakan untuk mengubah **waktu absolut (datetime)** menjadi **format waktu relatif** yang mudah dibaca manusia (human readable time).

Contoh:
- `Baru saja`
- `5 menit lalu`
- `2 jam lagi`
- `3 hari lalu`

Cocok untuk:
- Feed / Timeline
- Log aktivitas
- Sistem komentar
- Notifikasi
- Dashboard admin

---

## ✨ Fitur

- Konversi waktu ke format relatif Bahasa Indonesia
- Mendukung waktu **lampau & masa depan**
- Aman dari input kosong / tidak valid
- Static method (mudah dipanggil)

---

## 📂 Struktur File

```text
src/
└── App/
    └── WaktuRelatif.php
```

## 🚀 Cara Penggunaan PHP Native
```php
require __DIR__ . 'vendor/PHPNusantara/src/App/WaktuRelatif.php';

use PHPNusantara\App\WaktuRelatif;

echo WaktuRelatif::dariSekarang('2026-01-16 08:00:00');
// Output: 2 jam yang lalu
```
# 🔤 String Helper – PHPNusantara

Library **StringHelper** adalah kumpulan helper untuk **manipulasi string Bahasa Indonesia** yang sering digunakan dalam aplikasi web.

Cocok untuk:
- Judul artikel
- URL slug
- Preview konten
- CMS / Blog
- Sistem informasi & dashboard

---

## ✨ Fitur

- Format judul otomatis (Title Case)
- Generator slug URL ramah SEO
- Potong teks dengan ellipsis (`...`)
- Static method (mudah dipanggil)
- Aman dari input kosong

---

## 📂 Struktur File

```text
src/
└── Bahasa/
    └── StringHelper.php
```

## 🚀 Cara Penggunaan PHP Native
```php
require __DIR__ . 'vendor/PHPNusantara/src/Bahasa/StringHelper.php';

use PHPNusantara\Bahasa\StringHelper;

echo StringHelper::judul('belajar php nusantara');
// Output: Belajar Php Nusantara

echo StringHelper::slug('Belajar PHP Nusantara!');
// Output: belajar-php-nusantara

echo StringHelper::potong('Ini adalah contoh teks yang sangat panjang', 20);
// Ini adalah contoh te...
```

# 🔢 Angka Formatter – PHPNusantara

Library **Angka** adalah helper untuk **memformat angka** ke format yang lebih **mudah dibaca** dan **user-friendly**, khususnya untuk kebutuhan aplikasi di Indonesia.

Cocok untuk:
- Statistik dashboard
- Jumlah pengunjung
- Total transaksi
- Laporan keuangan
- Tampilan ringkas angka besar

---

## ✨ Fitur

- Format angka dengan pemisah ribuan Indonesia (`.`)
- Dukungan desimal fleksibel
- Singkatan angka besar (`rb`, `jt`, `M`)
- Aman dari input non-numeric
- Static method (langsung pakai)

---

## 📂 Struktur File

```text
src/
└── Formatter/
    └── Angka.php
```

## 🚀 Cara Penggunaan PHP Native
```php
require __DIR__ . 'vendor/PHPNusantara/src/Formatter/Angka.php';

use PHPNusantara\Formatter\Angka;

echo Angka::format(1500000);
// Output: 1.500.000

echo Angka::format(1500000, 2);
// Output: 1.500.000,00

echo Angka::singkat(1500000);
// Output: 1.5 jt

```

# 📊 Persentase Formatter – PHPNusantara

Library **Persentase** digunakan untuk **memformat nilai persentase** ke format yang rapi dan sesuai standar Indonesia.

Mendukung:
- Nilai pecahan (`0.75` → `75%`)
- Nilai langsung (`75` → `75%`)
- Desimal fleksibel
- Penanganan input kosong / tidak valid

---

## ✨ Fitur

- Konversi pecahan ke persen otomatis
- Format angka Indonesia (`.` ribuan, `,` desimal)
- Dukungan desimal opsional
- Aman dari input null / string kosong
- Static method (mudah digunakan)

---

## 📂 Struktur File

```text
src/
└── Formatter/
    └── Persentase.php
```

## 🚀 Cara Penggunaan PHP Native
```php
require __DIR__ . 'vendor/PHPNusantara/src/Formatter/Persentase.php';

use PHPNusantara\Formatter\Persentase;

echo Persentase::format(0.75);
// Output: 75%

echo Persentase::format(0.756, 2);
// Output: 75,60%

echo Persentase::format(75, 0, false);
// Output: 75%

```

# 💰 Rupiah Formatter – PHPNusantara

Library **Rupiah** digunakan untuk **memformat angka ke mata uang Rupiah (IDR)** dengan format standar Indonesia.

Cocok untuk:
- Aplikasi kasir
- Sistem keuangan
- Invoice & laporan
- E-commerce
- Dashboard admin

---

## ✨ Fitur

- Format Rupiah dengan atau tanpa simbol `Rp`
- Dukungan desimal fleksibel
- Format angka Indonesia (`.` ribuan, `,` desimal)
- Aman dari input non-numeric
- Static method (mudah digunakan)

---

## 📂 Struktur File

```text
src/
└── Formatter/
    └── Rupiah.php
```

## 🚀 Cara Penggunaan PHP Native
```php
require __DIR__ . 'vendor/PHPNusantara/src/Formatter/Rupiah.php';

use PHPNusantara\Formatter\Rupiah;

echo Rupiah::format(1500000);
// Output: Rp 1.500.000

echo Rupiah::format(1500000, 2);
// Output: Rp 1.500.000,00

echo Rupiah::format(1500000, 0, false);
// Output: 1.500.000

```

# 📆 Tanggal Formatter – PHPNusantara

Library **Tanggal** digunakan untuk **memformat tanggal ke format Bahasa Indonesia**, misalnya:

> `2026-01-16` → **16 Januari 2026**

Library ini memanfaatkan **Bulan Formatter** untuk menampilkan nama bulan Indonesia.

Cocok untuk:
- Laporan
- Artikel / berita
- Sistem akademik
- Invoice & dokumen resmi
- Dashboard admin

---

## ✨ Fitur

- Format tanggal Indonesia (DD NamaBulan YYYY)
- Integrasi dengan `Bulan::nama()`
- Aman dari input kosong / tidak valid
- Static method (mudah digunakan)

---

## 📂 Struktur File

```text
src/
├── App/
│   └── Bulan.php
└── Formatter/
    └── Tanggal.php
```

## 🚀 Cara Penggunaan PHP Native
```php
require __DIR__ . 'vendor/PHPNusantara/src/App/Bulan.php';
require __DIR__ . 'vendor/PHPNusantara/src/Formatter/Tanggal.php';

use PHPNusantara\Formatter\Tanggal;

echo Tanggal::indo('2026-01-16');
// Output: 16 Januari 2026

```

# 📝 Terbilang Formatter – PHPNusantara

Library **Terbilang** digunakan untuk **mengubah angka menjadi teks terbilang Bahasa Indonesia**.

Contoh:
- `125` → **Seratus Dua Puluh Lima**
- `1000` → **Seribu**
- `-15` → **Minus Lima Belas**

Cocok untuk:
- Invoice
- Kwitansi
- Dokumen resmi
- Sistem keuangan
- Aplikasi administrasi

---

## ✨ Fitur

- Konversi angka ke teks Bahasa Indonesia
- Mendukung angka negatif
- Penulisan sesuai kaidah Indonesia
- Aman dari input non-numeric
- Static method (mudah digunakan)

---

## 📂 Struktur File

```text
src/
└── Formatter/
    └── Terbilang.php
```

## 🚀 Cara Penggunaan PHP Native
```php
require __DIR__ . 'vendor/PHPNusantara/src/Formatter/Terbilang.php';

use PHPNusantara\Formatter\Terbilang;

echo Terbilang::buat(125);
// Output: Seratus Dua Puluh Lima

```
# ⏰ Waktu Formatter – PHPNusantara

Library **Waktu** menyediakan berbagai helper untuk **memformat waktu** dan **menghitung selisih waktu** dalam format yang mudah dibaca.

Cocok untuk:
- Absensi
- Log aktivitas
- Jadwal
- Dashboard admin
- Sistem akademik & kepegawaian

---

## ✨ Fitur

- Format jam & menit (`HH:mm`)
- Format waktu lengkap (`HH:mm:ss`)
- Format tanggal + jam Indonesia
- Hitung selisih waktu (detik, menit, jam, hari)
- Integrasi dengan `Bulan` formatter
- Static method (mudah digunakan)

---

## 📂 Struktur File

```text
src/
├── App/
│   └── Bulan.php
└── Formatter/
    └── Waktu.php
```

## 🚀 Cara Penggunaan PHP Native
```php
require __DIR__ . 'vendor/PHPNusantara/src/App/Bulan.php';
require __DIR__ . 'vendor/PHPNusantara/src/Formatter/Waktu.php';

use PHPNusantara\Formatter\Waktu;

echo Waktu::jamMenit('2026-01-16 08:30:45');
// Output: 08:30

echo Waktu::lengkap('2026-01-16 08:30:45');
// Output: 08:30:45

echo Waktu::tanggalJamIndo('2026-01-16 08:30:45');
// Output: 16 Januari 2026 08:30
```
# 📧 Email Helper – PHPNusantara

Library **Email** adalah helper sederhana untuk **validasi** dan **masking email** demi keamanan dan privasi data pengguna.

Cocok untuk:
- Form registrasi & login
- Tampilan data user (disensor)
- Validasi input
- Sistem akun & autentikasi

---

## ✨ Fitur

- Validasi format email
- Masking email (sensor sebagian karakter)
- Aman dari input tidak valid
- Static method (mudah digunakan)

---

## 📂 Struktur File

```text
src/
└── Identity/
    └── Email.php
```

## 🚀 Cara Penggunaan PHP Native
```php
require __DIR__ . 'vendor/PHPNusantara/src/Identity/Email.php';

use PHPNusantara\Identity\Email;

Email::valid('user@email.com'); 

// Output: true

Email::mask('user@email.com');

// Output: user*@email.com

```

# 📞 Telepon Identity – PHPNusantara

Library **Telepon** adalah bagian dari ekosistem **PHPNusantara** yang berfungsi untuk **validasi, normalisasi, dan masking nomor HP Indonesia** 🇮🇩.

Cocok digunakan untuk:
- Form pendaftaran
- Sistem login berbasis nomor HP
- Aplikasi kasir & UMKM
- API backend (PHP Native, Laravel, CodeIgniter)

---

## ✨ Fitur

- Validasi nomor HP Indonesia
- Normalisasi format (`+62`, `62` → `08`)
- Masking nomor HP (keamanan data)
- Static method
- Ringan & tanpa dependency

---

## 📂 Struktur File

```text
src/
└── Identity/
    └── Telepon.php
```

## 🚀 Cara Penggunaan PHP Native
```php
require __DIR__ . 'vendor/PHPNusantara/src/Identity/Telepon.php';

use PHPNusantara\Identity\Telepon;

Telepon::valid('08123456789');
// Output: true

Telepon::normalize('+628123456789');
// Output: 08123456789

Telepon::mask('08123456789');
// Output: 08123****789

```

# 🆔 NIK Identity – PHPNusantara

Library **NIK** adalah bagian dari ekosistem **PHPNusantara** yang berfungsi untuk **validasi, masking, dan ekstraksi tanggal lahir dari Nomor Induk Kependudukan (KTP Indonesia)**.

Cocok digunakan untuk:
- Sistem akademik
- Aplikasi pemerintahan
- Sistem registrasi warga
- Validasi data pengguna

---

## ✨ Fitur

- Validasi NIK 16 digit
- Deteksi tanggal lahir dari NIK
- Masking NIK (keamanan data)
- Static method
- Tanpa dependency eksternal

---

## 📂 Struktur File

```text
src/
└── Identity/
    └── NIK.php
```

## 🚀 Cara Penggunaan PHP Native
```php
require __DIR__ . 'vendor/PHPNusantara/src/Identity/NIK.php';

use PHPNusantara\Identity\NIK;

NIK::valid('3175091203980001');
// Output: true

NIK::mask('3175091203980001');
// Output: 317509********01

NIK::tanggalLahir('3175091203980001');
// Output: 1998-03-12

```






