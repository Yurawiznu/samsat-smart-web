# Samsat Smart Web

**Sistem Informasi dan Monitoring Samsat Berbasis Web**

## 1. Gambaran Umum

Samsat Smart Web merupakan sebuah sistem berbasis web yang dirancang untuk membantu proses monitoring, pemetaan, dan dokumentasi di lingkungan Samsat.

Sistem ini akan mengintegrasikan beberapa fitur utama ke dalam satu platform sehingga informasi dapat dikelola dan ditampilkan secara lebih terstruktur.

> **Status Proyek:** Tahap Perencanaan dan Analisis

---

## 2. Tujuan Proyek

Sistem ini bertujuan untuk:

* Membantu monitoring keaktifan karyawan.
* Menampilkan persentase keaktifan karyawan secara terukur.
* Menampilkan lokasi agen Samsat pada peta wilayah Ponorogo.
* Membantu proses dokumentasi menggunakan kamera.
* Menyimpan dokumentasi secara terorganisir melalui Google Drive.
* Menyatukan beberapa kebutuhan monitoring dan dokumentasi dalam satu sistem berbasis web.

---

## 3. Fitur Utama

### 3.1 Monitoring Keaktifan Karyawan

Sistem dapat menampilkan informasi mengenai tingkat keaktifan karyawan Samsat dalam bentuk persentase dan statistik.

Rencana informasi yang ditampilkan:

* Jumlah karyawan.
* Jumlah karyawan aktif.
* Jumlah karyawan tidak aktif.
* Persentase keaktifan.
* Grafik/statistik keaktifan.
* Riwayat aktivitas.

> Detail indikator dan metode perhitungan keaktifan akan disesuaikan dengan kebutuhan dan ketentuan dari pihak Samsat.

---

### 3.2 Pemetaan Lokasi Agen Samsat

Sistem dapat menampilkan lokasi agen Samsat di wilayah Ponorogo dalam bentuk peta interaktif.

Informasi yang direncanakan:

* Nama agen.
* Alamat agen.
* Titik koordinat.
* Status agen.
* Informasi tambahan sesuai kebutuhan.

Gambaran alur:

```text
Data Agen
    ↓
Koordinat Lokasi
    ↓
Sistem Pemetaan
    ↓
Peta Wilayah Ponorogo
    ↓
Marker Lokasi Agen
```

---

### 3.3 Kamera dan Dokumentasi

Sistem menyediakan fitur kamera yang dapat digunakan untuk mengambil foto melalui web.

Alur dasar:

```text
Buka Kamera
     ↓
Ambil Foto
     ↓
Preview Foto
     ↓
Upload
     ↓
Google Drive
```

Dokumentasi yang tersimpan dapat dilengkapi dengan informasi seperti:

* Tanggal.
* Waktu.
* Nama pengguna/petugas.
* Kategori dokumentasi.
* Lokasi, jika diperlukan.

> Detail metadata dan mekanisme integrasi Google Drive akan ditentukan pada tahap perancangan teknis.

---

## 4. Pengguna Sistem

Pengguna sistem akan ditentukan berdasarkan kebutuhan operasional Samsat.

Rancangan awal pengguna:

### Admin

Memiliki akses untuk:

* Mengelola data pengguna.
* Mengelola data karyawan.
* Mengelola data agen.
* Melihat monitoring.
* Mengelola dokumentasi.

### Pimpinan

Memiliki akses untuk:

* Melihat dashboard.
* Melihat statistik keaktifan.
* Melihat informasi agen.
* Melihat dokumentasi dan laporan.

### Petugas/Karyawan

Akses akan disesuaikan dengan kebutuhan sistem dan kebijakan Samsat.

> Pembagian hak akses akan ditentukan setelah kebutuhan pengguna dikonfirmasi kepada pihak Samsat.

---

## 5. Gambaran Arsitektur Sistem

Rancangan awal sistem:

```text
                    PENGGUNA
                       │
                       ▼
                WEB SAMSAT
                       │
                       ▼
                BACKEND / API
                       │
          ┌────────────┼────────────┐
          │            │            │
          ▼            ▼            ▼
      DATABASE      MAPS API     GOOGLE DRIVE
          │
          │
          ├── Data Pengguna
          ├── Data Karyawan
          ├── Data Aktivitas
          ├── Data Agen
          └── Data Dokumentasi
```

Arsitektur final akan disesuaikan dengan infrastruktur server yang tersedia di Samsat.

---

## 6. Rancangan Data Awal

Data yang kemungkinan diperlukan:

### Data Pengguna

* ID
* Nama
* Username
* Password/credential
* Role

### Data Karyawan

* ID
* Nama
* Jabatan
* Status

### Data Aktivitas

* ID
* ID Karyawan
* Tanggal
* Waktu
* Status aktivitas

### Data Agen

* ID
* Nama Agen
* Alamat
* Latitude
* Longitude
* Status

