# 🏕️ Absensi Digital — Pramuka Ambalan 58

Aplikasi web pencatatan kehadiran anggota **Pramuka Ambalan 58** berbasis single-page HTML yang terintegrasi langsung dengan **Google Sheets** melalui **Google Apps Script**. Dirancang ringan, responsif (*mobile-first*), dan mendukung sinkronisasi *real-time* maupun penyimpanan *cache* lokal.

---

## ✨ Fitur Utama

- **Auto-Detect Jadwal Pertemuan:** Otomatis mendeteksi bulan berjalan dan perkiraan minggu ke- berdasarkan tanggal sistem saat halaman dibuka (dapat diubah secara manual).
- **Pencatatan Status Cepat (1-Tap):** Mendukung 4 kode status kehadiran standar:
  - `H` — Hadir
  - `S` — Sakit
  - `I` — Izin
  - `A` — Alpa
- **Aksi Massal (*Bulk Action*):** Tombol **Set Semua Hadir (H)** untuk mempercepat pengisian daftar hadir.
- **Pendaftaran Anggota Baru Langsung:** Menambahkan peserta baru (Nama & Kelas `X-A` hingga `XII-H`) langsung dari antarmuka absensi, lengkap dengan **deteksi nama ganda** otomatis sebelum data disimpan.
- **Filter Peserta Aktif (`purnaCols`):** Otomatis menyaring anggota yang sudah berstatus purna pada kolom jadwal terkait.
- **Offline-First Cache (`localStorage`):** Menyimpan salinan data sementara selama 5 menit agar aplikasi tetap cepat dimuat sekaligus melakukan sinkronisasi latar belakang (*stale-while-revalidate*).
- **Rekapitulasi Real-Time:** Menampilkan ringkasan jumlah Hadir, Sakit, Izin, dan Alpa secara langsung pada bilah aksi bawah sebelum dikirim ke Google Sheets.

---

## 🛠️ Teknologi yang Digunakan

- **Frontend:** HTML5, Vanilla JavaScript (ES6+)
- **Styling:** [Tailwind CSS](https://tailwindcss.com/) (via CDN) & Google Fonts (`Plus Jakarta Sans`)
- **Backend / Database:** Google Sheets + Google Apps Script Web App (`doGet` & `doPost`)

---

## 📂 Struktur Proyek

```text
├── index.html      # Seluruh antarmuka UI, styling, dan logika aplikasi
└── README.md       # Dokumentasi proyek
