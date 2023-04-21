# Fundamentals of PHP
PHP (Hypertext Preprocessor) adalah bahasa pemrograman server-side yang paling umum digunakan untuk membangun situs web dan aplikasi web dinamis. PHP pertama kali dirilis pada tahun 1995 dan saat ini merupakan salah satu bahasa pemrograman paling populer di dunia.

PHP adalah bahasa pemrograman server-side yang kuat dan serbaguna. Dengan kemampuan untuk memproses formulir, mengelola database, dan berintegrasi dengan mudah dengan server web dan database, PHP menjadi bahasa pemrograman pilihan untuk banyak pengembang web. Selain itu, kemampuan untuk membuat fungsi dan kelas sendiri membuat PHP lebih mudah dikembangkan untuk aplikasi yang lebih kompleks.

# Contents
1. [Tipe Data Dalam Bahasa Program PHP](#tipe-data-dalam-bahasa-program-php)
    - [Integer](#1-integer)

# Tipe Data Dalam Bahasa Program PHP
PHP memiliki beberapa tipe data yang berbeda yang digunakan untuk menyimpan nilai dan informasi. Berikut ini adalah tipe data dalam bahasa pemrograman PHP beserta deskripsi dan ukuran memori yang digunakan:

| Tipe Data | Deskripsi                  | Ukuran Memori |
|-----------|----------------------------|---------------|
| Integer   | Bilangan bulat             | 4 byte        |
| Float     | Bilangan pecahan           | 8 byte        |
| String    | Kumpulan karakter          | variabel      |
| Boolean   | Nilai benar atau salah     | 1 byte        |
| Array     | Kumpulan data              | variabel      |
| Object    | Instance dari sebuah class | variabel      |
| NULL	     | Tidak memiliki nilai       | 0 byte        |

> Ukuran memori **variable** bisa bervariasi dari 1 byte sampai beberapa kilobyte tergantung pada tipe datanya.

Berikut adalah daftar tipe data yang tersedia di PHP beserta contoh penggunaannya:

## 1. Integer
Tipe data `Integer` pada PHP digunakan untuk merepresentasikan bilangan bulat, baik positif maupun negatif. Berikut adalah
contoh penggunaan tipe data Integer pada PHP:

```php
// Mendefinisikan variabel dengan tipe data Integer
$angka = 10;

// Operasi aritmatika menggunakan tipe data Integer
$hasil_penjumlahan = 5 + 3; // 8

// Menampilkan variabel dengan tipe data Integer
echo $angka; // 10
```

Tipe data Integer dapat menyimpan bilangan bulat dengan rentang nilai antara -`2147483648` hingga `2147483647` pada 
sistem **32-bit**, atau `-9223372036854775808` hingga `9223372036854775807` pada sistem **64-bit**.

```php
echo "Nilai maksimum integer: " . PHP_INT_MAX; // output: Nilai maksimum integer: 9223372036854775807
echo "Nilai minimum integer: " . PHP_INT_MIN; // output: Nilai minimum integer: -9223372036854775808
```

Selain itu, tipe data Integer juga dapat dituliskan dalam format heksadesimal (base 16), oktal (base 8), atau biner
(base 2), dengan menggunakan awalan 0x untuk heksadesimal, 0 untuk oktal, dan 0b untuk biner. Berikut adalah contoh 
penggunaan tipe data Integer dengan format lain pada PHP:

```php
// Tipe data Integer dalam format heksadesimal
$angka_hex = 0x10; // 16

// Tipe data Integer dalam format oktal
$angka_oct = 012; // 10

// Tipe data Integer dalam format biner
$angka_bin = 0b1010; // 10
```

Dalam operasi aritmatika, tipe data `Integer` dapat digunakan dalam berbagai jenis operasi, seperti penjumlahan,
pengurangan, perkalian, pembagian, modulo, dan lain sebagainya. Berikut adalah contoh penggunaan tipe data `Integer` dalam
operasi aritmatika pada PHP:

```php
// Operasi aritmatika menggunakan tipe data Integer
$hasil_penjumlahan = 5 + 3; // 8
$hasil_pengurangan = 5 - 3; // 2
$hasil_perkalian = 5 * 3; // 15
$hasil_pembagian = 5 / 3; // 1 (integer division)
$hasil_modulo = 5 % 3; // 2
```

Pada PHP, tipe data integer juga dapat diubah menjadi tipe data float menggunakan tanda desimal atau notasi ilmiah. 
Contoh:
```php
$angka = 10;
$angka_float = 10.0;
$angka_sains = 1e3; // sama dengan 1000
```
