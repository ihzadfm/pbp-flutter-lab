Nama : Ihza Dafa Maulidan 
NPM : 21066652726 
PBP F

1. Jelaskan apa yang dimaksud dengan stateless widget dan stateful widget dan jelaskan perbedaan dari keduanya.

Stateful widget adalah widget yang bisa diubah bentuknya berkali-kali. Sifat widget ini lebih dinamis mengikuti perintah arahan, dan bisa digunakan pada layar lain saat aplikasi tengah dijalankan. Contohnya, bentuk tombol yang berubah saat ditekan user, atau mungkin perubahan teks pada tombol tersebut.

Beda halnya dengan stateless widget. Widget ini bersifat statis, tidak bisa diubah, dan sudah ditetapkan dengan pasti oleh konfigurasi tertentu. Stateless widget tidak akan berubah bentuknya walau kamu sudah menekannya di layar. Selain itu, stateless widget tidak bisa kamu gunakan di layar lain selayaknya stateful widget. Maka dari itu, kamu harus melakukan proses coding stateless widget dari awal supaya bisa menggunakan fitur ini lebih dari sekali.

2. Sebutkan widget apa saja yang kamu pakai di proyek kali ini dan jelaskan fungsinya.
 
Saya menggunakan widget seperti Row class yang mempunyai fungsi widget yang digunakan untuk memposisikan widget-widget lainnya secara horizontal, yang kedua widget floatingActionButton sebagai tombol di bawah kanan kiri screen yang membuat aksi ketika diklik, yang ketiga widget Expanded widget sebagai container yang memperluas anak dari Row, Column (widget) atau flex sehingga mengisi ruang yang tersedia, dan yang terakhir Text widget supaya teks dapat muncul di screen.

3. Apa fungsi dari setState()? Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut.

Data dari sebuah stateful widget akan disimpan pada object State, membuatnya terpisah dari bagian presentasi (atau view). Nantinya, di dalam object State ini, data akan dimanipulasi dan diubah dengan memanggil fungsi setState(). Untuk merubah state gunakan perintah this.setState(). Ketika state berubah secara otomatis component akan di render ulang. method disini menggunakan arrow function untuk menghindari problem javascript bind.

4. Jelaskan perbedaan antara const dengan final.

"final" berarti penugasan tunggal: variabel terakhir atau bidang harus memiliki penginisialisasi. Setelah diberi nilai, nilai variabel final tidak dapat diubah. final memodifikasi variabel. variabel final hanya dapat ditetapkan sekali dan diinisialisasi ketika .__ diakses. konst secara internal bersifat final tetapi perbedaan utamanya adalah bahwa .__ konstanta waktu kompilasi yang diinisialisasi selama kompilasi. Variabel dari kelas dapat bersifat final tetapi tidak konstan dan jika Kita menginginkan konstanta .__ pada tingkat kelas, buatlah konstanta statis.

"const" memiliki arti yang sedikit lebih kompleks dan halus di Dart. const memodifikasi nilai. Kita dapat menggunakannya saat membuat koleksi, seperti const [1, 2, 3], dan ketika membangun objek (bukan yang baru) seperti const Point (2, 3). Di sini, const berarti bahwa seluruh keadaan dalam objek dapat ditentukan sepenuhnya pada waktu kompilasi dan bahwa objek akan dibekukan dan sepenuhnya tidak dapat diubah. Objek Const memiliki beberapa sifat dan batasan menarik:
- Dibuat dari data yang dapat dihitung pada waktu kompilasi. Objek const tidak memiliki akses ke apa pun yang Kita perlu hitung pada saat runtime. 1 + 2 adalah ekspresi const yang valid, tetapi DateTime.now () baru tidak. 
- Jika kita memiliki bidang terakhir yang berisi koleksi, koleksi itu masih bisa berubah. Jika Kita memiliki koleksi const, semua yang ada di dalamnya juga harus const, secara rekursif. 
- Dikanonikal. Ini adalah semacam string interning: untuk nilai const yang diberikan, objek const tunggal akan dibuat dan digunakan kembali tidak peduli berapa kali ekspresi const dievaluasi.

5. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas.

-  Kita mengganti FloatingActionButton yang ada dengan sebuah baris.

- Setelah itu, otomatis setelah menambahkan satu lagi dengan tujuan dikurangi karena berisi dua buah FloatingActionButton dari parameter FloatingActionButton sebagai sebuah baris.

- Saya kemudian mengubah  "You have clicked this button many times" menjadi string yang bergantung pada nilai state-counter.

- Sebelumnya, saya membuat variabel status baru untuk isGanjil dan warna komponen teks, terenyata saya juga dapat menggunakan operator ternary untuk menentukan variabel teks dan tipe TextStyle secara kondisional.
