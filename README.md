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

Berikut adalah jawaban lengkap untuk pertanyaan dan tugas mengenai JavaScript pada gambar di atas:

---

### 1. Jelaskan perbedaan `console.log()`, `alert()`, `prompt()`, dan `textContent`/`innerHTML`



* **`console.log()`**: Digunakan untuk mencetak pesan atau hasil data ke konsol browser (biasanya digunakan oleh programmer untuk keperluan *debugging* atau mengecek nilai variabel).
* **`alert()`**: Memunculkan jendela pop-up peringatan kecil di browser yang berisi pesan dan tombol "OK".
* **`prompt()`**: Memunculkan jendela pop-up dialog yang meminta pengguna untuk memasukkan teks/input melalui sebuah kolom isian.
* **`textContent`**: Properti untuk mengubah atau mengambil teks biasa di dalam suatu elemen HTML tanpa memproses tag HTML di dalamnya.
* **`innerHTML`**: Properti untuk mengubah atau mengambil konten di dalam elemen HTML, termasuk struktur tag HTML di dalamnya (seperti tag `<b>`, `<span>`, dll.).

---

### 2. Apa perbedaan `let` dan `const`? Berikan contoh



* **`let`**: Digunakan untuk mendeklarasikan variabel yang nilainya **dapat diubah** (*reassigned*) di kemudian hari.
* **`const`**: Digunakan untuk mendeklarasikan variabel yang nilainya **tetap** (konstan) dan tidak dapat diubah setelah pertama kali dideklarasikan.
* **Contoh:**
```javascript
let skor = 10;
skor = 15; // Valid: nilai let boleh diubah

const pi = 3.14;
// pi = 3.15; // Error: nilai const tidak boleh diubah ulang

```



---

### 3. Apa perbedaan operator `==` dan `===` ?



* **`==` (Equal)**: Membandingkan dua nilai untuk melihat apakah **nilainya sama**. Operator ini melakukan konversi tipe data otomatis (*type coercion*) jika tipe data kedua sisi berbeda (contoh: `"5" == 5` bernilai `true`).
* **`===` (Strict Equal)**: Membandingkan nilai **sekaligus tipe datanya**. Nilai dan tipe data harus benar-benar sama persis tanpa konversi otomatis (contoh: `"5" === 5` bernilai `false` karena satu string dan satu number).



---

### 4. Jelaskan fungsi `if-else` dan `switch`. Kapan masing-masing dapat digunakan?



* **`if-else`**: Digunakan untuk mengevaluasi kondisi berdasarkan nilai boolean (`true` atau `false`).
* *Kapan digunakan*: Sangat cocok untuk kondisi yang kompleks, melibatkan rentang nilai (misalnya `nilai >= 80`), atau pengecekan banyak kondisi berbeda.


* **`switch`**: Digunakan untuk mengevaluasi satu ekspresi atau variabel terhadap banyak pilihan nilai tetap secara spesifik.
* *Kapan digunakan*: Cocok digunakan ketika Anda memeriksa satu variabel terhadap banyak nilai diskrit yang pasti (misalnya pilihan menu 1, 2, 3, atau hari dalam seminggu).



---

### 5. Apa fungsi parameter dan `return` dalam *function*?



* **Parameter**: Variabel penampung yang ditulis di dalam tanda kurung saat fungsi dideklarasikan, berfungsi untuk menerima data atau argumen dari luar saat fungsi tersebut dipanggil.
* **`return`**: Perintah di dalam fungsi untuk menghentikan eksekusi fungsi sekaligus mengembalikan hasil akhir proses dari fungsi tersebut kembali ke bagian program yang memanggilnya.

---

### 6. Bagaimana JavaScript memilih elemen HTML menggunakan `document.getElementById()`?



Fungsi `document.getElementById('namaId')` bekerja dengan cara mencari dan mengambil elemen unik di dalam dokumen HTML berdasarkan nilai atribut `id` yang spesifik. Setelah elemen ditemukan, JavaScript dapat memodifikasi isi, mengubah gaya (CSS), atau membaca nilai dari elemen tersebut.

---

### 7. Buat *script* untuk memvalidasi *form* agar nama tidak kosong dan nilai berada pada rentang 0–100



Berikut adalah contoh fungsi JavaScript sederhana untuk melakukan validasi tersebut:

```javascript
function validasiForm() {
    // Mengambil nilai dari input HTML
    let nama = document.getElementById('namaInput').value.trim();
    let nilai = Number(document.getElementById('nilaiInput').value);

    // Validasi 1: Cek apakah nama kosong
    if (nama === "") {
        alert("Nama tidak boleh kosong!");
        return false;
    }

    // Validasi 2: Cek apakah nilai berada di rentang 0 - 100
    if (isNaN(nilai) || nilai < 0 || nilai > 100) {
        alert("Nilai harus berupa angka dan berada pada rentang 0 sampai 100!");
        return false;
    }

    alert("Validasi berhasil! Data valid.");
    return true;
}

```
