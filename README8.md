Nama : Ihza Dafa Maulidan 
NPM : 21066652726 
PBP F TUGAS 8 

1. Jelaskan perbedaan Navigator.push dan Navigator.pushReplacement.

Di flutter memiliki cara untuk keluar dari halaman sambil menghapus halaman saat yang diakses seperti menggunakan Navigator.pushReplacement yang hanya mengganti halaman(routing) yang baru diakses dengan sifat sementara setelah routing dipush kedalam stack.

Beda halnya dengan Navigator.push yang dengan tidak menghapus halman(routing) sebelumnya karena routing akan di push ke dalam stack secara langsung

2. Sebutkan widget apa saja yang kamu pakai di proyek kali ini dan jelaskan fungsinya.
 
Saya menggunakan widget seperti ListViewBuilder yang digunakan untuk menampilkan data yang telah diinput oleh pengguna dengan tampilan list tak terbatas, 

yang kedua widget TextButton sebagai tombol yang digunakan sebagai ActionListener untuk menjalankan (menyimpan data), 

yang ketiga widget DropdownButton sebagai penerima input dari pilihan dropdown pengguna bersama dengan widget DropdownHideUnderline untuk menghapus garis bawah dari DropdownButton, 

yang keempat Material yang menggabungkan sejumlah widget yang umumnya diperlukan untuk aplikasi yang mengimplementasikan Desain Material.

dan yang terakhir ListTile yang berguna untuk menampilkan pilihan pada drawer

3. Sebutkan jenis-jenis event yang ada pada Flutter (contoh: onPressed).

a. onPressed: Event akan dieksekusi setelah menerima input berupa tekan (biasanya pada button)
b. onHover: Event akan dieksekusi setelah menerima input selama pointer mouse berada di widget
c. onFocusChange: Event akan dieksekusi setelah menerima input selama pengguna sedang berinteraksi pada widget
d. onChanged: Event akan dieksekusi setelah menerima input selama pengguna sednag melakukan perubahan terhadap value yang dimiliki oleh widget
e. onSaved: Event akan dieksekusi ketika nilai dari form disimpan melalui FormState.save

4. Jelaskan bagaimana cara kerja Navigator dalam "mengganti" halaman dari aplikasi Flutter.

Cara kerja sebuah navigator menggunakan konsep tumpukan seperti stack untuk mengubah halaman dari aplikasi Flutter. Flutter biasanya dapat dipush untuk membuka halaman yang dijalankannya di tumpukan (stack), menggunakan pop untuk kembali ke halaman yang dilihat/kembali sebelumnya dengan menggunakan push atau menggeser halaman kembali. Flutter menggunakan MaterialPageRoute untuk melakukan proses pagination (halaman terpisah).

5. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas.

-  Kita membuat beberapa file seperti drawer.dart berisi DrawerApp "const DrawerApp({super.key})" yang akan digunakan sebagai drawer di main.dart, data_budget.dart, dan tambah_budget.dart untuk menavigasi halaman.

- Selanjutnya kita buat form dengan elemen input yang menerima String judul budget, int nominal budget, String jenisBudget tergantung pemasukan atau pengeluaran dan date sebagai input pada tambah_budget.dart.

- Saya kemudian membuat kelas Budget di tambah_budget.dart yang menerima input yang sama dengan form.

- Menambahkan file globals.dart yang berisi Budget  sebagai variabel global yang merupakan daftar dari Budget yang kita buat sebagai list untuk menyimpan datanya, nah dengan melakukan import saya bisa mengakses list di file tambah_budget.dart untuk digunakan pada file data_budget.dart

- Terakhir kita taampilkan data di globals.budgets di data_budget.dart menggunakan ListView.builder yang berisi ListTile.
