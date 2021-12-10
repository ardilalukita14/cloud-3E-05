# 14 - SERVERLESS

1. Mahasiswa bisa mengetahui apa itu serverless.
2. Mahasiswa dapat mendeploy aplikasi dari suatu function.

#
# Praktikum

#

## 1.	Hello World Function
Pada praktikum yang pertama akan dilakukan pengenalan terkait Serverless (Faas). Sebagai studi kasus, akan dideploy aplikasi hello world.


### 1.1.	Membuat Application dan Function

1. Masuk ke akun https://cloud.oracle.com dan navigasi ke menu Developer Services -> Applications.<br><br>
![Screenshot](img/langkah1.png)<br><br>

2. Tekan tombol Create Application dan lengkapi informasi form Name dengan hello-app. Lengkapi juga VCN dan subnet yang dibutuhkan. Jika anda belum mempunyai VCN, silahkan membuat terlebih dahulu VCN.
    <br><br>

    ![Screenshot](img/langkah2.png)<br>
    ![Screenshot](img/langkah3.png)<br>

3. Tekan tombol create dan tunggu sampai muncul halaman Getting Started.
    <br><br>

    ![Screenshot](img/langkah4.png)<br>

4. Pada halaman Getting Started terdapat contoh langkah-langkah deploy menggunakan perintah fn. Terdapat dua pilihan deploy, melalui Cloud Shell Setup atau Local Setup.<br><br>
![Screenshot](img/langkah5.png)<br>

5. Aktifkan Cloud Shell dengan menekan tombol Launch Cloud Shell. Tunggu proses provisioning cloud shell selesai. Anda akan mendapatkan sebuah terminal built-in yang dapat digunakan untuk melakukan proses deployment.<br><br>
![Screenshot](img/langkah6.png)<br>
![Screenshot](img/langkah7.png)<br>

6. Ikuti langkah-langkah dengan melakukan copy perintah kemudian tempelkan ke dalam terminal Cloud Shell.<br><br>

    <b>Langkah 1 :</b><br>
    Jalankan perintah "fn list context" dan dilanjutkan dengan perintah "fn use context ap-osaka-1.
        <br>
        
    ![Screenshot](img/langkah8.png)<br>

    <b>Langkah 2 :</b><br>
    Jalankan perintah fn update context oracle.compartment-id seperti berikut.<br>
        
    ![Screenshot](img/langkah9.png)<br>


7. Perhatikan pada langkah ke 4, ubah nilai [repo-name-prefix] menggunakan username / repository name. Sebagai contoh: polinema.<br><br>
![Screenshot](img/langkah10.png)<br>

8. Pada langkah ke 5, dilakukan proses pembuatan token untuk autentikasi. Tekan tombol Generate Token dan lengkapi form Description dengan nama yang relevan (contoh: faas). Simpan token tersebut.<br><br>
![Screenshot](img/langkah11.png)<br>
![Screenshot](img/langkah12.png)<br>
![Screenshot](img/langkah13.png)<br>
![Screenshot](img/langkah14.png)<br>

9. Token yang didapatkan, akan digunakan untuk autentikasi pada langkah ke 6. Tempel token yang didapatkan dan pastikan proses login telah berhasil.<br><br>
![Screenshot](img/langkah15.png)<br>

10. Menjalankan perintah fn list apps.<br><br>
![Screenshot](img/langkah16.png)<br>

11. Create, deploy, and invoke your function.<br><br>
![Screenshot](img/langkah17.png)<br>
![Screenshot](img/langkah18.png)<br>
![Screenshot](img/langkah19.png)<br>

12. Ikuti langkah-langkah sampai anda dapat menampilkan tampilan “Hello, world!”<br><br>
![Screenshot](img/langkah20.png)<br>

13. Navigasi menu ke Functions di sebelah kiri bawah. Anda akan mendapatkan detil fungsi yang tersedia. Pada halaman ini terdapat informasi mengenai Functions, serta invoke endpoint yang dapat digunakan untuk pemanggilan function.<br><br>
![Screenshot](img/langkah21.png)<br>

14. Memanggil Function<br>
a.	Selain menggunakan fn, Function pada FaaS dapat juga dipanggil menggunakan oci-cli.<br>
b.	Salin invoke endpoint kemudian panggil dengan format perintah sebagai berikut.<br><br>
![Screenshot](img/langkah22.png)<br>


   

