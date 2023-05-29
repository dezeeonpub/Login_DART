
<p align="center">
 <img src="https://user-images.githubusercontent.com/91085882/137566814-9c8c078c-1c3e-475c-b23d-7f4922f74beb.gif"/>
</p>
<p align="center">
<a href="https://github.com/akmalabdilah"><img title="Author" src="https://img.shields.io/discord/102860784329052160?color=BLUE&label=M.%20AKMAL%20AL%20ABDILAH1&logo=GITHUB&logoColor=BLACK&style=plastic"></a>
<p align="center">

<p align="center">
<a href="https://github.com/akmalabdilah/Tutorial_Drat_2.git">Requirements</a> •
<a href="https://github.com/akmalabdilah/Tutorial_Drat_2.git">Informasi</a> •
<a href="https://github.com/akmalabdilah/Tutorial_Drat_2.git">Tutorial</a>
</p>
</div>

# Requirements
- [Dart](https://git-scm.com/download)

# Informasi Dart
Apa itu Dart?
<p>
Dart adalah bahasa pemrograman yang dikembangkan oleh Google. Dart didesain untuk membangun aplikasi lintas platform, termasuk aplikasi mobile untuk Android dan iOS, aplikasi web, dan juga aplikasi desktop. Dart memiliki sintaks yang mirip dengan bahasa pemrograman C dan JavaScript, sehingga relatif mudah dipelajari bagi para pengembang yang sudah memiliki pengalaman dengan bahasa-bahasa tersebut. Salah satu keunggulan Dart adalah fitur Just-in-Time (JIT) dan Ahead-of-Time (AOT) compilation yang memungkinkan aplikasi yang ditulis dengan Dart berjalan dengan performa tinggi. Dart juga dilengkapi dengan kerangka kerja Flutter yang populer untuk pengembangan aplikasi mobile dan UI yang kaya.
</p>

# Tutorial
- Pada saat pertama kali menggunakan Dart, perlu dilakukan penginstalan extension
di visual Studio Code. Jalankan perintah berikut:

```bash
> Dart
```


![Gambar 1](Screenshots/ss1.JPG)


- Setelah itu jalankan perintah Ctrl+Shift+P dan tulis Dart: New Project. untuk membuat repository 

- Untuk membuat file pilih yang bagian ke dua dan berilah nama sesuka kalian dan jika sudah di pindahkan ke halaman folder hapus isi yang ada di polder dan buat file baru di dalam polder tersebut.

<h1> Soal buatkan codingan fungsi validasi login dalam bahasa dart, dengan kualifikasi berikut:</h1>

- untuk user name
  - min 6 karakter.
- Untuk password 
  - min 6 karakter.
  - harus ada huruf besar.
  - harus ada character.
  - harus ada angka.
  - harus ada huruf kecil.

### ini adalah hasil runnya yang berhasil.

![Gambar 2](Screenshots/ss2.JPG)

-Diatas ini adalah gambar run apa bila tidak ada yang eror pas input data user name dan password ,dan yang di bawah ini adalah koding dartnya.

#### Dibawah ini adalah penjelasan kode dart dan kode dartnya.

<p>Sedikit penjelasan kode dart di bawah. 
Fungsi login() digunakan untuk memvalidasi login dengan melakukan beberapa pengecekan terhadap username dan password yang diinputkan oleh pengguna. Berikut adalah penjelasan singkat tentang setiap langkah validasi:

  Mengambil input username dan password dari pengguna menggunakan stdin.readLineS().

  Memeriksa panjang password. Jika panjangnya kurang dari 6 karakter, maka akan mencetak pesan error dan mengembalikan false yang menunjukkan login gagal.

  Memeriksa keberadaan huruf besar dalam password. Jika tidak ada huruf besar, maka akan mencetak pesan error dan mengembalikan false.

  Memeriksa keberadaan huruf kecil dalam password. Jika tidak ada huruf kecil, maka akan mencetak pesan error dan mengembalikan false.

  Memeriksa keberadaan angka atau karakter khusus dalam password. Jika tidak ada angka atau karakter khusus, maka akan mencetak pesan error dan mengembalikan false.

  Jika semua pengecekan berhasil, yaitu panjang password mencukupi dan terdapat huruf besar, huruf kecil, serta angka atau karakter khusus, maka fungsi akan mengembalikan true, menandakan login berhasil.

Pada main(), fungsi login() dipanggil untuk memvalidasi login. Jika hasilnya true, maka mencetak "Login berhasil", dan jika false, maka mencetak "Login gagal".</p>

```dart
import 'dart:io';

void main() {
  // Memanggil fungsi login
  bool isLoggedIn = login();

  if (isLoggedIn) {
    print("Login berhasil");
  } else {
    print("Login gagal");
  }
}

bool login() {
  print("=== Menu Login ===");

  stdout.write("Masukkan username: ");
  String username = stdin.readLineSync()!;

  stdout.write("Masukkan password: ");
  String password = stdin.readLineSync()!;

  // Memeriksa panjang password
  if (password.length < 6) {
    print("Eror: Password harus memiliki setidaknya 6 karakter");
    return false;
  }

  // Memeriksa keberadaan huruf besar
  if (!password.contains(RegExp(r'[A-Z]'))) {
    print("Eror: Password harus mengandung setidaknya satu huruf besar");
    return false;
  }

  // Memeriksa keberadaan huruf kecil
  if (!password.contains(RegExp(r'[a-z]'))) {
    print("Eror: Password harus mengandung setidaknya satu huruf kecil");
    return false;
  }

  // Memeriksa keberadaan angka atau karakter khusus
  if (!password.contains(RegExp(r'[0-9\W]'))) {
    print(
        "Eror: Password harus mengandung setidaknya satu angka atau karakter khusus");
    return false;
  }

  // Jika semua persyaratan terpenuhi, login berhasil
  return true;
}

```

- Dibawah adalah Gambar run yang eror apa bilah pas input data password tidak mengikuti aturan validasi yang dibuat Eror: Password harus memiliki setidaknya 6 karakter

![Gambar 4](Screenshots/ss4.JPG)

- Dibawah adalah Gambar run yang eror apa bilah pas input data password tidak mengikuti aturan validasi yang dibuat Eror: Password harus mengandung setidaknya satu huruf besar

![Gambar 3](Screenshots/ss3.JPG)

- Dibawah adalah Gambar run yang eror apa bilah pas input data password tidak mengikuti aturan validasi yang dibuat Eror: Password harus mengandung setidaknya satu huruf kecil

![Gambar 5](Screenshots/ss5.JPG)

- Dibawah adalah Gambar run yang eror apa bilah pas input data password tidak mengikuti aturan validasi yang dibuat Eror: Password harus mengandung setidaknya satu angka atau karakter khusus

![Gambar 6](Screenshots/ss6.JPG)

- Untuk kode dartnya sama sama yang di atas karna 4 gambar eror barusan hanya untuk gambaran saja apa bila eror memasukan password karna tidak mengikuti validasi yang berlaku, Sekian dan.


- Selesai
