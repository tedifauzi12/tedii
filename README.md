Nama  : Tedi Fauzi
NIM   : C2583207020
Kelas : PTI3B

1 Nama Proyek
Sistem Monitoring Stok dan Penjualan Kantin Kampus Berbasis Bahasa C

2. Deskripsi Singkat
Sistem Monitoring Stok dan Penjualan Kantin Kampus merupakan aplikasi berbasis console yang dibuat menggunakan bahasa pemrograman C. Program ini dirancang untuk membantu pengelolaan data produk kantin, pemantauan persediaan barang, serta pencatatan transaksi penjualan.

Program menyediakan berbagai fitur, seperti menambahkan produk, mengubah data produk, melakukan transaksi penjualan, menambah stok, mencari produk, mengurutkan produk, dan menampilkan laporan penjualan.

Data produk disimpan menggunakan array sebagai struktur data utama. Dengan adanya program ini, proses pengelolaan stok dan penjualan kantin menjadi lebih terstruktur, praktis, dan mudah dilakukan.

3. Daftar Fitur Program
Berikut adalah fitur-fitur yang tersedia dalam program:
No.	Fitur	Deskripsi
1	Lihat Daftar Produk	Menampilkan seluruh produk beserta harga dan stok yang tersedia.
2	Tambah Produk	Menambahkan produk baru dengan nama, harga, dan stok awal.
3	Ubah Produk	Mengubah harga dan jumlah stok produk yang sudah terdaftar.
4	Transaksi Penjualan	Melakukan pembelian produk, menghitung subtotal, dan total pembayaran.
5	Tambah Stok	Menambahkan jumlah persediaan produk.
6	Cari Produk	Mencari produk berdasarkan nama atau sebagian kata dari nama produk.
7	Urutkan Produk	Mengurutkan produk berdasarkan harga termurah atau jumlah terjual terbanyak.
8	Laporan Penjualan	Menampilkan jumlah produk terjual, pendapatan, total unit, dan produk terlaris.
9	Cek Stok Menipis	Menampilkan produk yang memiliki stok kurang dari 5.
10	Keluar	Mengakhiri program.

Fitur tambahan:
- Validasi input agar data yang dimasukkan sesuai ketentuan.
- Pemeriksaan stok agar transaksi tidak melebihi persediaan.
- Pencegahan nama produk yang sama.
- Data awal berupa 6 produk yang sudah tersedia ketika program dijalankan.
- 
4. Penjelasan Penggunaan Array
Program ini menggunakan array sebagai struktur data utama untuk menyimpan dan mengelola informasi produk kantin.

Terdapat lima array utama dan satu variabel penghitung jumlah data.
A. Array nama
char nama[MAKS][PANJANG_NAMA];


Digunakan untuk menyimpan nama produk dalam bentuk array karakter dua dimensi.
- MAKS = 50: kapasitas maksimal produk.
- PANJANG_NAMA = 30: kapasitas karakter untuk setiap nama produk.
Contohnya: Nasi Goreng, Mie Ayam, Es Teh, dan sebagainya.
B. Array harga
int harga[MAKS];


Digunakan untuk menyimpan harga satuan setiap produk.

Contohnya:
- Nasi Goreng: Rp12.000
- Mie Ayam: Rp10.000
- Es Teh: Rp4.000
C. Array stok
int stok[MAKS];


Digunakan untuk menyimpan jumlah persediaan setiap produk yang masih tersedia.

Nilai stok akan berkurang ketika terjadi transaksi penjualan dan bertambah ketika pengguna melakukan penambahan stok.
D. Array terjual
int terjual[MAKS];


Digunakan untuk mencatat jumlah unit setiap produk yang berhasil terjual.

Data ini digunakan dalam pembuatan laporan penjualan dan menentukan produk terlaris.
E. Array pendapatan
int pendapatan[MAKS];


Digunakan untuk menyimpan akumulasi pendapatan dari setiap produk berdasarkan transaksi yang berhasil dilakukan.
F. Variabel jumlah
int jumlah = 0;


Digunakan untuk menghitung jumlah produk yang sudah terdaftar dalam program.

Variabel ini juga menentukan batas perulangan dalam mengakses data array, yaitu dari indeks 0 sampai jumlah-1.
G. Penerapan Array dalam Program
Semua array utama menggunakan indeks yang saling berhubungan.

Sebagai contoh:
Indeks	Nama	Harga	Stok
0	Nasi Goreng	12.000	20
1	Mie Ayam	10.000	15
2	Es Teh	4.000	30
3	Gorengan	2.000	40

Artinya, indeks ke-0 pada array nama, harga, dan stok merujuk pada produk yang sama, yaitu Nasi Goreng.

Kesimpulan penggunaan array:

