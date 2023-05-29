

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

