---

1. Algoritme yang Digunakan

Sistem Anda mengimplementasikan dua jenis *substitution cipher* (sandi substitusi):

* **Caesar Cipher:**
* **Cara Kerja:** Ini adalah sandi geser. Setiap huruf dalam teks digantikan oleh huruf lain yang memiliki selisih posisi tertentu dalam alfabet.
* **Input Kunci:** Berupa angka (misal: kunci 3, maka A menjadi D).


* **Vigenère Cipher:**
* **Cara Kerja:** Ini adalah versi lebih canggih dari Caesar. Alih-alih menggeser semua huruf dengan angka yang sama, Vigenère menggunakan kata kunci (teks). Setiap huruf pada kata kunci menentukan jumlah pergeseran untuk huruf yang bersesuaian di pesan asli.
* **Input Kunci:** Berupa kata/huruf (misal: kunci "ABC").



---

2. Fitur Utama Sistem

* **Antarmuka Dinamis:** Menggunakan JavaScript untuk mengubah *placeholder* dan validasi input secara otomatis saat pengguna memilih jenis cipher (misalnya, input kunci hanya menerima angka untuk Caesar dan hanya huruf untuk Vigenère).
* **Case Sensitive Preservation:** Kode Anda cukup cerdas untuk mempertahankan huruf besar dan kecil. Jika Anda memasukkan "Halo", hasilnya tetap memiliki huruf kapital di awal.
* **Abaikan Karakter Non-Alfabet:** Simbol seperti spasi, tanda seru, atau angka tidak akan dienkripsi, sehingga struktur kalimat tetap terjaga.
* **Desain Visual (UI):** Menggunakan animasi CSS `aurora` dan `neonGlow` yang memberikan kesan futuristik/hacker pada judul dan garis pemisah.

---

3. Alur Kerja Logika (Backend JavaScript)

Secara teknis, sistem Anda bekerja dengan langkah berikut:

1. **Pengambilan Data:** Mengambil teks dan kunci dari elemen `<input>`.
2. **Konversi ASCII:** Menggunakan fungsi `charCodeAt()` untuk mengubah huruf menjadi kode angka standar (ASCII).
3. **Operasi Matematika:**
* **Enkripsi:**  (Pesan + Kunci).
* **Dekripsi:**  (Pesan - Kunci).


4. **Output:** Mengembalikan hasil hitungan tadi ke dalam bentuk karakter menggunakan `String.fromCharCode()` dan menampilkannya di layar.

---

4. Analisis Kelebihan dan Kekurangan

Kelebihan
1.User Friendly: Mudah digunakan bahkan oleh orang awam.
2.Responsif: Berjalan langsung di browser tanpa butuh server (Client-side).
3.Edukatif: Sangat baik untuk alat belajar dasar-dasar keamanan informasi

Kekurangan
1.Keamanan Rendah: Caesar dan Vigenère sangat mudah dipecahkan (brute force) dengan komputer modern.
2.Terbatas: Hanya mendukung alfabet (A-Z), tidak bisa mengenkripsi file atau gambar.

---

### Saran Pengembangan:

Jika Anda ingin meningkatkan proyek ini ke **"Level 2"**, Anda bisa mencoba menambahkan:

1. **Copy to Clipboard:** Tombol untuk menyalin hasil enkripsi secara otomatis.
2. **Dark/Light Mode:** Fitur beralih tema.
3. **Algoritme Modern:** Mencoba implementasi **AES (Advanced Encryption Standard)** yang digunakan secara nyata di dunia perbankan dan WhatsApp.

