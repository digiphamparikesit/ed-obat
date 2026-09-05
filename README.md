# Aplikasi Laporan Obat/BMHP Expired — Farmasi RSUD

Aplikasi berbasis web untuk pelaporan retur obat/BMHP expired menggunakan **Supabase** sebagai database dan **GitHub Pages** sebagai hosting.

## Fitur
- Input laporan retur dengan autocomplete petugas dan barang.
- Riwayat retur per unit dengan edit jumlah, kirim ke gudang, dan batalkan.
- Dashboard monitoring (dalam pengembangan).
- Status ED otomatis (EXPIRED, NEAR ED3, NEAR ED6, AMAN).

## Teknologi
- HTML + CSS + JavaScript murni (tanpa framework).
- Supabase (PostgreSQL) sebagai database.
- GitHub Pages untuk hosting.

## Instalasi & Deploy

### 1. Buat proyek Supabase
- Daftar di [supabase.com](https://supabase.com).
- Buat proyek baru.
- Jalankan skrip SQL di `schema.sql` di SQL Editor.

### 2. Konfigurasi
- Buka `config.js` dan ganti `SUPABASE_URL` dan `SUPABASE_ANON_KEY` dengan data dari proyek Supabase Anda.

### 3. Deploy ke GitHub Pages
- Buat repository GitHub.
- Upload semua file (`index.html`, `config.js`, `style.css`, dll).
- Aktifkan GitHub Pages di Settings > Pages > Branch `main`.

### 4. Akses aplikasi
- Buka URL GitHub Pages Anda.

## Struktur Database
- `unit` – daftar unit/gudang.
- `daftar_petugas` – daftar petugas.
- `data_barang` – master barang.
- `master_data` – laporan retur.
- `arsip_master_data` – arsip otomatis.
- `app_settings` – konfigurasi (password dashboard).

## Password Dashboard
Default: `gudangfarmasi2026`  
Bisa diubah di tabel `app_settings` pada baris `dashboard_password`.

## Lisensi
Untuk penggunaan internal RSUD.
