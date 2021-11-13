# 11 - Docker2

## Tujuan Pembelajaran

1. Mengetahui cara membuat dan memeriksa docker network.
2. Mengetahui cara menghubungkan container ke network.
3. Mengetahui cara membuka port container.
4. Mengetahui cara membuat volume.
5. Mengetahui cara menghapus volume.
6. Mengetahui tentang docker compose.

## Hasil Praktikum

#
## 1. Docker Network
### 1.1	Membuat dan Memeriksa Docker Network 

#

1. Pertama ketik perintah di bawah ini untuk mengetahui network yang tersedia pada docker host kita.<br><br>
![Screenshot](img/langkah1.png)<br>

2. Selanjutnya untuk mengetahui perintah-perintah dasar yang bisa digunakan untuk docker network.<br><br>
![Screenshot](img/langkah2.png)<br>

3. Untuk membuat network bisa menggunakan perintah create seperti pada gambar di bawah ini.<br><br>
![Screenshot](img/langkah3.png)<br>

4. Selanjutnya cek network yang sudah dibuat menggunkan perintah ls, seharusnya akan menambahkan network. Hasilnya adalah sebagai berikut.<br><br>
![Screenshot](img/langkah4.png)<br>

5. Terakhir, ketika ingin mengetahui informasi detail dari network yang telah kita buat bisa menggunakan perintah inspect.<br><br>
![Screenshot](img/langkah5.png)<br>

<b>Noted:</b> Network yang telah kita buat ini selanjutnya bisa kita gunakan untuk menghubungkan container satu dengan yang lain.

# 

### 1.2	Menghubungkan Container ke Network

#

1. Buat terlebih dahulu contoh container, misalkan kita akan membuat container linux yaitu busybox.<br><br>
![Screenshot](img/langkah6.png)<br>

2. Buat container yang kedua menggunakan image linux alphine, buka windows yang baru agar container1 tetap berjalan.<br><br>
![Screenshot](img/langkah7.png)<br>

<b>Noted:</b> Jangan lupa mengubah nama container dari yang sebelumnya.

3. Kemudian cek masing-masing container tersebut menggunakan perintah ps untuk mengetahui status container yang sedang jalan. Buka windows baru, jalankan perintah berikut.<br><br>
![Screenshot](img/langkah8.png)<br>

4. Kemudian jalankan inspect untuk mengetahui informasi detail dari masing-masing container.<br><br>
Container 1
![Screenshot](img/langkah9a.png)<br>
![Screenshot](img/langkah9b.png)<br>
<br><br>

Container 2
![Screenshot](img/langkah10a.png)<br>
![Screenshot](img/langkah10b.png)<br>
<br>

5. ntuk membuktikan silakan ping dari container1 ke container2, seharusnya akan reply.<br><br>
![Screenshot](img/langkah11.png)<br>


# 

### 1.3	Membuka Port Container

#

1. isalkan kita ingin membuat image dari apache, layanan httpd. Bisa dilakukan dengan perintah di bawah ini.<br><br>
![Screenshot](img/langkah12.png)<br>

2. Silakan cek menggunakan telnet terhadap port yang di-expose atau dengan mengetik pada browser seperti ditunjukkan di bawah ini.<br><br>
![Screenshot](img/langkah13.png)<br>

3. Kemudian untuk mengetahui port yang dilakukan expose pada container, bisa menggunakan perintah di bawah ini.<br><br>
![Screenshot](img/langkah14.png)<br>

<b>Noted:</b> Setelah mengetahui cara untuk melakukan expose dan mapping port, dapat diterapkan ketika Anda membuat container dan container tersebut bisa menerima request dari luar.

#
## 2. Docker Volume
### 2.1. Membuat Volume

#


1. Buat terlebih dahulu folder di host(laptop/computer/vps), misalkan buat folder docker-shared.<br><br>
![Screenshot](img/langkah16.png)<br>

2. Cek di folder local Anda, bisa menggunakan perintah ls atau dir. Dapat juga dilihat menggunakan windows explorer.<br><br>
![Screenshot](img/langkah18.png)<br>
![Screenshot](img/langkah17.png)<br><br>

<b>Noted:</b> etelah kita melakukan mapping volume dari container ke local direktori, kemudian kita akan membuat volume pada docker.<br>

1. Perintah pertama yang bisa dijalankan adalah sebagai berikut, mengecek volume yang telah ada sebelumnya.<br><br>
![Screenshot](img/langkah19.png)<br> 
Disini terlihat masih kosong karena belum ada volume yang terbuat sebelumnya.

2. ntuk membuat volume baru, bisa menggunakanperintah di bawah ini.<br><br>
![Screenshot](img/langkah20.png)<br> 

3. Disini terlihat bahwa volume yang baru kita buat berhasil tersimpan.<br><br>
![Screenshot](img/langkah21.png)<br> 

4. Jalankan container dengan menyertakan volume yang telah kita sebelumnya dan buat file log.txt, jangan lupa masuk ke direktori volume terlebih dahlulu.<br><br>
![Screenshot](img/langkah22.png)<br> 

5. uat container yang lain, dengan mengulangi langkah yang sama sebelumnya. Ketik perintah ls untuk mengetahui isi folder volume.<br><br>
![Screenshot](img/langkah23.png)<br> 

#

### 2.1. Membuat Volume

#

1. Untuk menghapus volume yang telah kita buat sebelumnya dapat dilakukan dengan cara di bawah ini.<br><br>
![Screenshot](img/langkah24.png)<br> 

<b>Noted:</b> Sebelum menghapus volume, pastikan terlebih dahulu volume tersebut tidak digunakan pada container.

#
## 3. Docker Compose

#

1. Silakan masuk ke oracle cloud dan ke VM Anda, kemudian install docker compose dengan perintah sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose.<br><br>
![Screenshot](img/langkah25.png)<br> 

2. Ubah docker compose menjadi executable menggunakan command berikut.<br><br>
![Screenshot](img/langkah26.png)<br>

3. Cek versi docker compose untuk memastikan proses installasi berhasil dilakukan dengan perintah.<br><br>
![Screenshot](img/langkah27.png)<br>

4. Clone repo yang telah disediakan menggunakan git atau download secara manual.<br><br>
![Screenshot](img/langkah28.png)<br>

5. Masuk ke direktori tersebut dan ganti branch menjadi cloud-docker dengan perintah seperti berikut ini.<br><br>
![Screenshot](img/langkah29.png)<br>

6. Build image tersebut menggunakan perintah build pada docker.<br><br>
![Screenshot](img/langkah30.png)<br>

7. Selanjutnya buat folder data di bawah /opt agar data mysql tidak hilang ketika container dihapus.<br><br>
![Screenshot](img/langkah31.png)<br>

8. Jalankan docker compose menggunakan perintah berikut ini.<br><br>
![Screenshot](img/langkah32.png)<br>