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
