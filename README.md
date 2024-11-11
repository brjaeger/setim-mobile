# setim_mobile

Tugas 7
1. Jelaskan apa yang dimaksud dengan stateless widget dan stateful widget, dan jelaskan perbedaan dari keduanya.
- Stateless Widget: Ini adalah widget yang tidak memiliki state yang bisa berubah selama masa hidupnya. Artinya, data yang ada di dalam Stateless Widget bersifat tetap (immutable), sehingga ketika widget ini dibangun, tampilannya tidak akan berubah meskipun terjadi perubahan di luar widget tersebut. Contoh dari Stateless Widget adalah Text, Icon, dan Container.
- Stateful Widget: Ini adalah widget yang memiliki state yang bisa berubah selama masa hidupnya. Widget ini dapat merespons perubahan yang terjadi dan bisa memperbarui tampilannya ketika state-nya berubah. Contoh dari Stateful Widget adalah Checkbox, Slider, atau Form dengan input yang dapat diubah.

Perbedaan utama antara Stateless dan Stateful Widget adalah bahwa Stateless Widget tidak bisa berubah, sedangkan Stateful Widget dapat berubah selama masa hidup widget tersebut karena memiliki state yang dinamis.

2. Sebutkan widget apa saja yang kamu gunakan pada proyek ini dan jelaskan fungsinya.
- AppBar: Menampilkan bagian atas halaman yang berfungsi sebagai judul dari aplikasi.
- Text: Menampilkan teks pada layar.
- Icon: Menampilkan ikon pada layar.
- Card: Membuat kotak dengan bayangan dan padding yang rapi, cocok untuk menampilkan informasi dalam format kotak.

3. Apa fungsi dari setState()? Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut.
- setState() adalah metode yang digunakan dalam Stateful Widget untuk memberi tahu sistem bahwa state atau data internal widget tersebut telah berubah. Ketika setState() dipanggil, Flutter akan membangun ulang widget tersebut dan child-nya, yang memungkinkan tampilan diperbarui untuk mencerminkan perubahan data.
- Variabel apa saja yang terkait dengan perubahan dalam widget, seperti nilai dari input, status pilihan pada Checkbox, atau data yang diambil dari API, dapat terdampak oleh setState() karena mereka mempengaruhi tampilan widget.

4. Jelaskan perbedaan antara const dengan final.
- const: const digunakan untuk variabel atau objek yang nilai dan statusnya bersifat konstan sejak kompilasi. Variabel yang dideklarasikan dengan const tidak dapat diubah lagi, dan harus diberikan nilai pada saat deklarasi. const umumnya digunakan untuk mendefinisikan objek immutable yang sudah diketahui saat compile time.
- final: final juga digunakan untuk membuat variabel yang tidak dapat diubah, tetapi berbeda dengan const, nilai variabel final dapat ditetapkan di waktu runtime, bukan hanya pada compile time. final cocok digunakan untuk variabel yang nilainya tidak diketahui saat kompilasi, seperti data yang diterima dari input pengguna atau hasil dari suatu perhitungan.

5. Jelaskan bagaimana cara kamu mengimplementasikan checklist-checklist di atas
- Pertama yaitu membuat aplikasi Flutter baru dengan menjalankan perintah flutter create .
- Membuat file menu.dart dan mengisinya untuk menampilkan layout yang akan muncul pada bagian homepage.
- Membuat kode untuk menampilkan widget yang akan dibuat seperti InfoCard dan GridView untuk menampilkan tombol, dan lain-lain sesuai dengan kebutuhan.
- Menambahkan Snackbar untuk menampilkan tulisan sesuai dengan tombol yang diklik
- Merubah warna tombol agar memiliki lebih banyak variasi.

