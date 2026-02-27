# 🏘️ Portal Warga

![Version](https://img.shields.io/badge/version-2.0.7-blue.svg)
![Platform](https://img.shields.io/badge/platform-Google_Apps_Script-0F9D58.svg)
![Database](https://img.shields.io/badge/database-Google_Sheets-34A853.svg)
![Frontend](https://img.shields.io/badge/frontend-Bootstrap_5-7952B3.svg)

Portal Warga adalah aplikasi berbasis web (Single Page Application/SPA) yang dirancang untuk mendigitalisasi dan mempermudah tata kelola lingkungan perumahan (RT/RW/Cluster). Dibangun sepenuhnya di atas ekosistem **Google Workspace (Google Apps Script & Google Sheets)**, menjadikannya sistem yang *serverless*, gratis (tanpa biaya hosting), dan mudah dikelola (Scalable & Maintainable).

---

## ✨ Fitur Utama

### 👥 Untuk Warga (User)
* **Dashboard Cerdas**: Ringkasan informasi, tagihan aktif, dan notifikasi.
* **Manajemen Tagihan (MyBill)**: Pengecekan tagihan Iuran Pengelolaan Lingkungan (IPL) & Air Bersih secara transparan.
* **Pembayaran Terintegrasi**: Fitur unggah bukti transfer langsung dari aplikasi.
* **Informasi & Berita (Feeds)**: Akses ke pengumuman RT, kegiatan warga, dan laporan keamanan.
* **Buku Kontak**: Direktori kontak antar warga dan pengurus lingkungan.
* **Kontak Darurat**: Akses cepat 24 jam ke nomor-nomor penting (Damkar, Polisi, RS, Security).

### 🛡️ Untuk Pengurus (Admin)
* **Verifikasi Pembayaran**: Halaman khusus untuk memvalidasi atau menolak bukti pembayaran warga.
* **Monitoring Tunggakan**: Rekap otomatis warga yang belum membayar tagihan, dilengkapi fitur pengingat via WhatsApp (Auto-Generate WA Message).
* **Laporan Keuangan**: Transparansi kas masuk (IPL/Air/Donasi) dan kas keluar (Operasional).
* **Input Meteran Air**: Fitur pencatatan meteran air bulanan per rumah.

---

## 🛠️ Arsitektur & Teknologi

Aplikasi ini dibangun dengan prinsip **DRY (Don't Repeat Yourself)** dan **Separation of Concerns**, memisahkan antara *Data Layer*, *Logic Layer*, dan *View Layer*.

* **Backend**: Google Apps Script (ES5/ES6).
* **Database**: Google Sheets (Relational-like mapping).
* **Frontend**: HTML5, CSS3, Vanilla JavaScript.
* **UI Framework**: Bootstrap 5.3 & Google Material Icons.
* **State Management**: Caching di memori lokal klien (`Script.html`) dan caching di memori server (`CacheService` GAS) untuk performa super cepat.

---

## 📂 Struktur Proyek

```text
├── Code.gs                   # Backend API, Database Queries, Server-side routing
├── index.html                # Main SPA Wrapper & Shell
├── Script.html               # Global Frontend Logic, State Management, Router
├── Style.html                # Global CSS & Custom Animations
├── CompBottomNav.html        # UI Component: Bottom Navigation Bar
├── PageHome.html             # View: Dashboard
├── PageInvoice.html          # View: Template Tagihan (Reusable)
├── PageVerification.html     # View: Admin List Verifikasi & Tunggakan
├── PageVerificationDetail.html # View: Admin Detail Validasi Pembayaran
└── ... (Halaman lainnya)
