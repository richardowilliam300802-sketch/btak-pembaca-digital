PEMBACA DIGITAL — BANGSAWAN TIDAK AKAN KAYA TANPA LEPAS JUBAH
Karya: Andre W. Koreh

ISI PAKET
- public/index.html : tampilan pembaca buku dengan efek membalik halaman
- public/book.pdf : PDF asli buku (479 halaman)
- public/toc.json : daftar isi yang diambil dari bookmark PDF
- public/assets/cover.png : gambar sampul asli

FITUR
- Efek membalik halaman (page flip)
- Daftar isi yang dapat diklik
- Navigasi halaman awal/akhir dan nomor halaman
- Zoom dan layar penuh
- Tata letak responsif untuk HP dan komputer

PENTING SEBELUM ONLINE
PDF berukuran sekitar 48 MB. Beberapa layanan hosting membatasi ukuran satu file saat unggah. Karena itu, jangan menghapus atau mengganti book.pdf. Jika memakai Cloudflare Pages dan unggahan menolak file PDF karena batas ukuran, simpan book.pdf di Cloudflare R2 atau layanan penyimpanan file yang mendukung file besar, lalu ubah konstanta PDF_URL di public/index.html menjadi alamat publik file PDF tersebut. Pastikan file PDF dapat diakses publik dan CORS mengizinkan situs pembaca.

CARA MENCOBA DI KOMPUTER
1. Jalankan server lokal dari folder public (jangan buka index.html dengan klik ganda karena PDF.js membutuhkan HTTP).
2. Jika Python tersedia, buka terminal pada folder public lalu jalankan:
   python -m http.server 8000
3. Buka http://localhost:8000

CARA ONLINE
Unggah isi folder public ke layanan hosting situs statis. Contohnya Cloudflare Pages. Jika file PDF 48 MB tidak diterima oleh uploader, gunakan Cloudflare R2 untuk book.pdf dan ganti PDF_URL di index.html ke URL publik R2.

CATATAN
Situs ini menggunakan PDF.js dan PageFlip melalui CDN. Koneksi internet diperlukan saat pertama kali membuka situs. File PDF asli tidak diubah.