### Data Dokumentasi

* ID
* Nama File
* Tanggal
* Waktu
* ID Pengguna
* ID/File Google Drive

> Struktur database belum final dan akan disesuaikan dengan hasil analisis kebutuhan.

---

## 7. Infrastruktur dan Server

Sistem akan menggunakan infrastruktur server yang tersedia dan diizinkan oleh pihak Samsat.

Hal yang perlu dikonfirmasi:

* Sistem operasi server.
* Jenis database.
* Web server.
* Spesifikasi server.
* Jaringan yang digunakan.
* Metode akses/deployment.
* Server development/testing.
* Server production.
* Kebijakan keamanan dan akses data.

**Catatan:** Informasi server belum ditentukan pada tahap awal proyek.

---

## 8. Teknologi

Teknologi yang digunakan akan ditentukan setelah kebutuhan sistem dan infrastruktur Samsat diketahui.

Rencana komponen:

| Komponen                | Teknologi            |
| ----------------------- | -------------------- |
| Frontend                | TBD                  |
| Backend                 | TBD                  |
| Database                | TBD                  |
| Pemetaan                | TBD                  |
| Penyimpanan Dokumentasi | Google Drive         |
| Server                  | Infrastruktur Samsat |
| Version Control         | Git + GitHub         |

**TBD (To Be Determined)** berarti masih dalam tahap penentuan.

---

## 9. Tahapan Pengembangan

```text
1. Analisis Kebutuhan
        ↓
2. Penyusunan Kerangka Sistem
        ↓
3. Validasi Kebutuhan dengan Samsat
        ↓
4. Perancangan Sistem
        ↓
5. Perancangan Database
        ↓
6. Perancangan UI/UX
        ↓
7. Pengembangan Backend
        ↓
8. Pengembangan Frontend
        ↓
9. Integrasi Maps
        ↓
10. Integrasi Kamera & Google Drive
        ↓
11. Testing
        ↓
12. Deployment ke Server Samsat
        ↓
13. Dokumentasi & Pemeliharaan
```

---

## 10. Pembagian Tim

Proyek dikerjakan oleh 4 anggota.

| Anggota   | Tanggung Jawab Utama                         |
| --------- | -------------------------------------------- |
| Anggota 1 | Project Lead, Analisis Sistem, dan Integrasi |
| Anggota 2 | Frontend dan UI/UX                           |
| Anggota 3 | Backend dan Database                         |
| Anggota 4 | Maps, Kamera, dan Integrasi Google Drive     |

Pembagian tugas dapat berubah sesuai kebutuhan proyek.

---

## 11. Version Control

Pengembangan sistem menggunakan Git dan GitHub.

Repository:

**samsat-smart-web**

Branch utama:

```text
main
```

Setiap anggota akan menggunakan branch fitur masing-masing selama proses pengembangan.

Contoh:

```text
main
├── feature/frontend
├── feature/backend
├── feature/database
└── feature/maps-camera
```

Penggabungan kode dilakukan melalui Pull Request setelah dilakukan pemeriksaan dan testing.

---

## 12. Keamanan Data

Karena sistem digunakan dalam lingkungan instansi, keamanan data menjadi salah satu aspek utama dalam pengembangan.

Data yang bersifat sensitif tidak boleh dimasukkan ke repository GitHub secara langsung.

Contoh data yang tidak boleh di-commit:

* Password.
* API Key.
* Credential server.
* Credential Google Drive.
* Data pribadi karyawan.
* Data dokumentasi asli.
* Konfigurasi rahasia lainnya.

Credential dan konfigurasi sensitif akan dikelola menggunakan mekanisme yang sesuai dengan lingkungan deployment.

---

## 13. Status Pengembangan

| Komponen            | Status               |
| ------------------- | -------------------- |
| Kerangka Proyek     | 🟡 Dalam Perencanaan |
| Analisis Kebutuhan  | 🟡 Belum Final       |
| Monitoring Karyawan | 🟡 Perencanaan       |
| Pemetaan Agen       | 🟡 Perencanaan       |
| Kamera              | 🟡 Perencanaan       |
| Google Drive        | 🟡 Perencanaan       |
| Database            | ⚪ Belum Ditentukan   |
| Server              | ⚪ Menunggu Informasi |
| UI/UX               | ⚪ Belum Dimulai      |
| Backend             | ⚪ Belum Dimulai      |
| Frontend            | ⚪ Belum Dimulai      |
| Testing             | ⚪ Belum Dimulai      |
| Deployment          | ⚪ Belum Dimulai      |

---

## 14. Catatan Pengembangan

Dokumen ini merupakan kerangka awal proyek dan masih dapat mengalami perubahan berdasarkan hasil diskusi dengan pihak Samsat.

Setiap perubahan kebutuhan, fitur, arsitektur, maupun teknologi akan didokumentasikan melalui repository proyek.
