# APEM — Static Demo untuk Vercel

Versi statis APEM yang menggunakan logo baru dan tema warna navy, biru, kuning, serta oranye. Referensi dashboard diterapkan secara ringan pada kartu ringkasan akun; alur utama tetap berfokus pada marketplace.

## Deploy ke Vercel

1. Ekstrak ZIP ini ke folder di komputer.
2. Buka https://vercel.com dan masuk/daftar.
3. Pilih **Add New → Project**.
4. Hubungkan repository GitHub yang berisi isi folder ini (disarankan), atau gunakan Vercel CLI.
5. Saat konfigurasi project, pilih **Framework Preset: Other**.
6. **Root Directory**: folder yang berisi `index.html` dan `vercel.json`.
7. **Build Command**: kosongkan / Override lalu nonaktifkan.
8. **Output Directory**: `.` (titik).
9. **Install Command**: kosongkan / nonaktifkan.
10. Klik **Deploy**.

### Cara paling mudah lewat GitHub
- Buat repository baru di GitHub.
- Upload/commit `index.html`, folder `assets/`, `vercel.json`, dan `README.md` (bisa melalui GitHub web atau Git).
- Di Vercel pilih **Add New → Project**, import repository itu, lalu ikuti konfigurasi di atas.
- Setelah deploy, Vercel memberi URL `*.vercel.app`. Setiap push baru ke branch production akan memicu deployment baru.

### Alternatif lewat Vercel CLI
Pastikan Node.js terpasang. Dari terminal/PowerShell, masuk ke folder hasil ekstrak, lalu jalankan:

```bash
npx vercel
```

Ikuti pertanyaan CLI dan pilih folder saat ini sebagai project. Untuk publikasi production:

```bash
npx vercel --prod
```

## File yang berubah / ditambahkan

- `index.html` — diperbarui logo, palet warna, dan mode demo statis. Logic marketplace/aksesibilitas yang sudah ada dipertahankan sejauh berjalan di browser.
- `assets/apem-logo.png` — logo APEM baru dari gambar yang diberikan.
- `vercel.json` — konfigurasi hosting statis dan header keamanan dasar.
- `README.md` — panduan hosting.

## Batasan versi statis

Tidak ada backend, database, server login, ataupun payment gateway di paket ini. Fitur jelajah dan alur demo berbasis browser dapat digunakan, tetapi pesanan persisten, autentikasi produksi, chat antarpengguna, dashboard server, upload file, notifikasi, dan pembayaran nyata belum aktif. Login/profil demo hanya simulasi sesi browser dan bukan sistem keamanan. Jangan masukkan data pribadi atau kredensial sungguhan.

Jika nanti membutuhkan akun/pesanan lintas perangkat, pembayaran, atau data produksi, backend perlu ditambahkan dan dikonfigurasi terpisah.
