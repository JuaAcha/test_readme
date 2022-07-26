###### Nama : Ach Ilham M.A
###### Kelas : XII RPL 1
###### No. Absen : 03

# Modul 1

Soal NO.1
lakukan proses Instalasi framework laravel kedalam folder dengan nama masing-masing

Soal NO.2
Buatlah projek pertama laravel dengan nama projek “penjualan” dan tampilkan dalam browser

![image](https://user-images.githubusercontent.com/109930502/180912278-dbba15cc-fc7d-4620-b0d4-9e8e589a39c4.png)

```
composer create-project laravel/laravel penjualan
```


# Modul 2

## Soal NO.1
Buatlah migration tabel kategori dengan menggunakan teknik yang telah dipelajari dalam modul ini.

# Langkah 1

Buatlah tabel migration dengan mengetik source code seperti dibawah ini
```
php artisan make:migration create_kategori_table
```
# Langkah 2

ketik source code kedalam file Database->Migrations->create_kateori_table
![image](https://user-images.githubusercontent.com/109930502/180917420-f84a2ba6-b8a0-4e36-b9bb-039f2139696a.png)

Pastikan programnya berjalan dengan lancar tanpa ada error di dalamnya

untuk mengeRUN ketik
```
php artisan migrate
```

# Langkah 3
Membuat Model 
Model merupakan bagian dari konsep MVC pada Laravel yang fungsinya untuk berinteraksi 
dengan database. Model dibuat berdasarkan nama tabel pada aplikasi yang dibangun. Misalnya 
sebelumnya kita telah membuat satu tabel yang bernama barangs. Untuk membuat model untuk table 
barangs kita dapat menjalankan perintah artisan dengan sciprt sebagai berikut:
```
php artisan make:model kategori
```

untuk hasil dari pembuatan model kategori seperti ini

![image](https://user-images.githubusercontent.com/109930502/180918430-fa0a317e-1d2a-483f-8ad8-e282c6f75b1c.png)

nama file model disini adalah kategori maka nama tabel yang ada di dalam database adalah kategoris. Namun hal tersebut dapat 
dikonfigurasi dengan cara membuka file model barang.php yang baru saja dibuat dan tambahkan script 
berikut:

![image](https://user-images.githubusercontent.com/109930502/180918801-354fef2d-bdf2-44be-86d6-ce14cc7b7bbc.png)

Di dalam class model kategori kita mendefinsikan satu variabel bernama table, value dari variabel ini 
akan dianggap sebagai nama tabel yang diwakili oleh model ini.

## Soal NO.2

Kita menggunakan seeder yang telah kita pelejari pada modul ini

### langkah 1

Gunakan perintah artisan pada ***CMD*** sebagai berikut :

![image](https://user-images.githubusercontent.com/109930502/180920154-0026b29f-3220-4e6f-af89-a57b1ec32c86.png)

Gunakan source code ini untuk membuat file baru pada folder Seeder. Hasil diatas dapat kita lihat sebagai berikut

![image](https://user-images.githubusercontent.com/109930502/180920422-149277f0-7129-4dc0-8e67-9023f04005ae.png)

### Langkah 2

ketik source code kedalam file kategoriTableSeeder seperti ini

![image](https://user-images.githubusercontent.com/109930502/180920994-85823781-8662-40c2-a734-5253d06267bc.png)

### Langkah 3

Langkah berikutnya, buka file DatabaseSeeder.php yang ada pada folder database/seeds dan panggil seeder yang baru dibuat pada method run dengan menambahkan script sebagai berikut:

![image](https://user-images.githubusercontent.com/109930502/180921212-f0fd1bcc-3cf9-4285-ab76-b96c640e2802.png)

Sekarang kita bisa menjalankan perintah atisan pada comand prompt untuk mengeksekusi seeder yang 
telah dibaut dengan perintah sebagai berikut:
```
php artisan db:seed
```



