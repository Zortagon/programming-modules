# Fundamentals of PHP
PHP (Hypertext Preprocessor) adalah bahasa pemrograman server-side yang paling umum digunakan untuk membangun situs web dan aplikasi web dinamis. PHP pertama kali dirilis pada tahun 1995 dan saat ini merupakan salah satu bahasa pemrograman paling populer di dunia.

PHP adalah bahasa pemrograman server-side yang kuat dan serbaguna. Dengan kemampuan untuk memproses formulir, mengelola database, dan berintegrasi dengan mudah dengan server web dan database, PHP menjadi bahasa pemrograman pilihan untuk banyak pengembang web. Selain itu, kemampuan untuk membuat fungsi dan kelas sendiri membuat PHP lebih mudah dikembangkan untuk aplikasi yang lebih kompleks.

# Contents
1. [Struktur Dasar PHP](#struktur-dasar-php)
2. [Tipe Data Dalam Bahasa Program PHP](#tipe-data-dalam-bahasa-program-php)
    - [Integer](#1-integer)
    - [Float](#2-float)
    - [String](#3-string)
    - [Boolean](#4-boolean)
    - [Array](#5-array)
    - Object
    - NULL
3. Variable dan Konstanta
   - Deklarasi Variable
   - Tipe Data pada Variable
   - Konstanta
4. Operator dalam PHP
   - Operator Aritmatika
   - Operator Penugasan
   - Operator Perbandingan
   - Operator Logika
5. Percabangan dalam PHP
   - If-Else
   - Switch-Case

# Struktur Dasar PHP
Berikut adalah struktur dasar PHP:
```php
<?php
  // kode PHP di sini
?>
```
- Kode PHP harus dimulai dengan `<?php`
- Diakhiri dengan `?>` (Tetapi tidak wajib jika di file PHP tersebut tidak ada HTML).
- Kode PHP dapat ditempatkan di antara kode HTML atau teks biasa.
- Kode PHP dapat mencetak output ke layar dengan menggunakan fungsi `echo`.
- Komentar dapat ditulis dengan menggunakan `//` untuk komentar satu baris atau `/* */` untuk komentar beberapa baris.

Berikut beberapa contoh menulis kode PHP:
```php
<?php
echo "Hello World!";
```
> Tag penutup `?>` tidak diwajib kan karena diatas hanya ada kode PHP.
```php
<!doctype html>
<html lang="en">
<head>
    <title>Document</title>
</head>
<body>
    <h1>
        <?php echo "Hello World"; // Akan print tulisan Hello World pada tag h1 ?>
    </h1>
</body>
</html>
```
> Tag penutup `?>` wajib karena kode PHP berada di HTML.


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

## 2. Float
Tipe data Float pada PHP digunakan untuk merepresentasikan bilangan pecahan atau desimal. Float pada PHP memiliki
presisi sekitar 14 digit dan dapat digunakan untuk menghitung nilai matematika dengan akurasi yang cukup baik.

Contoh penggunaan tipe data Float pada PHP:
```php
$pi = 3.14159265359;
$radius = 2.5;
$luas = $pi * $radius * $radius;
echo "Luas lingkaran dengan jari-jari $radius adalah $luas";
```

Pada contoh di atas, variabel `$pi` dan `$radius` dideklarasikan sebagai tipe data Float. Kemudian nilai dari variabel
`$luas` dihitung menggunakan rumus luas lingkaran dan dicetak ke layar.

## 3. String
Pada PHP, sebuah string dapat ditulis menggunakan tanda kutip tunggal ('...') atau tanda kutip ganda ("..."). String 
yang ditulis dengan tanda kutip tunggal dan ganda memiliki arti yang sama, kecuali jika terdapat karakter khusus yang
perlu dilakukan escapenya.

String dapat dibuat dengan beberapa cara, di antaranya:

- Dalam tanda kutip tunggal ('...'):
```php
$nama = 'John Doe';
```
- Dalam tanda kutip ganda ("..."):
```php
$nama = "John Doe";
```
- Dalam tanda kutip backtick (\`...\`):
```php
$nama = `John Doe`;
```
> **Note:** Semua cara pembuatan string diatas sama saja

Berikut adalah beberapa contoh penggunaan tipe data String di PHP:
```php
// deklarasi string dengan tanda kutip tunggal
$nama = 'Joko';

// deklarasi string dengan tanda kutip ganda
$salam = "Halo $nama, apa kabar?";

// output: Halo Joko, apa kabar?
echo $salam;
```
Pada contoh di atas, variabel `$nama` memiliki nilai string "Joko", sedangkan variabel `$salam` memiliki nilai string "Halo
Joko, apa kabar?". Dalam string `$salam`, terdapat penggunaan variabel `$nama` di dalamnya, yang dikelilingi dengan tanda 
kutip ganda. Dalam hal ini, PHP akan melakukan substitusi nilai variabel ke dalam string, sehingga variabel `$salam`
memiliki nilai "Halo Joko, apa kabar?".

Pada PHP terdapat sejumlah fungsi bawaan untuk memanipulasi string. Berikut ini adalah beberapa conto untuk
memanipulasi string pada PHP:

- **Konkatenasi**: Menggabungkan dua atau lebih string menggunakan operator titik (`.`):
```php
$nama_depan = 'John';
$nama_belakang = 'Doe';
$nama_lengkap = $nama_depan . ' ' . $nama_belakang;
echo $nama_lengkap; // Output: John Doe
```
- **Pemotongan string**: Memotong sebagian string menggunakan fungsi `substr()`:
```php
$nama = 'John Doe';
$nama_depan = substr($nama, 0, 4);
echo $nama_depan; // Output: John
```
- **Penggantian string**: Mengganti sebagian string menggunakan fungsi `str_replace()`:
```php
$kalimat = 'Saya suka makan nasi goreng';
$kalimat_baru = str_replace('nasi goreng', 'mie goreng', $kalimat);
echo $kalimat_baru; // Output: Saya suka makan mie goreng
```
- **Pencarian string**: Mencari posisi sebuah string menggunakan fungsi `strpos()`:
```php
$kalimat = 'Saya suka makan nasi goreng';
$posisi = strpos($kalimat, 'nasi');
echo $posisi; // Output: 13
```
- **Formatting string**: Memformat string menggunakan fungsi `sprintf()`:
```php
$harga = 10000;
$diskon = 0.1;
$harga_diskon = $harga * (1 - $diskon);
echo sprintf('Harga setelah diskon 10%% adalah Rp. %s', number_format($harga_diskon, 0, ',', '.')); // Output: Harga setelah diskon 10% adalah Rp. 9.000
```
Selain itu, pada PHP terdapat sejumlah fungsi bawaan untuk memanipulasi string, seperti `strlen()` untuk menghitung
panjang string, `strtolower()` untuk mengubah semua karakter dalam string menjadi huruf kecil, `strtoupper()` untuk 
mengubah semua karakter dalam string menjadi huruf besar, dan masih banyak lagi.

## 4. Boolean

Tipe data Boolean pada PHP hanya memiliki dua nilai yaitu `true` (benar) dan `false` (salah). Nilai `true` memiliki nilai 
numerik **1**, sedangkan `false` memiliki nilai numerik **0**.

Contoh penggunaan:

```php
$benar = true;
$salah = false;

if ($benar) {
  echo "Nilai variabel benar adalah true.";
}

if (!$salah) {
  echo "Nilai variabel salah adalah false.";
}
```
> Kode diatas menggunakan **if statement** ([5. Percabangan dalam PHP]()) dan **operator negasi** ([4. Operator dalam PHP]()).

Output:
```shell
Nilai variabel benar adalah true.
Nilai variabel salah adalah false.
```
Pada contoh di atas, variabel `$benar` memiliki nilai true, sehingga kondisi di dalam [if statement]() akan dieksekusi dan 
menghasilkan output "**Nilai variabel benar adalah true**.". Sementara itu, variabel `$salah` memiliki nilai false, tetapi 
karena menggunakan [operator negasi]() (`!`), kondisi di dalam [if statement]() menjadi true dan menghasilkan output 
"**Nilai variabel salah adalah false**.".

## 5. Array
Array pada PHP adalah sebuah tipe data yang digunakan untuk menyimpan sekumpulan nilai atau variabel dalam satu 
variabel. Array pada PHP memiliki beberapa tipe, yaitu:

- **Indexed Array**

Indexed array adalah tipe array yang menggunakan indeks numerik berupa angka sebagai penunjuk setiap elemen array. 
Indeks dimulai dari `0` dan seterusnya sesuai dengan jumlah elemen dalam array. Contoh:

```php
$nama = array("Andi", "Budi", "Cindy");
echo $nama[0]; // output: Andi
```
- **Associative Array**

Associative array adalah tipe array yang menggunakan kunci atau nama sebagai penunjuk setiap elemen array, 
tidak menggunakan indeks numerik. Contoh:

```php
$person = array("nama" => "Andi", "umur" => 20, "alamat" => "Jakarta");
echo $person["nama"]; // output: Andi
```
- **Multidimensional Array**

Multidimensional array adalah tipe array yang memiliki lebih dari satu dimensi atau lebih dari satu array di dalam 
array. Contoh:
```php
$nilai = array(
    array(80, 90, 70),
    array(75, 85, 95),
    array(60, 70, 80)
);
echo $nilai[1][2]; // output: 95
```
Dalam penggunaannya, array pada PHP sangat fleksibel dan dapat digunakan untuk berbagai keperluan seperti menyimpan
data dari database, menyimpan data sementara dalam program, dan sebagainya.

Di PHP, kita bisa membuat array menggunakan dua cara, yaitu dengan menggunakan `array()` atau `[]`. Kedua cara tersebut
memiliki hasil yang sama, yaitu membuat array.

- Contoh pembuatan array menggunakan `array()`:
```php
$angka = array(1, 2, 3, 4, 5);
$nama = array('Andi', 'Budi', 'Cindy');
```

- Contoh pembuatan array menggunakan `[]`:

```php
$angka = [1, 2, 3, 4, 5];
$nama = ['Andi', 'Budi', 'Cindy'];
```

Perlu diingat bahwa cara pembuatan array menggunakan `[]` baru tersedia pada PHP versi **5.4** ke atas. Sehingga, jika 
menggunakan PHP versi sebelumnya, harus menggunakan cara pembuatan array dengan `array()`.