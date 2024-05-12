## Mata Kuliah

Sebagai tugas praktikum: [1] Basis Data | Universitas Pelita Bangsa.

## Laporan Praktikum

- Bagian 1:

  > Disini saya menggunakan Shell dari XAMPP sebagai contoh.

  <p align="left">
    <img src="/ss/1.jpg" width="500">
  </p>

      # MySQL akan menanyakan password bahkan jika itu kosong (tekan enter saja)
      mysql -h localhost -u root -p

perintah diatas berarti **MySQL host:127.0.0.1 user:root pass:kosong**.

- Bagian 2:

  > Ingat. Database dan Tabel berbeda, Database itu inang sedangkan Tabel berada didalam Database.

  <p align="left">
    <img src="/ss/2.jpg" width="330">
  </p>

      # Membuat Database
      create database Walfu1;

**create database [yourdb]** merupakan perintah untuk membuat database.

- Bagian 3:

  > Dalam sebuah Database kita dapat merubah Tabel atau Database itu sendiri.

  <p align="left">
    <img src="/ss/3.jpg" width="400">
  </p>

      # Masuk ke dalam Database
      use Walfu1

**use** digunakan untuk memasuki sebuah Database yang ingin dirubah.

- Bagian 4:

  > Membuat Tabel dalam Database.

  <p align="left">
    <img src="/ss/4.jpg" width="400">
  </p>

      # Membuat Tabel dan Tipe-nya
      CREATE TABLE biodata (
        Nama VARCHAR(30),
        Alamat VARCHAR(30),
        Keterangan VARCHAR(15)
      );

**CREATE TABLE** digunakan untuk membuat Tabel, sedangkan **VARCHAR(15)** merupakan variable character atau karakter ber-tipe variabel berjumlah 15.

- Bagian 5:

  > Menambah, Merubah, Mendefinisikan sebuah Tabel.

  <p align="left">
    <img src="/ss/5.jpg" width="400">
  </p>

      # Menambah Tabel di Kolom Pertama dan setelah Kolom tertentu
      ALTER TABLE biodata ADD COLUMN id INT(11) FIRST;
      ALTER TABLE biodata ADD COLUMN Email VARCHAR(20) AFTER HP;
      ALTER TABLE biodata ADD COLUMN Phone VARCHAR(15) AFTER Alamat;

      # Merubah Nama dan Tipe dari sebuah Kolom
      ALTER TABLE biodata CHANGE Phone HP VARCHAR(20);

      # Merubah Tipe dari sebuah Kolom
      ALTER TABLE biodata MODIFY id CHAR(11);

**ALTER TABLE** digunakan untuk merubah sebuah Tabel atau Kolom. **ADD COLUMN** digunakan untuk menambahkan sebuah Kolom. **CHANGE** digunakan untuk merubah Nama dan Tipe dari sebuah Kolom, sedangkan **MODIFY** hanya berlaku untuk Tipe-nya saja.

- Bagian 6:

  > Merubah Tabel dan Menghapus Kolom.

  <p align="left">
    <img src="/ss/6.jpg" width="400">
  </p>

      # Merubah Tabel
      ALTER TABLE biodata RENAME data_mahasiswa;
      ALTER TABLE data_mahasiswa CHANGE id NIM VARCHAR(10);
      
      # Menghapus Kolom
      ALTER TABLE biodata DROP Keterangan;

**RENAME** digunakan untuk merubah nama dari sebuah Tabel. **DROP** digunakan untuk menghapus sebuah Kolom.

- Bagian 7:

  > Menambahkan Key pada sebuah Kolom.

  <p align="left">
    <img src="/ss/7.jpg" width="400">
  </p>

      # Menambahkan Primary Key pada sebuah Kolom
      ALTER TABLE data_mahasiswa ADD PRIMARY KEY (NIM);

      # Menambahkan Unique Key pada sebuah Kolom
      ALTER TABLE data_mahasiswa ADD UNIQUE KEY (Email);

**PRIMARY** digunakan untuk menambahkan Key dalam definisi Primary, sedangkan **UNIQUE** digunakan untuk menambahkan Key dalam kategori Unique.

- Bagian 8:

  > Hasil Akhir.

  <p align="left">
    <img src="/ss/8.jpg" width="400">
  </p>

      # Memperlihatkan Tabel dan Kolom pada Database
      show tables;
      desc data_mahasiswa;

**show** digunakan untuk memperlihatkan daftar Tabel pada Database. **desc** digunakan untuk memperlihatkan seluruh Kolom pada Tabel.

## Documentation

All associated resources. are licensed under the [MIT License](https://mit-license.org/).
