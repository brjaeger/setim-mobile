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
