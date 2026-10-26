# Lab5_javascript
# LAPORAN PRAKTIKUM LAB 5 JAVASCRIPT
Nama    : Restu Aji Prasetyo
NIM     : 312510034
Kelas   : I253A

# Berikut dibawah ini hasil dari perubahan step by step
Langkah Pertama kita membuat isi awal dari laman webnya dengan menambahkan judul dan isi seperti dibawah ini
![Gambar1](media/konten_awal.png)
Langkah kedua yakni memberikan sentuhan javascript untuk merubah isi konten sesuai perintah dari code yang diberikan dari javascript
// script.js 
document.getElementById("pesan").textContent = "Hello World"; 
console.log("Hello World");
dan hasilnya seperti dibawah ini
![Gambar2](media/perubahan_1.png)
Langkah ke 3 yaitu memberikan code javascript untuk meminta input nama dengan code:
const namaPengguna = prompt("Masukkan nama Anda:", "");
dan akan tampil seperti dibawah ini
![Gambar3](media/Perubahan_2.png)
Lalu kita berikan code lagi agar website menyapa pengguna atas nama yang diberikan saat input dengan code:
if (namaPengguna && namaPengguna.trim() !== "") { 
  alert("Halo, " + namaPengguna + "!"); 
  document.getElementById("pesan").textContent = "Selamat datang, " + namaPengguna + "."; 
Maka akan tampil penyapaan atas nama pengunjung seperti dibawah ini
![Gambar4](media/Hasil_Perubahan_2.png)
![Gambar5](media/nilai_isi.png)
![Gambar6](media/ketika_nilai_isi.png)
![Gambar7](media/bilangan_isi.png)
![Gambar8](media/ketika_bilangan_isi.png)
![Gambar9](media/Home_after.png)
![Gambar10](media/nama_kosong.png)
![Gambar11](media/muncul_alert_nama.png)
![Gambar12](media/ketika_nama_kosong.png)
![Gambar13](media/ketika_bilangan_kosong.png)
![Gambar14](media/muncul_alert_input.png)
![Gambar15](media/masukkan_bil_bulat.png)
![Gambar16](media/button_background_green.png)
![Gambar17](media/button_background_white.png)
![Gambar18](media/button_background_blue.png)
![Gambar19](media/checkbox_harga_realtime.png)
![Gambar20](media/Nilai_A.png)
![Gambar21](media/Nilai_C.png)
![Gambar22](media/nilai_E.png)
![Gambar23](media/nilai_lewat_batas.png)


