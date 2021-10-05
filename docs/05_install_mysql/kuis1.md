# 05 - PAAS -> KUIS1 - SETUP WORDPRESS VM + DB


## Hasil Praktikum

1. Setelah semua proses instalasi diatas selesai, sekarang kita coba untuk menginstal Wordpress pada PaaS. Dimana langkah pertama yang kita lakukan ialah membuat database baru, berikut untuk perintah yang harus dijalankan.<br><br>
![Screenshot Langkah17](img/langkah18.png) <br><br>

2. Baru kemudian kita download Wordpress Pada Folder /var/www/html dengan perintah berikut.<br><br>
![Screenshot Langkah18](img/langkah19.png) <br><br>

3. Jangan lupa setelah itu kita ekstrak Wordpress yang ada pada folder /var/www/html dengan perintah <b>tar zxvf latest.tar.gz</b>, maka proses yang berjalan akan seperti berikut.<br><br>
![Screenshot Langkah19](img/langkah20.png) <br><br>

4. Selanjutnya, jika proses estrak file hasil download berhasil, kita bisa menghapus file hasil download dengan menggunakan perintah berikut.<br><br>
![Screenshot Langkah20](img/langkah21.png) <br><br>

5. Selanjutnya, kita akan menginstall extension mysql pada php dan mengaktifkannya pada <b>php.ini</b>. Berikut adalah perintah untuk menginstall extenstion mysql pada php. <br><br>
![Screenshot Langkah21](img/langkah22.png) <br><br>

6. Kemudian, kita coba akses file php.ini dan kita lakukan modifikasi seperti yang ada di dalam modul, yang mana fungsinya untuk mengaktifkan extension mysql pada php.<br><br>
![Screenshot Langkah22](img/langkah28.png) <br><br>
![Screenshot Langkah22](img/langkah27.png) <br><br>

7. Setelah semua proses diatas berhasil dilakukan, sekarang kita coba lakukan restart apache sekaligus setting ownership dan permissions dengan menggunakan perintah berikut.<br><br>
![Screenshot Langkah23](img/langkah29.png) <br><br>

8. Setelah semua proses diatas berhasil dilakukan, sekarang kita coba lakukan restart apache sekaligus setting ownership dan permissions dengan menggunakan perintah berikut.<br><br>
![Screenshot Langkah23](img/langkah29.png) <br><br>

9. Selanjutnya, kita akan melakukan proses Intalasi Wordpress melalui browser(http://168.138.51.31/wordpress). Berikut untuk step - stepnya.
#
1. Kita harus memilih terlebih dahulu bahasa untuk digunakan di dalam Dashboard Wordpress. <br><br>
![Screenshot Langkah24](img/langkah30.png) <br><br>
2. Kemudian, kita coba melakukan pengisian data untuk membuat table. <br><br>
![Screenshot Langkah25](img/langkah31.png) <br><br>
3. Setelah itu klik next, maka Wordpress siap diinstall. <br><br>
![Screenshot Langkah26](img/langkah32.png) <br><br>
4. Kita lanjutkan dengan pengisian data Judul Site, Password dan Email.<br><br>
![Screenshot Langkah27](img/langkah33.png) <br><br>
![Screenshot Langkah28](img/langkah34.png) <br><br>
5. Berikut untuk tampilan Wordpress yang berhasil tersinstall.<br><br>
![Screenshot Langkah29](img/hasil.png) <br><br>


#

