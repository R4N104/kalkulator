# kalkulator

s
NAMA    : ALIYAH ASMARANI


## DAFTAR ISI <br>
| No | Description | Link |
|-----|------|-----|
|1|Perintah|[Click Here](#PERINTAH)|
|2|Input|[Click Here](#INPUT)|
|3|Output|[Click Here](#OUTPUT)|


# PERINTAH
> Buatlah sebuah program kalkulator sederhana, dengan aturan sbb:
> 
> Kalkulator dapat melakukan penjumlahan, pengurangan, dan perkalian dan pembagian
> 
> Penjumlahan, pengurangan dan perkalian dan pembagian dijadikan method yang berbeda masing-masingnya, contoh: function pembagian(){…}, function pengurangan(){…}, dst
> 
>Berikan komentar di dalam kode

# INPUT 
```
<?php

// Fungsi penjumlahan
function jumlah ($bilangan1, $bilangan2){
    return $bilangan1 + $bilangan2;
}

// Fungsi pengurangan
function pengurangan ($bilangan1, $bilangan2){
    return $bilangan1 - $bilangan2;
}

 // Fungsi perkalian
 function perkalian ($bilangan1, $bilangan2){
    return $bilangan1 * $bilangan2;
}

 // Fungsi pembagian
 function pembagian ($bilangan1, $bilangan2){
    return $bilangan1 / $bilangan2;
}

if(isset($_POST['submit'])) {
    $bilangan1 = $_POST['bilangan1'];
    $bilangan2 = $_POST['bilangan2'];
    $jumlah = jumlah($bilangan1, $bilangan2);
    $kurang = pengurangan($bilangan1, $bilangan2);
    $kali = perkalian($bilangan1, $bilangan2);
    $bagi = pembagian($bilangan1, $bilangan2);

}

?>
```
> Fungsi jumlah digunakan untuk menjumlahkan dua bilangan.
> 
> Fungsi pengurangan digunakan untuk mengurangkan satu bilangan dari bilangan lainnya.
> 
> Fungsi perkalian digunakan untuk mengalikan dua bilangan.
> 
> Fungsi pembagian digunakan untuk membagi satu bilangan dengan bilangan lainnya.
```
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Bootstrap demo</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-9ndCyUaIbzAi2FUVXJi0CjmCapSmO7SnpJef0486qhLnuZ2cdeRhO02iuK6FUUVM" crossorigin="anonymous">
  </head>
  <body>
    <div class='text-center py-5'>
    <img src="kalkulator.png" alt="kalkulator" width='200px'>
</div>
    <h1 class= "text-center py-5">Aplikasi Kalkulator</h1>

    <div class="container px-5">
        <form method="POST">
            <div class="mb-3">
                <label for="bilangan1" class="form-label">Bilangan 1</label>
                <input type="number" class="form-control" id="bilangan1" name="bilangan1">
            </div>
            <div class="mb-3">
                <label for="bilangan2" class="form-label">Bilangan 2</label>
                <input type="number" class="form-control" id="bilangan2" name="bilangan2">
            </div>
            <input type="submit" class="btn btn-primary" value="Hitung" name="submit" style="width: 100%"><br><br>
        </form>
        <div>
            <?php
            if(isset($_POST['submit'])){
                echo "<h2>Hasil Perhitungan : </h2>";
                echo "<p>Bilangan 1 : $bilangan1</p>";
                echo "<p>Bilangan 2 : $bilangan2</p>";
                echo "<p>Hasil penjumlahan adalah : $jumlah</p>";
                echo "<p>Hasil pengurangan adalah : $kurang</p>";
                echo "<p>Hasil perkalian adalah : $kali</p>";
                if(is_nan($bagi)){
                    echo "<p>Error: Pembagian dengan nol tidak valid</p>";
                }else{
                    echo "<p>Hasil pembagian adalah : $bagi</p>";
                }
            }
            ?>
        </div>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js" integrity="sha384-geWF76RCwLtnZ8qwWowPQNguL3RmwHVBC9FhGdlKrxdiJJigb/j/68SIy3Te4Bkz" crossorigin="anonymous"></script>
  </body>
</html>
```
> Ketika halaman dimuat, gambar "kalkulator.png" akan ditampilkan di bagian atas halaman.
> 
> Judul "Aplikasi Kalkulator" ditampilkan di tengah halaman.
> 
> Terdapat sebuah formulir yang meminta pengguna memasukkan dua bilangan.
> 
> Ketika pengguna menekan tombol "Hitung" yang terdapat dalam formulir, kodingan PHP dijalankan.
> 
> Jika tombol "Hitung" ditekan, maka dilakukan perhitungan menggunakan fungsi-fungsi matematika dasar yang telah didefinisikan sebelumnya (jumlah, pengurangan, perkalian, dan pembagian).
> 
> Hasil perhitungan ditampilkan di bawah formulir.
> 
> Jika pembagian dilakukan dengan pembagi nol, maka akan ditampilkan pesan "Error: Pembagian dengan nol tidak valid".

# OUTPUT

### tampilan awal
![image](https://github.com/R4N104/kalkulator/assets/138820515/1bffe433-ee31-4136-91b1-956897bd8bda)

### hasil ketika sudah memasukkan angka
![image](https://github.com/R4N104/kalkulator/assets/138820515/fc9ed390-28c0-4ca6-9074-b121a6c98c19)

