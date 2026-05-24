# 🧾 Najwa Sakti Retail System – Point of Sale (POS)

Selamat datang di aplikasi Najwa Sakti Retail System, sebuah sistem Point of Sale (POS) modern untuk toko retail skala kecil hingga menengah. Aplikasi ini dirancang untuk memudahkan pengelolaan penjualan, pembelian, stok barang, piutang, hutang, shift kasir, dan laporan keuangan.

---

## 📋 Daftar Isi

- [Persyaratan Sistem](#-persyaratan-sistem)
- [Instalasi](#-instalasi)
- [Aktivasi Lisensi](#-aktivasi-lisensi)
- [Login Pertama Kali](#-login-pertama-kali)
- [Antarmuka Utama](#-antarmuka-utama)
- [Panduan Penggunaan Cepat](#-panduan-penggunaan-cepat)
  - [1. Input Barang & Master Data](#1-input-barang--master-data)
  - [2. Transaksi Penjualan](#2-transaksi-penjualan)
  - [3. Transaksi Pembelian](#3-transaksi-pembelian)
  - [4. Manajemen Shift & Laci Kasir](#4-manajemen-shift--laci-kasir)
  - [5. Laporan Keuangan](#5-laporan-keuangan)
- [Backup & Restore Database](#-backup--restore-database)
- [Pembaruan Aplikasi](#-pembaruan-aplikasi)
- [Pemecahan Masalah Umum](#-pemecahan-masalah-umum)
- [Dukungan Teknis](#-dukungan-teknis)

---

## 💻 Persyaratan Sistem

- **Sistem Operasi**: Windows 10 / 11 (64-bit)
- **Processor**: Intel Core i3 atau setara (minimal 2.0 GHz)
- **RAM**: 4 GB (disarankan 8 GB)
- **Penyimpanan**: 500 MB ruang kosong (ditambah ruang untuk database)
- **Printer**: Printer thermal (58mm/80mm) atau printer biasa (untuk laporan)
- **Koneksi Internet**: Diperlukan untuk aktivasi awal dan pengecekan update (opsional)

---

## 📦 Instalasi

1. **Unduh installer** `NajwaSaktiPOS_Setup.exe` dari media distribusi (USB, email, atau website).
2. **Jalankan installer** sebagai Administrator (klik kanan → *Run as administrator*).
3. Ikuti wizard instalasi:
   - Pilih folder tujuan (default `C:\Program Files\Najwa Sakti Retail\POS`)
   - Pilih shortcut yang ingin dibuat (Desktop, Start Menu)
   - Klik **Install** dan tunggu hingga selesai.
4. Setelah instalasi selesai, centang opsi **"Jalankan Najwa Sakti POS"** lalu klik **Finish**.

> ⚠️ **Catatan**: Jangan hapus folder `themes` atau `icons` di dalam folder instalasi, karena diperlukan untuk tampilan aplikasi.

---

## 🔑 Aktivasi Lisensi


1. **Jalankan aplikasi**. Akan muncul dialog **Aktivasi Lisensi**.

2. **Copy Machine ID** yang ditampilkan (teks panjang berwarna abu-abu).  
   Contoh: `a1b2c3d4e5f6...`

3. **Kirim Machine ID tersebut** kepada pengembang melalui email atau WhatsApp untuk mendapatkan kunci lisensi.

4. **Masukkan kunci lisensi** yang Anda terima ke dalam kolom "Kunci Lisensi", lalu klik **✅ Aktivasi**.

5. Jika berhasil, aplikasi akan menampilkan pesan sukses dan Anda bisa masuk ke halaman login.

### 🎫 Jenis Lisensi

| Jenis | Keterangan |
|-------|-------------|
| **Trial** | Berlaku 30 hari, hanya bisa digunakan **sekali** per komputer. Tidak dapat diulang. |
| **Full** | Permanen, tidak kedaluwarsa. Mendapat pembaruan gratis selama periode yang ditentukan. |

> ℹ️ Lisensi Full bersifat **perpetual**, tidak perlu perpanjangan tahunan kecuali ada kebijakan khusus.

---

## 🔐 Login Pertama Kali

Setelah aktivasi berhasil, Anda akan masuk ke halaman **Login**.

- **Username default admin**: `admin`
- **Password default**: `admin123`

> 🔐 Segera ganti password setelah login pertama melalui menu **Pengaturan > Data User**.

Untuk user **kasir**:
- **Username**: `kasir`
- **Password**: `kasir123`
- Role kasir hanya bisa mengakses modul **Penjualan** dan shift kasir.

---

## 🖥️ Antarmuka Utama

Setelah login, Anda akan melihat:

- **Title bar** (atas): judul aplikasi, logo, tombol minimize/maximize/close.
- **Toolbar**: menu utama (Menu Utama, Master Data, Pembelian, Penjualan, Persediaan, Akuntansi, Laporan, Pengaturan).
- **Stacked widget**: area konten dinamis sesuai menu yang dipilih.
- **Status bar** (bawah): menampilkan user aktif, tema, status shift, dan info lisensi.

---

## 🚀 Panduan Penggunaan Cepat

### 1. Input Barang & Master Data
- Buka menu **Master Data → Daftar Barang**.
- Klik **+ Item Baru**, isi:
  - **Kode Barang** (otomatis)
  - **Nama Barang**
  - **Kategori** (bisa tambah baru dengan tombol "+")
  - **Stok Minimum** (opsional, untuk notifikasi stok menipis)
- Masukkan satuan dan harga pada tab **Satuan & Harga**:
  - Satuan dasar (misal Pcs) dengan faktor konversi 1.
  - Satuan besar (misal Dus) dengan faktor konversi >1 (misal 1 dus = 20 kg → faktor 20).
  - Harga beli dan jual diisi minimal pada satuan besar, lalu klik **"Hitung Harga Satuan Dasar"** untuk mengisi otomatis.
- Klik **Simpan**.

> 📌 **Tips**: Input data suplier dan pelanggan juga bisa dilakukan di menu Master Data.

---

### 2. Transaksi Penjualan
- Buka menu **Penjualan → Daftar Penjualan** lalu klik **+ Tambah Penjualan**.
- Pilih **Pelanggan** (bisa dikosongkan = UMUM).
- **Tambah barang** dengan cara:
  - Ketik jumlah di kolom "Jumlah".
  - Ketik nama barang di kolom "Nama Barang" (akan muncul saran otomatis).
  - Tekan **Enter** atau klik tombol tambah.
- Ulangi untuk barang lain. Bisa edit langsung jumlah di tabel.
- Jika stok tidak mencukupi, akan muncul peringatan.
- Masukkan **Diskon** (Rp) dan **Biaya Lain** jika ada.
- Klik **💳 Bayar** → masukkan jumlah uang yang dibayar → **Simpan Pembayaran**.
- Akan muncul dialog cetak nota (pilih **Yes** untuk cetak ke printer thermal).

> 💡 **Shortcut**: Tekan `Ctrl + Enter` untuk langsung membuka dialog pembayaran.

---

### 3. Transaksi Pembelian
- Buka menu **Pembelian → Daftar Pembelian** → **+ Tambah Pembelian**.
- Pilih **Supplier**, lalu tambahkan barang seperti pada penjualan.
- Isi **Diskon** dan **Tunai**.
- Jika tunai > expected cash shift, akan muncul peringatan. Anda harus melakukan Cash In dari kas besar terlebih dahulu atau mengurangi pembelian tunai.
- Klik **Simpan**.

> ⚠️ Pembelian tunai akan mengurangi expected cash shift dan dicatat sebagai cash out.

---

### 4. Manajemen Shift & Laci Kasir
Shift berfungsi untuk mencatat uang awal, transaksi tunai, cash in/out, dan selisih akhir.

- **Buka Shift** (status bar) – isi uang awal laci (default 0).
- Selama shift aktif, setiap transaksi penjualan tunai akan menambah **expected cash**, sedangkan pembelian tunai akan menguranginya.
- **Cash In/Out** (tombol di status bar):
  - `cash_in_from_big_cash` – ambil uang dari kas besar ke laci (tidak mempengaruhi jurnal).
  - `cash_in_from_other` – setoran dari luar (pembayaran piutang, modal) → mempengaruhi jurnal.
  - `cash_out` – ambil uang untuk keperluan operasional → debit beban, kredit kas.
- **Tutup Shift** – masukkan jumlah uang fisik di laci, selisih akan dihitung dan dicetak laporan.
- Laporan shift bisa dilihat di menu **Laporan → Shift**.

---

### 5. Laporan Keuangan
Aplikasi menyediakan berbagai laporan:

| Laporan | Deskripsi |
|---------|------------|
| Neraca Saldo | Daftar saldo semua akun per tanggal |
| Laba Rugi | Pendapatan, HPP, beban, laba bersih per periode |
| Neraca | Aset, kewajiban, ekuitas pada tanggal tertentu |
| Hutang / Piutang | Rincian hutang/piutang per supplier/pelanggan |
| Pembelian / Penjualan | Rekap atau detail transaksi |
| Aging Hutang / Piutang | Pengelompokan umur hutang/piutang (0-30,31-60,61-90,>90) |
| Arus Kas | Kas masuk dan keluar berdasarkan jurnal |
| Shift | Laporan shift kasir (buka/tutup, selisih) |

> 📌 Setiap laporan bisa difilter berdasarkan periode dan dicetak ke PDF.

---

## 💾 Backup & Restore Database

- Buka menu **Pengaturan → Database**.
- **Backup Manual**:
  - Pilih folder tujuan.
  - Klik **Backup Sekarang** → file `.db` akan disimpan.
- **Restore Database**:
  - Pilih file backup `.db`.
  - Konfirmasi restore (aplikasi akan otomatis ditutup setelah restore).
- **Backup Otomatis**:
  - Aktifkan, pilih interval (6 jam, 12 jam, setiap hari, dll).
  - Pilih folder penyimpanan.
  - Sistem akan melakukan backup sesuai jadwal.

> ⚠️ Selalu backup sebelum melakukan update besar atau perbaikan data.

---

## 🔄 Pembaruan Aplikasi

- Aplikasi akan **mengecek update secara otomatis** setiap 24 jam (saat startup).
- Jika ada versi baru, muncul dialog dengan daftar perubahan dan link download.
- **Update manual**: Klik tombol **🔄 Cek Update** di toolbar.
- **Proses update**:
  1. Unduh installer versi baru dari link yang disediakan.
  2. Jalankan installer baru di atas instalasi lama (tidak perlu uninstall).
  3. Database dan semua data akan tetap utuh.

---

## ❗ Pemecahan Masalah Umum

| Masalah | Solusi |
|---------|--------|
| **Aplikasi tidak bisa dijalankan** | Pastikan file `themes` dan `icons` ada di folder yang sama dengan `.exe`. |
| **Error "No module named 'PyQt5'"** | Instal ulang aplikasi atau pastikan virtual environment tidak digunakan. |
| **Tidak bisa aktivasi lisensi** | Periksa koneksi internet (untuk NTP) dan pastikan Machine ID yang dikirim benar. |
| **Shift tidak bisa ditutup** | Pastikan tidak ada transaksi yang belum selesai. Tutup semua form transaksi. |
| **Printer tidak merespon** | Cek koneksi printer, pastikan driver terinstal. Di pengaturan Mini Printer, pilih printer yang benar. |
| **Laci kasir tidak terbuka** | Coba kode drawer lain di pengaturan Mini Printer → Laci Kasir. |
| **Database corrupt** | Restore dari backup terakhir. Jika tidak ada, hubungi dukungan teknis. |

---

## 📞 Dukungan Teknis

Jika Anda mengalami kendala atau ingin membeli lisensi full, hubungi:

- **Email**: gramaxon3@gmail.com
- **WhatsApp**: 62895428910895

Sertakan **Machine ID** dan **deskripsi masalah** untuk mempercepat penanganan.

---

## 📄 Lisensi

Aplikasi ini dilindungi hak cipta. Penggunaan tidak sah, penyalinan, atau rekayasa balik dilarang. Lisensi lengkap tersedia dalam file `license.txt` yang disertakan dalam installer.

---

© 2025 Najwa Sakti Retail. Hak cipta dilindungi undang-undang.
