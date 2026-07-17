🍋 Segmentasi Daun dan Buah Jeruk Nipis Berbasis Ruang Warna HSV
Repositori ini berisi source code dan Laporan Landasan Teori yang disusun untuk memenuhi tugas Ujian Praktikum Mata Kuliah Pengolahan Citra Digital.

Proyek ini berfokus pada implementasi teknik Computer Vision dasar untuk memisahkan (segmentasi) objek target (daun dan buah jeruk nipis) dari latar belakangnya dengan memanfaatkan deteksi spektrum warna pada ruang HSV (Hue, Saturation, Value).

📋 Deskripsi Proyek
Dalam pengolahan citra, mendeteksi objek berdasarkan warna pada ruang RGB sangat rentan terhadap perubahan intensitas cahaya (seperti pantulan sinar matahari atau bayangan). Proyek ini menyelesaikan masalah tersebut dengan mengonversi citra ke dalam ruang warna HSV.

Selain deteksi warna, proyek ini juga mengimplementasikan operasi morfologi untuk memperbaiki hasil masking yang berlubang akibat pantulan cahaya (noise), sehingga ekstraksi gambar dengan operasi logika bitwise dapat menghasilkan potongan objek yang utuh dan rapi.

🚀 Fitur dan Alur Pemrosesan (Pipeline)
1. Konversi Ruang Warna: Mengubah matriks citra dari format bawaan BGR (OpenCV) menjadi RGB (visualisasi) dan HSV (pemrosesan).

2. Thresholding & Masking: Penentuan batas bawah (lower bound) dan batas atas (upper bound) untuk mengisolasi piksel berwarna hijau menjadi citra biner (hitam-putih).

3. Morfologi Closing: Penggunaan kernel matriks 5x5 untuk menambal/mendempul titik-titik hitam (lubang) di dalam area daun yang disebabkan oleh silau cahaya matahari.

4. Ekstraksi Objek (Bitwise AND): Pemotongan gambar asli menggunakan mask yang sudah dibersihkan untuk menampilkan daun dan buah tanpa latar belakang.

🛠️ Teknologi yang Digunakan
- Bahasa Pemrograman: Python 3

- Environment: Jupyter Notebook (.ipynb)

- Library:

    - OpenCV (cv2) - Pemrosesan citra dasar.

    - NumPy (np) - Manipulasi matriks dan komputasi array.

    - Matplotlib (plt) - Visualisasi dan plotting gambar.

📂 Struktur Repositori
- JerukNipis.jpeg : Berkas gambar citra asli yang digunakan sebagai bahan uji.

- LokasiJN.jpeg : Berkas gambar lokasi pengambilan citra dilakukan.

- Segmentasi_Jeruk_Nipis.ipynb : Source code utama (Jupyter Notebook) yang memuat seluruh proses dari pembacaan gambar hingga visualisasi akhir.

- UAS_PCD_202431036_Fathur Rasyid Irimawa_E.pdf : Laporan resmi yang berisi Landasan Teori, Rumusan Masalah, dan Kesimpulan dari praktikum.

👨‍💻 Pembuat
- Nama: Fathur Rasyid Irimawa

- NIM: 202431036

- Mata Kuliah: Pengolahan Citra Digital
