<h1 align="center">GenderBridge</h2>

<p align="center"><em>Bridging Data, Empowering Equality</em></p>

<p align="center">
  <img width="1672" height="941" alt="Cover GenderBridge" src="https://github.com/user-attachments/assets/920335b4-c825-48e8-b4eb-08a6660ded31" />
</p>

---

| **Nama**                         | **NIM**     | **Kelas**           | **GitHub** |
|----------------------------------|------------|----------------------|------------|
| Grace Vies Angel                 | 2409116005 | Sistem Informasi A   | [![GitHub](https://img.shields.io/badge/GitHub-Grace-181717?logo=github)](https://github.com/GraceViesAngel) |
| Zahraturramadhani                | 2409116014 | Sistem Informasi A   | [![GitHub](https://img.shields.io/badge/GitHub-Zahra-181717?logo=github)](https://github.com/Zahraramadhani014) |
| Maifariza Aulia Dyas             | 2409116032 | Sistem Informasi A   | [![GitHub](https://img.shields.io/badge/GitHub-Maifa-181717?logo=github)](https://github.com/Maifariza) |

---

## Daftar Isi .✦ ݁˖

- [Latar Belakang](#latar-belakang)
- [Deskripsi Website](#deskripsi-website)
- [Role Pengguna](#role-pengguna)
- [Fitur Website](#fitur-website)
- [Struktur Database](#struktur-database)
  - [Tabel dim_company](#tabel-dim_company)
  - [Tabel dim_department](#tabel-dim_department)
  - [Tabel dim_gender](#tabel-dim_gender)
  - [Tabel dim_job_level](#tabel-dim_job_level)
  - [Tabel fact_employee](#tabel-fact_employee)
  - [Tabel staging_gender](#tabel-staging_gender)
  - [Tabel users](#tabel-users)

---

## Latar Belakang

Kesetaraan gender di tempat kerja masih menjadi perhatian di banyak perusahaan. Perusahaan perlu memberikan kesempatan yang sama kepada karyawan laki-laki dan perempuan, baik dalam hal gaji, promosi, pelatihan, maupun pengembangan karier. Namun, data karyawan yang banyak sering kali sulit dianalisis jika hanya disimpan dalam bentuk tabel biasa.

GenderBridge dibuat untuk membantu perusahaan mengelola dan menganalisis data karyawan dengan lebih mudah. Website ini menggunakan Business Intelligence (BI) dan Decision Support System (DSS) untuk menampilkan dashboard, visualisasi data, dan insight terkait kondisi kesetaraan gender pada perusahaan. Dengan sistem ini, pengguna dapat melihat informasi secara lebih cepat, terstruktur, dan mudah dipahami sehingga membantu proses pengambilan keputusan berbasis data.

---

## Deskripsi Website

GenderBridge merupakan website berbasis Business Intelligence (BI) dan Decision Support System (DSS) yang dirancang untuk membantu perusahaan menganalisis kesetaraan gender berdasarkan data karyawan. Sistem ini dibangun untuk mengelola data dari beberapa perusahaan secara terstruktur melalui proses ETL (Extract, Transform, Load) dan data warehouse menggunakan model Star Schema. GenderBridge menampilkan dashboard interaktif, visualisasi data, serta insight terkait gender, gaji, promosi, pelatihan, dan performa karyawan agar informasi lebih mudah dipahami. Selain itu, sistem juga menyediakan fitur rekomendasi sederhana untuk membantu HR dan manajemen mengambil keputusan yang lebih adil, cepat, dan berbasis data.

---

## Role Pengguna

| Role | Hak Akses |
|---|---|
| **Admin** | Memiliki akses penuh terhadap sistem. Admin dapat mengelola data karyawan, data perusahaan, data departemen, serta mengatur akun pengguna pada website GenderBridge. |
| **HR (_Human Resource_)** | Mengelola dan menganalisis data karyawan. HR dapat melihat dashboard, memantau kesetaraan gender, melihat data promosi, pelatihan, performa karyawan, serta menggunakan hasil rekomendasi dari sistem. |
| **Manager** | Melihat dashboard dan insight yang ditampilkan sistem untuk membantu proses pengambilan keputusan berdasarkan data karyawan dan kondisi kesetaraan gender pada perusahaan. |

---

## Fitur Website

| Fitur | Deskripsi |
|---|---|
| **Login System** | Sistem login untuk membatasi akses pengguna berdasarkan role seperti Admin, HR, dan Manager. |
| **Dashboard Interaktif** | Menampilkan visualisasi data karyawan, distribusi gender, promosi, pelatihan, gaji, dan performa karyawan secara real-time. |
| **Manajemen Data Karyawan** | Fitur untuk melihat, menambah, mengubah, dan menghapus data karyawan pada sistem. |
| **Manajemen Data Departemen** | Fitur untuk mengelola data departemen yang digunakan dalam analisis dashboard. |
| **Analisis Kesetaraan Gender** | Menampilkan perbandingan jumlah karyawan laki-laki dan perempuan berdasarkan perusahaan, departemen, dan level jabatan. |
| **Analisis Gaji** | Menampilkan rata-rata gaji berdasarkan gender dan departemen untuk membantu analisis kompensasi karyawan. |
| **Analisis Promosi dan Pelatihan** | Menampilkan data promosi dan pelatihan berdasarkan gender untuk membantu melihat pemerataan kesempatan kerja. |
| **Performance Score** | Menghitung skor performa karyawan berdasarkan masa kerja, promosi, pelatihan, kepuasan kerja, dan level jabatan. |
| **Rekomendasi Promosi** | Memberikan rekomendasi promosi karyawan berdasarkan performance score dan level jabatan. |
| **Data Warehouse** | Menyimpan data menggunakan model Star Schema agar data lebih terstruktur dan mudah dianalisis. |
| **ETL Process** | Proses Extract, Transform, dan Load untuk membersihkan serta menyiapkan data sebelum digunakan pada sistem dan dashboard. |
| **Insight Otomatis** | Menampilkan insight sederhana terkait kondisi kesetaraan gender berdasarkan hasil analisis data. |

---

## Struktur Database

Database **gender_dss** terdiri dari beberapa tabel utama yang digunakan untuk menyimpan data karyawan, data pendukung, dan data pengguna sistem.

### ᯓ★ Tabel `dim_company`

| Kolom | Tipe | Keterangan |
|---|---|---|
| company_id | INT | Primary key, ID perusahaan |
| company_name | VARCHAR(100) | Nama perusahaan |

### ᯓ★ Tabel `dim_department`

| Kolom | Tipe | Keterangan |
|---|---|---|
| department_id | INT | Primary key, ID departemen |
| department | VARCHAR(100) | Nama departemen |

### ᯓ★ Tabel `dim_gender`

| Kolom | Tipe | Keterangan |
|---|---|---|
| gender_id | INT | Primary key, ID gender |
| gender | VARCHAR(50) | Jenis gender karyawan |

### ᯓ★ Tabel `dim_job_level`

| Kolom | Tipe | Keterangan |
|---|---|---|
| job_level_id | INT | Primary key, ID level jabatan |
| job_level | VARCHAR(100) | Level jabatan karyawan |

### ᯓ★ Tabel `fact_employee`

| Kolom | Tipe | Keterangan |
|---|---|---|
| employee_id | VARCHAR(20) | Primary key, ID karyawan |
| company_id | INT | Relasi ke tabel `dim_company` |
| department_id | INT | Relasi ke tabel `dim_department` |
| gender_id | INT | Relasi ke tabel `dim_gender` |
| job_level_id | INT | Relasi ke tabel `dim_job_level` |
| years_of_service | FLOAT | Lama masa kerja karyawan |
| salary | FLOAT | Data gaji karyawan |
| job_satisfaction | INT | Nilai kepuasan kerja karyawan |
| promotion_status | VARCHAR(50) | Status promosi karyawan |
| training_status | VARCHAR(50) | Status pelatihan karyawan |
| service_category | VARCHAR(50) | Kategori masa kerja karyawan |
| salary_category | VARCHAR(50) | Kategori gaji karyawan |
| performance_score | FLOAT | Skor performa karyawan |

### ᯓ★ Tabel `staging_gender`

| Kolom | Tipe | Keterangan |
|---|---|---|
| employee_id | VARCHAR(20) | ID karyawan dari data awal |
| company_name | VARCHAR(100) | Nama perusahaan |
| department | VARCHAR(100) | Nama departemen |
| gender | VARCHAR(50) | Gender karyawan |
| job_level | VARCHAR(100) | Level jabatan karyawan |
| years_of_service | FLOAT | Lama masa kerja karyawan |
| salary | FLOAT | Data gaji karyawan |
| promotion_last_2_years | VARCHAR(20) | Status promosi dalam 2 tahun terakhir |
| leadership_training | VARCHAR(20) | Status pelatihan kepemimpinan |
| job_satisfaction | INT | Nilai kepuasan kerja karyawan |
| salary_category | VARCHAR(50) | Kategori gaji karyawan |
| promotion_status | VARCHAR(50) | Status promosi karyawan |
| training_status | VARCHAR(50) | Status pelatihan karyawan |
| service_category | VARCHAR(50) | Kategori masa kerja karyawan |
| performance_score | FLOAT | Skor performa karyawan |

### ᯓ★ Tabel `users`

| Kolom | Tipe | Keterangan |
|---|---|---|
| user_id | INT | Primary key, ID pengguna |
| name | VARCHAR(100) | Nama pengguna |
| username | VARCHAR(50) | Username untuk login |
| password | VARCHAR(255) | Password pengguna |
| role | ENUM('admin','hr','manager') | Role pengguna sistem |

---
