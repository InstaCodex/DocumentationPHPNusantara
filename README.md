# DocumentationPHPNusantara

## 🚀 Panduan Penggunaan

### 1 PHP Native – Format Rupiah

```php
<?php
require __DIR__ . '/vendor/PHPNusantara/src/Formatter/Rupiah.php';

use PHPNusantara\Formatter\Rupiah;

echo Rupiah::format(1500000);
// Output: Rp 1.500.000

```
### 2 PHP Native – Format Tanggal

```php
<?php
require __DIR__ . '/vendor/PHPNusantara/src/Formatter/Tanggal.php';
require __DIR__ . '/vendor/PHPNusantara/src/App/Bulan.php';

use PHPNusantara\Formatter\Tanggal;

echo Tanggal::indo('2026-01-15');
// Output: 15 Januari 2026

```

### 3 PHP Native – Format Hari

```php
<?php
require __DIR__ . '/vendor/PHPNusantara/src/Formatter/Hari.php';

use PHPNusantara\Formatter\Hari;

echo Hari::format('2026-01-15');
// Output: Kamis
```

### 4 PHP Native – Format Terbilang

```php
<?php
require __DIR__ . '/vendor/PHPNusantara/src/Formatter/Terbilang.php';

use PHPNusantara\Formatter\Terbilang;

echo Terbilang::buat(1500000);
// Output: Satu Juta Lima Ratus Ribu

```

### 5 PHP Native – Format Angka Indonesia

```php
<?php
require __DIR__ . '/vendor/PHPNusantara/src/Formatter/Angka.php';

use PHPNusantara\Formatter\Angka;

echo Angka::format(1500000);
// Output: 1.500.000

echo Angka::singkat(1500000);
// Output: 1.5 jt

```

### 6 PHP Native – Format Waktu Lengkap

```php
<?php
require __DIR__ . '/vendor/PHPNusantara/src/Formatter/Waktu.php';
require __DIR__ . '/vendor/PHPNusantara/src/App/Bulan.php';

use PHPNusantara\Formatter\Waktu;

echo Waktu::tanggalJamIndo('2026-01-15 14:30:00');
// Output: 15 Januari 2026 14:30

```

### 7 PHP Native – Format Sensor Email

```php
<?php
require __DIR__ . '/vendor/PHPNusantara/src/Identity/Email.php';

use PHPNusantara\Identity\Email;

$email = 'PHPNusantara@gmail.com';

echo Email::mask($email, 6);
// Output: PHPNu******@gmail.com

```

### 8 PHP Native – Format Judul, Slug, Potong

```php
<?php
require __DIR__ . '/vendor/PHPNusantara/src/Bahasa/StringHelper.php';

use PHPNusantara\Bahasa\StringHelper;

echo StringHelper::judul('belajar php nusantara');
// Belajar Php Nusantara

echo StringHelper::slug('Belajar PHP Nusantara 2026!');
// belajar-php-nusantara-2026

echo StringHelper::potong(
    'PHPNusantara adalah library PHP untuk kebutuhan format Indonesia', 30
);
// PHPNusantara adalah library...

```

### 9 PHP Native – Format Nama Bulan Indonesia

```php
<?php
require __DIR__ . '/vendor/PHPNusantara/src/App/Bulan.php';

use PHPNusantara\App\Bulan;

echo Bulan::nama(1);
// Output: Januari

```

### 10 PHP Native – Format Response Helper

```php
<?php
require __DIR__ . '/vendor/PHPNusantara/src/App/Response.php';

use PHPNusantara\App\Response;

print_r(Response::success([
    'nama' => 'Budi',
    'asal' => 'Solo'
]));
// Output:
  {
        "status": true,
        "message": "pria solo berhasil ditemukan",
        "data": {
          "nama": "Budi",
          "asal": "Solo"
        }
  }
```

### 11 PHP Native – Format Persentase

```php
<?php
require __DIR__ . '/vendor/PHPNusantara/src/Formatter/Persentase.php';

use PHPNusantara\Formatter\Persentase;

echo Persentase::format(0.25);
// Output: 25%

```
