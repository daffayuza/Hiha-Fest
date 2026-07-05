# Hihafest - Concert Ticket Platform

Hihafest adalah platform web komprehensif untuk penjualan tiket konser secara online. Proyek ini terdiri dari aplikasi frontend untuk pelanggan dan admin, serta backend yang mengelola transaksi, inventaris tiket, dan autentikasi.

## Frontend
https://github.com/daffayuza/FE-Hiha-Fest.git

## Backend
[https://github.com/username/concert-ticket-backend](https://github.com/daffayuza/BE-Hiha-Fest.git)

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
- **Manajemen Profil:** Dukungan pembaruan identitas admin, termasuk kemampuan mengunggah foto profil.

## Struktur Direktori

Project ini menggunakan arsitektur monorepo sederhana yang membedakan aplikasi klien dan layanan server:
- `/frontend` - Aplikasi klien (React, TypeScript, Tailwind) untuk pengunjung maupun admin.
- `/backend` - Layanan API, routing, konfigurasi database (Node.js, Express, Prisma).
- `prd.md` - Dokumen Product Requirements berisi spesifikasi fitur secara menyeluruh.

## Tech Stack

- **Frontend:** React, TypeScript, Vite, Tailwind CSS.
- **Backend:** Node.js, Express, Prisma ORM, JSON Web Token (JWT).
- **Database:** MySQL.
- **Pihak Ketiga (Third-party):** 
  - [Midtrans](https://midtrans.com/) (Payment Gateway)
  - Nodemailer (Pengiriman E-Ticket via Email)

## Cara Menjalankan Project (Local Development)

### Persyaratan Awal
Pastikan komputer Anda sudah terinstal **Node.js** dan memiliki akses ke instance layanan **MySQL**.

### 1. Setup Backend
1. Masuk ke direktori backend: 
   ```bash
   cd backend
   ```
2. Install dependensi: 
   ```bash
   npm install
   ```
3. Set environment variable: Buat file `.env` di dalam folder `backend` yang memuat konfigurasi koneksi database MySQL (`DATABASE_URL`), kredensial Midtrans Server Key, Secret Key untuk JWT, dll.
4. Lakukan Push Database Schema menggunakan Prisma: 
   ```bash
   npx prisma db push
   ```
5. Jalankan backend server: 
   ```bash
   npm run dev
   ```

### 2. Setup Frontend
1. Buka tab terminal baru dan arahkan ke direktori frontend: 
   ```bash
   cd frontend
   ```
2. Install dependensi: 
   ```bash
   npm install
   ```
3. Set environment variable: Buat file `.env` dan simpan variabel wajib seperti URL backend (`VITE_API_URL=http://localhost:5000/api`) dan Client Key midtrans (`VITE_MIDTRANS_CLIENT_KEY`).
4. Jalankan development server frontend: 
   ```bash
   npm run dev
   ```
5. Buka `http://localhost:5173` di browser Anda untuk menjelajahi platform Hihafest local.

---

*Platform ini dibangun secara iteratif untuk memberikan kemudahan bagi pembeli dalam mendapatkan tiket dan memberi wewenang penuh kepada manajemen acara melalui admin interface.*
