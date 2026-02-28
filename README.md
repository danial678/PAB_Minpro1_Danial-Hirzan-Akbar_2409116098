# Aplikasi Konservasi Penyu

Aplikasi Flutter untuk mencatat dan mengelola data konservasi penyu.

<img width="1302" height="885" alt="Cuplikan layar 2026-02-28 143714" src="https://github.com/user-attachments/assets/f5f1f045-afbd-46a7-b019-6c82e705d5b7" />

## Deskripsi Aplikasi

Aplikasi Konservasi Penyu adalah aplikasi mobile yang dibuat menggunakan **Flutter** dan **Dart**. Aplikasi ini dirancang untuk membantu mencatat data sarang penyu di pantai-pantai konservasi, mulai dari penemuan sarang, pencatatan jumlah telur, kondisi telur, hingga pemantauan proses konservasi.

Data disimpan secara **sementara menggunakan List** (state management), sehingga data akan hilang ketika aplikasi ditutup. Aplikasi ini cocok untuk pembelajaran dasar Flutter dan pengenalan konsep CRUD (Create, Read, Update, Delete).



## Fitur Aplikasi

| Fitur | Deskripsi |
|-------|-----------|
| **Create (Tambah Data)** | Menambahkan data sarang penyu baru melalui dialog form dengan 5 input field |
| **Read (Tampilkan Data)** | Menampilkan daftar sarang penyu dalam bentuk ListView dengan informasi lengkap |
| **Update (Edit Data)** | Mengubah data sarang yang sudah tersimpan melalui dialog edit |
| **Delete (Hapus Data)** | Menghapus data sarang dari daftar dengan konfirmasi dialog terlebih dahulu |
| **Validasi Input** | Validasi sederhana untuk memastikan field wajib diisi sebelum menyimpan |
| **Notifikasi** | Menampilkan Snackbar saat berhasil menambah, mengedit, atau menghapus data |

<img width="109" height="62" alt="Cuplikan layar 2026-02-28 143732" src="https://github.com/user-attachments/assets/f5c1154d-3677-407e-a594-03b77e825c4a" />

## Widget yang Digunakan

### Layout & Struktur
| Widget | Fungsi |
|--------|--------|
| `MaterialApp` | Root aplikasi yang mengatur tema dan konfigurasi utama |
| `Scaffold` | Struktur dasar halaman yang menyediakan AppBar, Body, dan FloatingActionButton |
| `AppBar` | Header aplikasi dengan judul dan ikon |
| `Center` | Menempatkan widget di tengah layar (untuk empty state) |

### Input & Form
| Widget | Fungsi |
|--------|--------|
| `TextField` | Input teks untuk menerima data dari pengguna (minimal 3 TextField) |
| `TextEditingController` | Mengontrol dan membaca nilai dari TextField |
| `AlertDialog` | Menampilkan dialog popup untuk form input dan konfirmasi hapus |
| `SingleChildScrollView` | Membuat konten dialog dapat di-scroll jika terlalu panjang |
| `InputDecoration` | Menambahkan label, hint, dan styling pada TextField |

### Tampilan Data
| Widget | Fungsi |
|--------|--------|
| `ListView.builder` | Menampilkan list data secara efisien dan dinamis |
| `Card` | Container untuk setiap item dengan efek bayangan (elevation) |
| `ListTile` | Layout item dengan leading (icon), title, subtitle, dan trailing (tombol) |
| `Icon` | Menampilkan ikon penyu, lokasi, dan aksi |
| `IconButton` | Tombol dengan ikon untuk aksi edit dan delete |

### State Management
| Widget/Method | Fungsi |
|---------------|--------|
| `StatefulWidget` | Widget yang memiliki state yang dapat berubah |
| `setState()` | Memperbarui tampilan UI ketika data berubah |
| `List&lt;TurtleNest&gt;` | Menyimpan data sarang penyu secara sementara |

## Minimal 3 TextField

Aplikasi ini memiliki **5 TextField** yang wajib diisi:

1. **Lokasi Sarang** - Tempat ditemukannya sarang penyu
2. **Jenis Penyu** - Spesies penyu (contoh: Penyu Hijau, Penyu Sisik)
3. **Jumlah Telur** - Jumlah telur dalam sarang (input angka)
4. **Kondisi** - Kondisi telur (Baik/Rusak/Dicuri)
5. **Tanggal Ditemukan** - Tanggal penemuan sarang

<img width="375" height="571" alt="image" src="https://github.com/user-attachments/assets/e70f2efe-008b-4ca6-bd4c-8163c381e331" />
