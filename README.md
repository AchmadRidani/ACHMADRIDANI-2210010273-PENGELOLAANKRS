
## Aplikasi Pengelolaan KRS (Kartu Rencana Studi)

**Tugas UAS**

Nama: Achmad Ridani  
NPM: 2210010273

---

### 1. Deskripsi Program

Aplikasi ini adalah aplikasi GUI berbasis Java untuk mengelola data KRS mahasiswa. Pengguna dapat menambahkan, mengubah, menghapus, serta mencetak data mahasiswa dan KRS. Aplikasi ini menggunakan database MySQL sebagai tempat penyimpanan data.

### 2. Komponen GUI

Aplikasi ini menggunakan komponen GUI berikut:

- **JFrame**: Sebagai kerangka utama aplikasi.
- **JPanel**: Sebagai wadah komponen GUI.
- **JLabel**: Label teks untuk elemen input.
- **JTextField**: Input teks untuk data mahasiswa dan KRS.
- **JComboBox**: Pilihan dropdown untuk NPM mahasiswa.
- **JButton**: Tombol untuk aksi seperti Tambah, Edit, Hapus, dan Cetak.
- **JTable**: Tabel untuk menampilkan data mahasiswa dan KRS.
- **JOptionPane**: Dialog untuk notifikasi atau peringatan.

### 3. Fitur Program

- **Data Mahasiswa**
  - Tambah mahasiswa baru.
  - Edit data mahasiswa.
  - Hapus data mahasiswa.
  - Tampilkan data mahasiswa dalam tabel.

- **Data KRS**
  - Tambah data KRS.
  - Edit data KRS.
  - Hapus data KRS.
  - Tampilkan data KRS dalam tabel.

- **Cetak Data**
  - Cetak data mahasiswa dan KRS langsung dari JTable.

### 4. Struktur Database

**Database:** `pengelolaan_krs`  
Terdapat dua tabel utama:

- **Tabel `mahasiswa`**
  - `npm` (VARCHAR, Primary Key)
  - `nama` (VARCHAR)
  - `tanggal_lahir` (DATE)
  - `jurusan` (VARCHAR)
  - `no_telepon` (VARCHAR)
  - `email` (VARCHAR)

- **Tabel `pengambilan_krs`**
  - `id_pengambilan` (INT, Primary Key, Auto Increment)
  - `npm` (VARCHAR, Foreign Key ke tabel mahasiswa)
  - `kode_mata_kuliah` (VARCHAR)
  - `nama_mata_kuliah` (VARCHAR)
  - `sks` (INT)
  - `semester` (VARCHAR)
  - `tahun_akademik` (INT)
  - `nama_dosen` (VARCHAR)

### 5. Cara Menjalankan Program

1. Pastikan server database MySQL berjalan.
2. Buat database `pengelolaan_krs` dan tabel sesuai struktur di atas.
3. Atur koneksi database di file program pada bagian berikut:
   ```java
   String url = "jdbc:mysql://localhost:3306/pengelolaan_krs";
   String user = "root"; // Ganti sesuai username MySQL Anda
   String password = ""; // Ganti sesuai password MySQL Anda
   ```
4. Jalankan file `PengelolaanKRS.java` di IDE seperti NetBeans.

### 6. Indikator Penilaian

| No | Komponen                          | Persentase |
|----|-----------------------------------|------------|
| 1  | Terdapat minimal 2 tabel master   | 30%        |
| 2  | Terdapat minimal 1 tabel transaksi | 20%       |
| 3  | Terdapat minimal 2 laporan        | 30%        |
| 4  | Kesesuaian User Interface (layout dan komponen) | 20% |
| **Total** |                           | **100%**   |

### 7. Contoh Tampilan Program



Aplikasi ini dirancang untuk mempermudah proses pengelolaan KRS dengan antarmuka yang sederhana dan mudah digunakan.
