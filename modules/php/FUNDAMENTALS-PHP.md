# Fundamentals of PHP
PHP (Hypertext Preprocessor) adalah bahasa pemrograman server-side yang paling umum digunakan untuk membangun situs web dan aplikasi web dinamis. PHP pertama kali dirilis pada tahun 1995 dan saat ini merupakan salah satu bahasa pemrograman paling populer di dunia.

PHP adalah bahasa pemrograman server-side yang kuat dan serbaguna. Dengan kemampuan untuk memproses formulir, mengelola database, dan berintegrasi dengan mudah dengan server web dan database, PHP menjadi bahasa pemrograman pilihan untuk banyak pengembang web. Selain itu, kemampuan untuk membuat fungsi dan kelas sendiri membuat PHP lebih mudah dikembangkan untuk aplikasi yang lebih kompleks.

## Contents
- [Tipe Data](#tipe-data) : Berbagai tipe data yang terdapat di bahasa pemrograman PHP.
    - [NULL](#1.-null)

## Tipe Data
### **1. NULL**
Membuat variable yang berisi `NULL`
```php
$name = NULL;
```
Mengecek jika variable `NULL`, gunakan function `is_null($<variable>)`
```php
echo (is_null($name));
```
#### **Menghapus variabel**
Selain mengubah menjadi `NULLL`, di PHP juga bisa menghapus sebuah variable, caranya dengan menggunakan function `unset($<variable>)`
```php
unset($name);

// Akan error karena variable `$name` sudah dihapus.
echo $name;
```
Untuk mengecek apakah variable ada atau tidak bisa menggunakan function `isset($<variable>)`.
```php
if (isset($name)) {
    echo $name;
}
```
> Mengecek variable `name` ada atau tidak.

## **Tipe Data: Array**
Array adalah tipe data yang berisikan kosong atau banyak data. Array di PHP bisa berisikan data dengan jenis tipe data berbeda-beda dan memiliki panjang dinamis, artinya kita bisa menambah data ke Array sebanyak-banyaknya, tidak dibatasi kapasitasnya.

Membuat variable yang berisi Array
```php
$my_array = array(1, 2, 3, 4);
// Atau
$my_array = ["Joni", "Kiko", "Santoso"];
```
Jika ingin membuat Array yang kosong
```php
$my_array = []
```
### **Operasi Array**
| Operasi                 | Keterangan                                                 |
|-------------------------|------------------------------------------------------------|
| `$array[index]`         | Mengakses data di array pada nomor index.                  |
| `$array[index] = value` | Mengubah data di array pada nomor index dengan value baru. |
| `$array[] = value`      | Menambah data di array pada posisi paling belakang.        |
| `unset($array[index])`  | Menghapus data di array, index otomatis hilang dari array. |
| `count($array)`         | Mengambil total data di array.                             |

### **Array Sebagai Map**
Secara default Array akan menggunakan index (number) sebagai key dan value nya kita bebas memasukan data ke dalam Array. Namun jika kita ingin, kita juga bisa mengubah index nya tidak harus menggunakan number, bisa gunakan tipe data lain, seperti `string` misal-nya.

Membuat Array Map
```php
$person_data = array(
    "nama" => "Kurniawan",
    "umur" => 30,
    "alamat" => "Jakarta"
);
```
> Jika ingin mengambil data array map bisa menggunakan operasi array `$person_data[<key>]`. Contoh semisal `$person_data["nama"]` untuk mengambil value `nama`.

### **Array di dalam Array**
Array di PHP bisa berisikan data apapun, sehingga kita juga bisa membuat array di dalam array jika memang dibutuhkan.

Membuat Array di dalam Array
```php
$person_data = array(
    "nama" => "Kurniawan",
    "umur" => 30,
    "alamat" => [
        "city" => "Jakarta",
        "country" => "Indonesia"
    ]
);
```
> Contoh semisal `$person_data["address"]["country"]` untuk mengambil value `country` yang tersimpan di dalam key `alamat`.
## **Operator: Aritmatika**

| Operasi                  | Keterangan  |
|--------------------------|-------------|
| `+$variable`             | Positif     |
| `-$variable`             | Negatif     |
| `$variable + $variable`  | Penambahan  |
| `$variable - $variable`  | Pengurangan |
| `$variable * $variable`  | Perkalian   |
| `$variable / $variable`  | Pembagian   |
| `$variable % $variable`  | Sisa bagi   |
| `$variable ** $variable` | Pangkat     |

Menggunakan operator Aritmatika
```php
$result = 10 + 10;
var_dump($result);

$result = 100 % 3;
var_dump($result);

// Merubah hasil $result menjadi positif
$numPositive = +$result;
var_dump($result);

// Merubah hasil $result menjadi negatif
$numNegative = -$result;
var_dump($result);
```
## **Operator: Penugasan**
Operator penugasan di PHP sama seperti bahas pemrograman lain, yaitu dengan menggunakan karakter `=` (sama dengan). 

Operator penugasan sudah sering kita gunakan, terutama jika mengubah value sebua variable. 

Namun selain hal itu, operasi penugasan juga bisa digunakan untuk operasi aritmatika.

| Penugasan  | Keterangan  |
|------------|-------------|
| `$a += $b` | $a = $a + b |
| `$a -= $b` | $a = $a - b |
| `$a *= $b` | $a = $a * b |
| `$a /= $b` | $a = $a / b |
| `$a %= $b` | $a = $a % b |

Menggunakan operator penugasan
```php
$price = 0;

$fruit = 500;
$drink = 800;

// Menggunakan operator penugasan untuk menambah nilai `$price`
$price += $fruit;
$price += $drink;

var_dump($price);
```
> Jumlah `price` sekarang adalah 1300.

## **Operator: Perbandingan**
Operator perbandingan, seperti namanya, digunakan untuk membandingkan duat buah value

Hasil dari operator perbandingan adalah `boolean`, **true** jika perbandinganya benar, **false** jika perbandingannya salah.

| Operator    | Nama                         | Keterangan                                                             |
|-------------|------------------------------|------------------------------------------------------------------------|
| `$a == $b`  | Sama dengan                  | true jika $a sama dengan $b setelah dilakukan konversi tipe data       |
| `$a === $b` | Identik                      | true jika $a sama dengan $b dan memiliki tipe data yang sama           |
| `$a != $b`  | Tidak sama dengan            | true jika $a tidak sama dengan $b setelah dilakukan konversi tipe data |
| `$a <> $b`  | Tidak sama dengan            | true jika $a tidak sama dengan $b setelah dilakukan konversi tipe data |
| `$a !== $b` | Tidak identik                | true jika $a tidak sama dengan $b atau tidak sama tipe data            |
| `$a < $b`   | Kurang dari                  | true jika $a kurang dari $b                                            |
| `$a <= $b`  | Kurang daru atau sama dengan | true jika $a kurang dari atau sama dengan $b                           |
| `$a > $b`   | Lebih dari                   | true jika $a lebih dari $b                                             |
| `$a >= $b`  | Lebih dari sama dengan       | true jika $a lebih daru atau sama dengan $b                            |

Menggunakan operator perbandingan
```php
// true (karena type juggling)
var_dump("10" == 10);

// false (karena menggunakan operator identik)
var_dump("10" === 10);
```
## **Operator: Logika**
Operator logika bertugas untuk membandingkan `boolean`

| Operator         | Nama | Keterangan                                        |
|------------------|------|---------------------------------------------------|
| `$a **&&** $b`   | And  | true jika $a dan $b keduanya true                 |
| `$a **and** $b`  | And  | true jika $a dan $b keduanya true                 |
| `$a **\|\|** $b` | Or   | true jika $a dan $b salah satu atau keduanya true |
| `$a **or** $b`   | Or   | true jika $a dan $b salah satu atau keduanya true |
| `**!**$a`        | Not  | true jika $a bernilai false                       |
| `$a **xor** $b`  | Xor  | true jika $a salah satu true, tapi tidak keduanya |

```php
var_dump(true && true);     # true
var_dump(true and false);   # false
var_dump(true || false);    # true
var_dump(true or false);    # true
var_dump(!true);            # false
var_dump(true xor false);   # true
```
## **Increment & Decrement**
PHP mendukung gaya bahasa pemrograman C untuk menaikan dan menurunkan data number sejumlah 1 angka. Ini bisa mempersingkat kita ketika ingin menaikan data.

| Contoh | Nama           | Efek                                       |                    
|--------|----------------|--------------------------------------------|                    
| `$a++` | Post increment | Kembalikan $a lalu naikan 1 angka          |                    
| `++$a` | Pre increment  | Naikan $a satu angka, lalu kembalikan $a   |                    
| `$a--` | Post decrement | Kembalikan $a lalu turunkan 1 angka        |                    
| `--$a` | Pre decrement  | Turunkan $a satu angka, lalu kembalikan $a |                               

Contoh menggunakan **POST Increment**.
```php
$point = 10;

var_dump($point++);
var_dump($point++);
var_dump($point++);

var_dump($point);
```
> Output nilai `$point` berturut-turut pada program diatas adalah **10**, **11**, **12**, **13**. Karena pada POST increment akan mengembalikan nilai variable-nya terlebih dahulu baru ditambahkan. Berlaku juga pada decrement.

Contoh menggunakan **PRE Increment**.
```php
$point = 10;

var_dump(++$point);
var_dump(++$point);
var_dump(++$point);

var_dump($point);
```
> Output nilai `$point` berturut-turut pada program diatas adalah **11**, **12**, **13**, **14**. Karena pada PRE increment akan ditambahkan terlebih dahulu baru mengembalikan nilai variable-nya. Berlaku juga pada decrement.

## **Operator: Array**
Pada PHP, Array memiliki operator khusus. Mungkin terlihat mirip dengan operator-operator sebelumnya, tapi cara kerjanya sedikit berbeda.

Berikut adalah daftar operator array yang dapat digunakan dalam PHP.

| Operator | Deskripsi |
|----------|-----------|
| `+`      | Menggabungkan dua array (Union) |
| `==`     | Memeriksa kesamaan nilai dari dua array (Equality) |
| `===`    | Memeriksa kesamaan nilai dan tipe data dari dua array (Identity) |
| `!=`     | Memeriksa ketidaksamaan nilai dari dua array (Inequality) |
| `<>`     | Memeriksa ketidaksamaan nilai dari dua array (Inequality) |
| `!==`    | Memeriksa ketidaksamaan nilai atau tipe data dari dua array (Non-identity) |
| `[]`     | Menambahkan elemen ke akhir array (Push) |

Menggunakan operator array **Union**.
```php
$person = ["username" => "John"];
$attribute = ["address" => "New York"];

var_dump($person + $attribute);
```
Output
```bash
array(2) {
  ["username"]=>
  string(4) "John"
  ["address"]=>
  string(8) "New York"
}
```
## **Expression, Statement dan Block**

### **Expression**
Expression adalah bagian terpenting di PHP. Hampir semua kode yang kita tulis adalah sebuah expression.

Secara sederhana, expression adalah apapun yang memiliki nilai atau value.

Contoh Expression Sederhana
```php
$point = 5;
```
> `$point = 5;` Ketika kita menuliskan **5**, maka tentu itu adalah nilai, oleh karena itu **5** tersebut adalah expression.

Contoh Expression Complex
```php
function getPoint() {
    return 100;
}

$newPoint = getPoint();
```
> Pada kode diatas, `getPoint()` adalah expression, karena `getPoint()` bernilai angka **100**.

### **Statement**
Statement bisa dibilang adalah kalimat lengkap dalam bahasa. Sebuah statement berisikan execution komplit, biasanya diakhiri dengan titik koma.

Contoh Statement
```php
$name = "John";

echo $name;
```
> Pada sebuah statement biasanya juga mengandung expression. Jadi bisa dibilang expression adalah bagian dari statement.

### **Block**
Block adalah kumpulan statement yang terdiri dari nol atau lebih statement. Biasanya diawali dan diakhiri dengan kurung kurawal `{}`.

Contoh Block
```php
function runApplication($name) {
    echo "Starting..." . PHP_EOL;
    echo "Welcome, $name" . PHP_EOL;
}
```