Tugas 8
1. Apa kegunaan const di Flutter? Jelaskan apa keuntungan ketika menggunakan const pada kode Flutter. Kapan sebaiknya kita menggunakan const, dan kapan sebaiknya tidak digunakan?
   - Kegunaan: Kata kunci const di Flutter digunakan untuk membuat objek bersifat immutable (tidak dapat diubah) dan compile-time constant. Artinya, nilai objek tersebut ditentukan pada saat kompilasi, bukan pada saat runtime.
   - Keuntungan: Penggunaan const memberikan beberapa keuntungan, antara lain:
      1. Mengurangi Penggunaan Memori: Objek const hanya akan dibuat satu kali, sehingga memori yang digunakan lebih efisien. Ini sangat bermanfaat untuk widget statis yang sering digunakan.
      2. Optimisasi Kinerja: Karena objek const tidak perlu dibuat ulang setiap kali widget di-render, penggunaan const dapat mengurangi waktu render dan mempercepat performa aplikasi.
   - Kapan Menggunakan const: Sebaiknya gunakan const pada widget atau objek yang tidak akan berubah selama runtime. Contohnya, pada teks, ikon, atau layout yang tidak membutuhkan update ulang.
   - Kapan Tidak Menggunakan const: Jangan gunakan const jika objek atau widget tersebut memiliki elemen yang dinamis (akan berubah saat runtime), seperti input teks yang dapat diubah oleh pengguna atau tampilan yang tergantung pada data API.
   
2. Jelaskan dan bandingkan penggunaan Column dan Row pada Flutter. Berikan contoh implementasi dari masing-masing layout widget ini!
   - Column: Widget yang menyusun elemen di dalamnya secara vertikal.
   - Row: Widget yang menyusun elemen di dalamnya secara horizontal.
   Perbandingan:
   - Column: Cocok digunakan untuk tata letak elemen yang memanjang ke bawah. Biasanya digunakan dalam bentuk daftar atau urutan elemen secara vertikal.
   - Row: Cocok untuk tata letak elemen yang memanjang ke samping. Biasanya digunakan ketika elemen perlu diletakkan bersebelahan secara horizontal.
    Contoh Pengimplementasian:
   - Column: Pada penempatan tombol di menu.dart.
   - Row: Pada penempatan text untuk product, descriptionm dan price di moodentry_form.dart.
     
3. Sebutkan apa saja elemen input yang kamu gunakan pada halaman form yang kamu buat pada tugas kali ini. Apakah terdapat elemen input Flutter lain yang tidak kamu gunakan pada tugas ini? Jelaskan!
   - Elemen Input yang Digunakan: Beberapa elemen input yang sering digunakan di Flutter adalah TextField untuk input teks, Checkbox untuk memilih opsi tertentu, DropdownButton untuk pilihan opsi dropdown, dan Switch untuk opsi on/off.
   - Elemen Input Lain yang Tidak Digunakan: Elemen seperti Slider, Radio, dan DatePicker juga tersedia tetapi mungkin tidak diperlukan tergantung pada kebutuhan halaman form.

4. Bagaimana cara kamu mengatur tema (theme) dalam aplikasi Flutter agar aplikasi yang dibuat konsisten? Apakah kamu mengimplementasikan tema pada aplikasi yang kamu buat?
   - Cara Mengatur Tema: Untuk mengatur tema, Flutter menyediakan ThemeData di MaterialApp yang memungkinkan kita mengatur warna, font, dan gaya default untuk seluruh aplikasi, sehingga tampilannya konsisten. Ya, saya mengimplementasikan tema pada aplikasi ini

5. Bagaimana cara kamu menangani navigasi dalam aplikasi dengan banyak halaman pada Flutter?
   - Navigator: Flutter menyediakan widget Navigator untuk menangani navigasi di antara halaman. Setiap kali kita berpindah halaman, Flutter menambahkan atau menghapus halaman dari stack navigasi, sehingga kita bisa melakukan navigasi push dan pop.
   - Named Routes: Ini memungkinkan navigasi menggunakan nama untuk setiap halaman yang lebih terstruktur dan mudah dikelola