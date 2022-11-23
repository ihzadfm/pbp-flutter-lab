Nama : Ihza Dafa Maulidan 
NPM : 21066652726 
PBP F TUGAS 9

1. Apakah bisa kita melakukan pengambilan data JSON tanpa membuat model terlebih dahulu? Jika iya, apakah hal tersebut lebih baik daripada membuat model sebelum melakukan pengambilan data JSON?

Iya, bisa ngambilan data JSON tanpa membuat model terlebih dahulu dan yang akan dikirim adalah data yang belum jadi pada Future<http.Response>. Ini akan mempersulit pengembang code untuk mengakses data, jadi dengan bantuan model s mempunyai tujuan agar dapat mengubah respons http menjadi objek dart. Menurut saya, lebih baik membangun modelnya terlebih dahulu dikarenakan tidak hanya lebih baik dan lebih mudah, tetapi juga kodenya lebih bersih.

2. Sebutkan widget apa saja yang kamu pakai di proyek kali ini dan jelaskan fungsinya!

1. TextButton: sebagai tombol yang digunakan sebagai ActionListener untuk menjalankan (menyimpan data)
2. FutureBuilder: build serta fetching data dan mengelola asynchronous sumber data
3. ListTile: untuk menjalankan dan menampilkan perintah onTap() menampilkan pilihan dan data pada drawer alignment dan position yang sesuai
4. Checkbox: Sebagai widget yang terjadinya checkbox yang dapat diklik

3. Jelaskan mekanisme pengambilan data dari json hingga dapat ditampilkan pada Flutter!

a. Gunakan HTTP dalam fungsifetchWatchlist agar bisa melakukan HTTP request seperti GET dalam pengambilan data. Nah hal ini akan mengembalikan list objek MyWatchlist
Selanjutnya berikan proyek yang sedang dibangun koneksi internet dengan menambahkan beberapa baris kode ke file android/app/src/main/AndroidManifest.xml yakni: 

'
 <!-- Required to fetch data from the Internet. -->
    <uses-permission android:name="android.permission.INTERNET" />
'

b. Buat direktori kelas template model dan buat file dart template model dengan data json yang ingin kita ambil dan tampilkan dengan response data. Saya menggunakan situs web Quicktype untuk menulis kode contoh MyWatchlist yang menyesuaikan dengan JSON yang disediakan

c. Tambahkan halaman di direktori page yang menampilkan data json dan buat fungsi FutureBuilder yang mendapatkan data dari alamat HTTP yang diberikan dengan mendekode url ke json dan mengonversinya menjadi objek WatchList.

d. Menampilkan data dengan widget yang diinginkan seperti menggunakan ListView dan ListTile untuk menampilkan data dari fungsi fetchWatchlistv.

4. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas!

1. Refactor file di dalam folder lib menjadi 3 folder, yaitu model, page, dan utl. Menambahkan tombol navigasi pada drawer ke halaman mywatchlist.

2. Membuat file mywatchlist.dart di folder model untuk membuat Model MyWatchList untuk mempermudah data dan struktur data apa yang akan diterima nantinya ketika melakukan pemanggilan JSON dari web service.

3. Membuat file fetch_watchlist.dart di folder utl untuk melakukan pengambilan data JSON dari web service berupa data watchlist. File tersebut dengan depedensi HTTP melakukan request ke server heroku yang sudah dideploy di tugas3

4. Membuat file my_watchlist.dart di folder page untuk menampilkan seluruh judul watchlist pada halaman mywatchlist dengan StatefulWidget MywatchlistPage yang berisi FutureBuilder pengambilan data dengan fungsi fetchwatchlist. Setiap judul watchlist ditampilkan per baris yang dibungkus dengan widget Card. Kemudian dibuat navigasi dari setiap judul ke halaman detail menggunakan widget ListTile

5. Membuat file my_watchlist_detail.dart di folder page untuk menampilkan halaman detail untuk setiap watchlist pada halaman mywatchlist dengan StatelessWidget MywatchlistDetailPage yang berisi pengambilan data dan diterusakannya dari MyWatchlistPage ke MyWatchlistDetailPage menggunakan Navigator.push

6. Halamannya menampilkan judul, release date, rating, review, dan status (sudah ditonton/belum) dengan menambahkan juga widget checkbox dan juga onChanged fungsi