# Hihafest - Concert Ticket Platform

Hihafest adalah platform web komprehensif untuk penjualan tiket konser secara online. Proyek ini terdiri dari aplikasi frontend untuk pelanggan dan admin, serta backend yang mengelola transaksi, inventaris tiket, dan autentikasi.

## Frontend
https://github.com/daffayuza/FE-Hiha-Fest.git

## Backend
https://github.com/daffayuza/BE-Hiha-Fest.git


## Fitur Utama

### 🎫 Customer Facing (Publik)
- **Katalog Event:** Lihat daftar konser yang tersedia.
- **Guest Checkout:** Beli tiket tanpa perlu registrasi akun.
- **Integrasi Pembayaran:** Terintegrasi dengan Midtrans (mendukung VA, e-Wallet, dll).
- **E-Ticket Otomatis:** Tiket elektronik lengkap dengan QR code/Barcode dikirimkan otomatis ke email pembeli setelah pembayaran sukses.
- **Order Lookup / Cek Tiket:** Lacak dan periksa status pesanan menggunakan alamat email atau nomor order.

### 🛡️ Admin CMS
- **Dashboard Ringkasan:** Pantau secara real-time total penjualan, sisa kuota, dan pendapatan per event.
- **Manajemen Event:** CRUD (Create, Read, Update, Delete) informasi event dan kategori tiket beserta harga dan kuota.
- **Manajemen Transaksi:** Lihat rincian seluruh pembelian tiket dari pelanggan.
- **Autentikasi & Keamanan:** Rute web yang dilindungi dengan token untuk menjamin hanya admin yang berhak mengakses dasbor dan manajemen konten.

## Tech Stack

- **Frontend:** React, TypeScript, Vite.
- **Backend:** Node.js, Express, Prisma ORM, JSON Web Token (JWT).
- **Database:** MySQL.
- **Pihak Ketiga (Third-party):** 
  - [Midtrans](https://midtrans.com/) (Payment Gateway)
  - Nodemailer (Pengiriman E-Ticket via Email)


*Platform ini dibangun secara iteratif untuk memberikan kemudahan bagi pembeli dalam mendapatkan tiket dan memberi wewenang penuh kepada manajemen acara melalui admin interface.*
