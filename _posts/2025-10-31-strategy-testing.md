---
title: 1. Strategi Testing
date: 2025-10-31
categories: [Artikel, Software Testing and Quality Assurance]
tags: [Artikel]
---

# Testing Strategi
---

## 1. Pengertian Testing
Testing adalah proses **mengevaluasi perangkat lunak** untuk mendeteksi kesalahan (*bug*) dan memastikan sistem berfungsi sesuai **kebutuhan fungsional maupun non-fungsional**.  
Tujuan utama testing adalah untuk menjamin **kualitas software**, **keamanan sistem**, **pengalaman pengguna yang baik**, serta **efisiensi biaya pengembangan**.

| **Aspek**             | **Penjelasan**                                                                 |
|------------------------|--------------------------------------------------------------------------------|
| **Tujuan Testing**     | Menemukan bug dan memastikan sistem bekerja sesuai kebutuhan.                  |
| **Manfaat**            | Mengurangi risiko kegagalan, meningkatkan kepercayaan stakeholder, efisiensi biaya. |
| **Hasil Akhir**        | Software berkualitas tinggi, aman, stabil, dan memenuhi kebutuhan pengguna.    |

---

## 2. Software Testing Life Cycle (STLC)
STLC adalah **proses sistematis** yang terdiri dari tahapan berurutan untuk menjamin kualitas perangkat lunak.

| **Tahap**                       | **Deskripsi**                                                                  | **Hasil Utama**                            |
|---------------------------------|--------------------------------------------------------------------------------|--------------------------------------------|
| **1. Test Planning**            | Menentukan strategi, waktu, biaya, lingkungan, dan peran pengujian.            | Dokumen rencana pengujian.                |
| **2. Test Design**              | Membuat *test case*, data uji, dan skenario pengujian.                         | Daftar test case & RTM (*Requirement Traceability Matrix*). |
| **3. Test Execution**           | Menjalankan pengujian (unit, integrasi, sistem, acceptance).                   | Hasil pelaksanaan uji.                    |
| **4. Test Reporting & Analysis**| Menganalisis hasil, mencatat bug, dan memberi rekomendasi perbaikan.           | Laporan hasil uji dan rekomendasi.        |

---

## 3. Jenis Pengujian Berdasarkan Abstraksi

| **Jenis Testing**     | **Tujuan**                                                | **Contoh**                                      |
|------------------------|-----------------------------------------------------------|-------------------------------------------------|
| **Unit Testing**       | Menguji fungsi/metode tunggal agar hasilnya akurat.      | Menguji fungsi perhitungan diskon.              |
| **Integration Testing**| Memastikan interaksi antar modul berjalan baik.          | Modul login terhubung dengan modul profil.      |
| **System Testing**     | Menguji sistem secara keseluruhan terhadap spesifikasi.  | Aplikasi e-commerce untuk 1000 pengguna.        |
| **Acceptance Testing** | Validasi akhir oleh pengguna/klien sebelum rilis.        | Klien menyetujui aplikasi sebelum diluncurkan.  |

---

## 4. Jenis Pengujian Berdasarkan Fungsi

| **Jenis**               | **Fokus**                                      | **Contoh**                                   | **Tujuan**                               |
|--------------------------|------------------------------------------------|-----------------------------------------------|-------------------------------------------|
| **Fungsional Testing**   | Menguji fungsi utama sistem sesuai kebutuhan. | Login, reset password, pembayaran online.     | Menjamin fungsi berjalan dengan benar.    |
| **Non-Fungsional Testing**| Menguji performa, keamanan, dan reliabilitas. | Uji performa saat flash sale, uji respon sistem. | Menilai kualitas dan ketahanan sistem.   |

---

## 5. Jenis Pengujian Berdasarkan Domain

| **Jenis Testing**      | **Fokus**                              | **Contoh**                                      | **Tujuan**                                      |
|-------------------------|-----------------------------------------|-------------------------------------------------|-------------------------------------------------|
| **Performance Testing** | Kinerja & stabilitas sistem di beban tinggi. | Menguji website saat traffic tinggi.            | Menjamin sistem tetap cepat & stabil.           |
| **Security Testing**    | Identifikasi celah keamanan.           | Uji serangan SQL injection, XSS.                | Melindungi data pengguna dan sistem.            |
| **Usability Testing**   | Kemudahan penggunaan bagi user.        | Evaluasi kemudahan navigasi & ikon.             | Memastikan aplikasi ramah dan mudah digunakan.  |

---

## 6. Jenis Pengujian Berdasarkan Struktur

| **Jenis Testing**     | **Penjelasan**                                                  | **Kelebihan**                                         | **Kekurangan**                                       |
|------------------------|----------------------------------------------------------------|--------------------------------------------------------|------------------------------------------------------|
| **Black-Box Testing**  | Penguji tidak tahu struktur kode, hanya menguji input–output. | Mudah dilakukan, sesuai sudut pandang user.            | Tidak mendeteksi bug dalam logika internal.          |
| **White-Box Testing**  | Penguji memahami struktur & logika kode program.              | Dapat menemukan bug tersembunyi dan meningkatkan kualitas kode. | Membutuhkan waktu & keahlian teknis tinggi.         |

---

## 7. Pelaporan & Analisis Testing
Setelah pengujian selesai, hasil dianalisis untuk mengukur kualitas dan menentukan langkah perbaikan.

| **Komponen**         | **Isi Pelaporan**                                                                 |
|-----------------------|-----------------------------------------------------------------------------------|
| **Ringkasan Hasil**   | Jumlah test case yang berhasil, gagal, dan belum dijalankan.                     |
| **Evaluasi Kualitas** | Apakah sistem memenuhi spesifikasi fungsional dan non-fungsional.                |
| **Identifikasi Bug**  | Jenis kesalahan, tingkat keparahan, dan status perbaikan.                        |
| **Rekomendasi**       | Saran peningkatan performa, keamanan, dan stabilitas sistem.                     |
| **Analitik & Grafik** | Tren hasil pengujian seperti jumlah bug dan keberhasilan test case dari waktu ke waktu. |

---

## 8. Kesimpulan
Testing merupakan **tahapan krusial dalam SDLC (Software Development Life Cycle)** karena berfungsi memastikan **kualitas, keamanan, dan keandalan software** sebelum dirilis kepada pengguna.  
Dengan testing yang baik, tim pengembang dapat:

- Mengurangi risiko dan biaya perbaikan di tahap akhir,  
- Menjamin performa & keamanan sistem,  
- Meningkatkan kepuasan dan kepercayaan pengguna.

| **Aspek Utama**        | **Dampak**                                                |
|-------------------------|-----------------------------------------------------------|
| **Kualitas Produk**     | Software lebih stabil, aman, dan bebas bug.              |
| **Kepercayaan Pengguna**| Meningkatkan kepuasan dan loyalitas pengguna.           |
| **Efisiensi Proyek**    | Waktu perbaikan berkurang dan biaya lebih terkendali.   |

---
