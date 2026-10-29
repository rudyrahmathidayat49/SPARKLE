# SPARKLE TRACK – TSSO v4.3.13

## Menjalankan lokal
- Buka `index.html` untuk tampilan utama.
- Untuk pemindaian QR kamera, jalankan melalui situs HTTPS (misalnya GitHub Pages) dan buka dengan Chrome Android. Membuka HTML langsung dari File Manager biasanya tidak memberi izin kamera.

## Deploy ke GitHub Pages
1. Ekstrak ZIP ini.
2. Unggah **isi folder hasil ekstrak** ke repository GitHub (bukan folder pembungkus). Pastikan `index.html` terlihat langsung di halaman utama repository.
3. Buka **Settings → Pages**.
4. Pada bagian Build and deployment, pilih **Deploy from a branch**, branch `main`, folder `/(root)`, lalu Save.
5. Tunggu URL HTTPS GitHub Pages muncul, lalu buka URL tersebut di Chrome Android.
6. Login sebagai Cleaning Service, pilih fitur checklist, izinkan akses kamera, lalu tekan Scan QR Kamera.

## Catatan prototype
- Data disimpan di `localStorage` browser, bukan database server; data antarperangkat tidak otomatis tersinkron.
- Pemindaian kamera membutuhkan browser yang mendukung `BarcodeDetector` dan izin kamera.
- QR lokasi demo disediakan di folder `qr/`. Gunakan QR yang berasal dari versi prototype yang sama.
- Ini prototype untuk pengujian, belum merupakan sistem produksi dengan autentikasi dan penyimpanan server.


## v4.3.14 — QR Master Lokasi Prototype
- QR pada menu Master Lokasi dibuat dinamis berdasarkan nama lokasi.
- QR berisi URL website dengan parameter `area`, sehingga nama lokasi baru dapat dikenali saat dibuka pada perangkat lain.
- Gambar QR dibuat melalui layanan QR online; perangkat perlu terhubung ke internet saat memuat QR.
- Ini tetap prototype statis: data master lokasi tidak menjadi database bersama. QR URL membawa nama lokasi dan akan menambahkan nama itu ke penyimpanan lokal perangkat yang membukanya.
- Gunakan URL GitHub Pages yang sebenarnya saat website sudah diterbitkan; QR dibuat berdasarkan alamat website yang sedang dibuka.


## v4.3.15 — Matriks Bulanan berdasarkan peran
- Admin dan Supervisor melihat matriks bulanan seluruh petugas Cleaning Service.
- Cleaning Service hanya melihat matriks dan rincian pekerjaan akun yang sedang login.
- Menu Supervisor menampilkan label Matriks Bulanan.
- Ini pembatasan tampilan prototype berbasis browser; bukan keamanan backend untuk operasional nyata.


## v4.3.16 — Perbaikan Matriks Bulanan
- Halaman Matriks Bulanan kini benar-benar dirender untuk setiap role.
- Admin dan Supervisor melihat seluruh petugas.
- Cleaning Service hanya melihat catatan akun yang sedang login.
- Perbaikan diuji untuk struktur ZIP dan pemeriksaan sintaks inline JavaScript; belum diuji di browser langsung.


## v4.3.17 — Matriks Bulanan Modern & Filter Fix
- Tampilan matriks diperbarui: ringkasan KPI, legenda status, sel warna, tabel sticky, dan layout responsif.
- Filter periode dan lokasi dipakai untuk ringkasan, matriks, serta rincian. Admin/Supervisor juga dapat memfilter PIC; ekspor Excel mengikuti filter PIC.
- Status harian dibedakan: terverifikasi, menunggu, ditolak, atau tanpa catatan.
- Seluruh fitur lain dipertahankan dari v4.3.16.
- Pemeriksaan: struktur ZIP dan sintaks JavaScript diperiksa. Belum diuji langsung di browser/GitHub Pages. Data masih menggunakan localStorage prototype; filter role di sisi klien bukan kontrol keamanan backend.