Array digunakan agar data produk dapat disimpan dalam satu kelompok dengan indeks yang terstruktur. Penggunaan array juga memudahkan proses penambahan, perubahan, pencarian, pengurutan, transaksi penjualan, serta pembuatan laporan tanpa harus membuat variabel terpisah untuk setiap produk.

Selain itu, program menggunakan array tambahan beli[MAKS] pada fungsi transaksi penjualan untuk menyimpan jumlah pembelian setiap produk dalam satu transaksi.
5. Petunjuk Kompilasi dan Menjalankan Program
Program dibuat menggunakan bahasa pemrograman C dan dapat dijalankan melalui compiler GCC, misalnya menggunakan MinGW pada Windows.
A. Persiapan
Pastikan komputer sudah memiliki:
1. Compiler GCC (MinGW atau MinGW-w64).
2. Text editor atau IDE, seperti Visual Studio Code, Code::Blocks, atau Dev-C++.
3. File sumber program kantin.c.
B. Kompilasi Program
Buka terminal atau Command Prompt, kemudian arahkan ke folder tempat file kantin.c disimpan.

Jalankan perintah berikut:
gcc kantin.c -o kantin


Perintah tersebut berfungsi untuk mengompilasi kode sumber C menjadi program executable bernama kantin.
C. Menjalankan Program
Untuk Windows:
kantin.exe


Untuk Linux:
./kantin


Jika kompilasi berhasil, program akan menampilkan menu utama seperti berikut.
D. Tampilan Menu Utama
CONTOH TAMPILAN PROGRAM
=========================================
   MONITORING STOK & PENJUALAN KANTIN
=========================================
1. Lihat Daftar Produk    6. Cari Produk
2. Tambah Produk          7. Urutkan Produk
3. Ubah Produk            8. Laporan Penjualan
4. Transaksi Penjualan    9. Cek Stok Menipis
5. Tambah Stok            0. Keluar

Pilih menu :



E. Cara Menggunakan Program
1. Masukkan angka 1 untuk melihat daftar produk.
2. Masukkan angka 2 untuk menambahkan produk baru.
3. Masukkan angka 3 untuk mengubah harga atau stok produk.
4. Masukkan angka 4 untuk melakukan transaksi penjualan.
5. Masukkan angka 5 untuk menambahkan stok produk.
6. Masukkan angka 6 untuk mencari produk.
7. Masukkan angka 7 untuk mengurutkan produk.
8. Masukkan angka 8 untuk melihat laporan penjualan.
9. Masukkan angka 9 untuk memeriksa stok yang menipis.
10. Masukkan angka 0 untuk keluar dari program.

6. Kesimpulan
Program Sistem Monitoring Stok dan Penjualan Kantin Kampus merupakan aplikasi sederhana berbasis bahasa C yang menerapkan konsep array, fungsi, percabangan, perulangan, dan pengolahan data.

Penggunaan array memungkinkan program menyimpan berbagai informasi produk secara terstruktur dan efisien. Program ini juga membantu pengguna dalam mengelola persediaan, mencatat transaksi, serta mengetahui hasil penjualan.

Dengan demikian, proyek ini dapat menjadi penerapan nyata materi Algoritma dan Pemrograman Lanjutan, khususnya dalam penggunaan array dan fungsi pada bahasa pemrograman C.
<img width="333" height="227" alt="Screenshot 2026-11-17 143131" src="https://github.com/user-attachments/assets/9f4acee5-a39c-4a90-a693-8bfbcf494abe" />
<img width="398" height="291" alt="Screenshot 2026-11-17 143224" src="https://github.com/user-attachments/assets/35804b67-f4ff-4f54-86fe-7653882d0d42" />
<img width="398" height="325" alt="Screenshot 2026-11-17 143301" src="https://github.com/user-attachments/assets/d474304a-97a3-4910-9467-2e39fae9f91d" />
<img width="397" height="321" alt="Screenshot 2026-11-17 143426" src="https://github.com/user-attachments/assets/2eaaf20f-0f2d-4b98-b062-a1438b6df3f8" />
<img width="416" height="409" alt="Screenshot 2026-11-17 143657" src="https://github.com/user-attachments/assets/9c96949f-685c-40ce-abe3-629bb7e3f722" />
<img width="265" height="246" alt="Screenshot 2026-11-17 143715" src="https://github.com/user-attachments/assets/be475616-dbf2-45f8-83cb-1b5da3e3bbae" />
<img width="392" height="212" alt="Screenshot 2026-11-17 143909" src="https://github.com/user-attachments/assets/3cb80222-5097-4243-a51d-c5c31a251233" />
<img width="340" height="181" alt="Screenshot 2026-11-17 143954" src="https://github.com/user-attachments/assets/7fc61064-dcf6-422c-b74e-b1b6efa6ee17" />
