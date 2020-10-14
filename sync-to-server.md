# Auto Sync changed file to server

[rsync usage article](https://www.tecmint.com/sync-new-changed-modified-files-rsync-linux/)

## Persiapan

- Install `rsync` pada local machine

## Tahap 1

Proses ini cukup dilakukan satu kali saja

- Clone code siakad ke local machine menggunakan perintah berikut

  ```
    rsync -a -e 'ssh -p <port ssh server>' --progress usernamessh@domainuniv:/home/usernamessh/ /full/path/ke/local/directory
  ```
  
- 
  
## Tahap 2

- Lakukan perubahan di local
- Buat sebuah file dengan nama `upload_to_server.sh` pada root project dan masukkan perintah berikut `rsync -a --exclude '.idea' --exclude 'siakad/siakad/uploads' --recursive --update -e 'ssh -p <port ssh server>' --progress . usernamessh@domainuniv:/home/usernamessh/`
- Open terminal dan tambahkan permission to execute untuk file tersebut, `chmod +x upload_to_server.sh`
- Jalankan perintah `./upload_to_server.sh` melalui terminal untuk melakukan proses upload. Anda harus melakukan input password SSH jika command mulai dieksekusi

Catatan:

Pada contoh di atas, kami mengabaikan folder dari IDE dan foto mahasiswa pada saat melakukan sync ke server.

