# 12 - CI/CD

1. Student can understand about CI/CD
2. Student can create pipeline
3. Student  can  understand  about  variables,  secrets 
and token.

#
# Praktikum

#

### 1. Hosting Static Website Menggunakan CI/CD Pipeline Pada praktikum yang pertama akan dilakukan hosting static website di layanan Object Storage dari Oracle menggunakan GitHub Actions.

### 1.1. Menyiapkan Bucket Object Storage<br>

1. Masuk ke akun https://cloud.oracle.com dan navigasi ke menu Storage -> Buckets<br><br>
![Screenshot](img2/langkah1.png)<br><br>

2. Tekan tombol Create Bucket, dan lengkapi Bucket Name dengan os-react. Biarkan nilai lainnya dengan nilai default kemudian tekan tombol Create.<br><br>
![Screenshot](img2/langkah2.png)<br><br>

3. Ubah visibility bucket dengan menekan tombol Edit Visibility, dan ubah menjadi public. Tekan tombol Save Changes untuk menyimpan perubahan.<br><br>
![Screenshot](img2/langkah3.png)<br>
![Screenshot](img2/langkah4.png)<br><br>

4. Pada dashboard bucket, perhatikan nilai Namespace. Nilai ini nanti akan digunakan untuk pengaturan deployment.<br><br>
![Screenshot](img2/langkah5.png)<br>

### 1.2. Menyiapkan Project
1. Pada praktikum ini, akan digunakan React sehingga harus diinstall terlebih dahulu Node. Untuk  langkah  instalasi  Node  silahkan  gunakan  tautan  berikut  sebagai  referensi https://nodejs.org/en/download/ atau https://nodejs.org/en/download/package-manager/<br>

2. Setelah Node terinstall, silahkan lakukan Langkah generate project dengan menggunakan 
perintah berikut.
