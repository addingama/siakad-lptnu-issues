# Pre-Migration

## Issue 1

Kode matakuliah di UNU NTB terdiri dari 15 karakter.

Perubahan panjang field kodemk satu-persatu dari pgadmin sangat memakan waktu dan tidak bisa dilakukan karena batasan dari PostgreSql yang tidak boleh merubah kolom yang berhubungan. 

Solusi:

- Export seluruh schema dari database menggunakan bantuan `Navicat Premium`
- Buatlah backup terlebih dahulu dari file yang telah di export
- Buka file hasil export
- Find `kodemk` dan ubah panjang field sesuai kebutuhan
- Hapus seluruh skema yang ada
- Import ulang file yang telah di modifikasi


## Isue 2

Terdapat kesalahan data NIM Mahasiswa. Ada kasus dimana nim yang sama digunakan pada beberapa Program Studi.

Cara mendeteksi duplikasi

- Gabungkan semua data mahasiswa seluruh angkatan ke dalam 1 buah file `.xlsx` dan buka di dalam `Google SpreadSheet` secara online. Pastikan informasi NIM dan Program Studi termasuk dalam file tersebut
- Tambahkan pivot tabel melalui menu Data -> Pivot Table -> New Sheet -> OK
- Tambahkan 2 row, row pertama adalah kolom Nim dan row kedua adalah kolom Program Studi. Hilangkan semua ceklis pada pengaturan row di sebelah kanan
- Periksa pivot tabel tersebut untuk mengetahui apakah ada nim yang duplikat. Ciri-cirinya adalah adanya bari kosong di kolom NIM.
- Setelah menemukan kesalahan tersebut, lakukan perbaikan NIM pada excel tersebut.
- Lakukan penyesuaian NIM pada file KHS hasil export dari PDDIKTIK untuk NIM yang bermasalah.
