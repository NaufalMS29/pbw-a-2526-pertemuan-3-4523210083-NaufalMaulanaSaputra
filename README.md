<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

# Pertemuan 1 - (Request -> root -> view -> response)  
## Naufal Maulana Saputra  
## 4523210083  

# LaraPress - Aplikasi Blog Sederhana

LaraPress adalah aplikasi blog sederhana yang dibangun menggunakan Laravel 12 untuk tujuan pembelajaran dan pengembangan keterampilan web development.

<img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/d92db5f6-9eb2-434a-a821-42640d6ed601" />

Tampilan halaman utama LaraPress

## 📋 Tentang Proyek

Proyek ini dibuat sebagai bagian dari pembelajaran Laravel framework. LaraPress mendemonstrasikan konsep-konsep dasar Laravel seperti routing, views, dan struktur MVC.

## 🚀 Fitur yang Sudah Diimplementasikan

### 1. *Halaman Utama (Welcome Page)*
   - Mengubah tampilan default Laravel menjadi halaman sederhana
   - Menampilkan judul "Selamat Datang di LaraPress"
   - Struktur HTML yang bersih dan minimal

### 2. *Halaman Tentang Kami*
   - Route: /tentang-kami
   - Menampilkan informasi tentang LaraPress
   - Menjelaskan tujuan proyek sebagai pembelajaran Laravel 12

### 3. *Halaman Kontak*
   - Route: /kontak
   - Menampilkan informasi kontak pengembang

## 📁 Struktur File yang Dimodifikasi

### File yang Dibuat/Dimodifikasi:

1. **resources/views/welcome.blade.php**
   - Mengubah tampilan default Laravel yang kompleks menjadi struktur HTML sederhana
   - Menampilkan pesan sambutan untuk pengunjung blog

2. **resources/views/about.blade.php** (BARU)
   - File view baru untuk halaman "Tentang Kami"
   - Berisi informasi tentang LaraPress sebagai proyek pembelajaran

3. **resources/views/kontak.blade.php** (BARU)
   - File view baru untuk halaman "kontak"
   - Berisi informasi tentang kontak pengembang

4. **routes/web.php**
   - Menambahkan route baru /tentang-kami yang mengarah ke view about.blade.php
   - Menambahkan route baru /kontak yang mengarah ke view contact.blade.php

## 🛠 Langkah-langkah Implementasi

### Step 1: Modifikasi Halaman Welcome
Mengubah file resources/views/welcome.blade.php dari tampilan default Laravel (266 baris) menjadi HTML sederhana:

html
<!DOCTYPE html>
<html>
<head>
    <title>Selamat Datang di LaraPress</title>
</head>
<body>
    <h1>Selamat Datang di Blog LaraPress</h1>
    <p>Ini adalah halaman utama dari aplikasi blog kita.</p>
    <a href="/tentang-kami">Lihat Halaman Tentang Kami</a>
    <br>
    <a href="/">Kembali ke Halaman Utama</a>
</body>
</html>


### Step 2: Membuat Route Baru
Menambahkan route baru di routes/web.php:

php
Route::get('/tentang-kami', function () {
    return view('about');
});
Route::get('/kontak', function () {
    return view('kontak');
});


### Step 3: Membuat View About
Membuat file baru resources/views/about.blade.php:

html
<!DOCTYPE html>
<html>

<head>
    <title>Tentang Kami - LaraPress</title>
</head>

<body>
    <h1>Tentang LaraPress</h1>
    <p>LaraPress adalah sebuah proyek blog sederhana yang dibuat untuk mempelajari dasar-dasar framework Laravel 12.</p>
    <a href="/kontak">Lihat Halaman Kontak</a>
    <br>
    <a href="/">Kembali ke Halaman utama</a>
</body>

</html>


### Step 4: Membuat View kontak
Membuat file baru resources/views/kontak.blade.php:

html
<!DOCTYPE html>
<html>

<head>
    <title>Kontak Kami - LaraPress</title>
</head>

<body>
    <h1>Kontak LaraPress</h1>
    <p>Nama : Naufal Maulana Saputra</p>
    <p>NPM : 4523210083</p>
    <p>Email : naufal4523083@univpancasila.ac.id</p>
    <p>No.Hp : 082118768976</p>
    <a href="/tentang-kami">Lihat Halaman Tentang Kami</a>
    <br>
    <a href="/">Kembali ke Halaman Utama</a>
</body>

</html>


## 🌐 Endpoint yang Tersedia

| Route | Method | Deskripsi |
|-------|--------|-----------|
| / | GET | Halaman utama LaraPress |
| /tentang-kami | GET | Halaman tentang LaraPress |
| /contact | GET | Halaman tentang kontak pengembang |

## 💻 Teknologi yang Digunakan

- *Framework*: Laravel 12
- *PHP Version*: 8.x
- *Database*: MySQL
- *Frontend*: Blade Template Engine, HTML, CSS
- *Build Tool*: None

## 📦 Instalasi

1. Clone repository ini:

```bash
git clone https://github.com/NaufalMS29/pbw-a-2526-pertemuan-3-4523210083-NaufalMaulanaSaputra.git
```

2. Masuk Ke Directory LaraPress:

```bash
cd .\pbw-a-2526-pertemuan-3-4523210083-NaufalMaulanaSaputra\
```

5. Install dependencies:

```bash
composer install

dijalankan satu persatu atau di beda terminal dalam satu direktori

npm install
```

4. Buat file .env:

```bash
cp .env.example .env

copy .env.example .env
```

5. Generate application key:

```bash
php artisan key:generate
```

6. Jalankan development server:

```bash
php artisan serve
```

7. Akses aplikasi di browser:

```bash
http://localhost:8000
```

## 📸 Screenshot

### Halaman Utama
<img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/d92db5f6-9eb2-434a-a821-42640d6ed601" />
Halaman utama menampilkan sambutan sederhana kepada pengunjung blog LaraPress.

### Halaman Tentang Kami
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/dc8c20a7-6f13-4eac-9aec-95e69067c91f" />
Halaman Tentang LaraPress berisi informasi tentang LaraPress sebagai proyek pembelajaran

### Halaman Kontak
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/cd76033f-d3ea-4cf9-8f39-14705617c1a8" />
Halaman Kontak LarapPress berisi informasi kontak pengembang


