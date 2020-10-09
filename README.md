# Sistem Informasi Manajemen

Repositori ini berisi catatan tahapan untuk proses implementasi Siakad dari LPTNU yang telah dilakukan di Universitas Nahdlatul Ulama NTB.


## Requirements

- Membayar iuran VPS selama 1 tahun

## Pre-Migration

- Periksa jumlah karakter untuk kode matakuliah di universitas anda. Untuk Siakad, panjang default kode matakuliah adalah `10 karakter`.
- Pastikan tidak ada data mahasiswa yang memiliki nim sama di lintas prodi. Kemungkinan terjadi karena salah ketik pada saat memasukkan data ke PDDIKTI. Jika ada yang salah, silahkan perbaiki terlebih dahulu data di excel nya dan perbaiki nim mahasiswa di excel hasil export krs.


## Migrasi Data

1. Input Data Unit
2. Import Data Mahasiswa
3. Import Data Matakuliah
4. Import Data Kelas
5. Import Data KHS
6. Input Jenis Tagihan di Keuangan Akademik
7. Input Tarif Tagihan Rutin
8. Input Tarif Form
9. Input Tarif Wisuda
