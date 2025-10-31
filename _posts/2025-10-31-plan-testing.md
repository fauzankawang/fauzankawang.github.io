---
title: 3. Plan Testing
date: 2025-10-31
categories: [Artikel, Software Testing and Quality Assurance]
tags: [Artikel]
---
# Plan Testing
---

## Pengertian Testing Plan
Testing Plan (Rencana Pengujian) adalah dokumen panduan yang menjelaskan bagaimana proses pengujian perangkat lunak akan dilakukan.

Isi utama dari Testing Plan meliputi:
- Ruang lingkup pengujian  
- Strategi atau metodologi yang digunakan  
- Sumber daya (tim, alat, data uji)  
- Jadwal pelaksanaan  

Testing Plan berfungsi sebagai acuan resmi bagi tim penguji agar kegiatan pengujian lebih terarah, konsisten, dan terdokumentasi dengan baik.

---

## Tujuan Testing Plan
- Memberikan gambaran jelas tentang apa yang diuji dan bagaimana pengujian dilakukan.  
- Memastikan pengujian dapat:
  - Menemukan sebanyak mungkin kesalahan (bug).
  - Menjamin perangkat lunak mencapai kualitas yang diharapkan pengguna.
  - Mengoptimalkan waktu, biaya, dan tenaga.
- Menyediakan dokumentasi untuk referensi proyek selanjutnya.

---

## Komponen Testing Plan
Menurut standar **IEEE 829-1988**, sebuah dokumen test plan terdiri atas beberapa komponen penting berikut.

| Komponen | Penjelasan |
|-----------|-------------|
| **Plan Identifier** | Penanda unik berupa kode atau versi dokumen test plan untuk membedakan antar proyek. |
| **References** | Daftar dokumen, standar, atau sumber pendukung agar test plan selaras dengan kebutuhan proyek. |
| **Introduction** | Ringkasan eksekutif yang menjelaskan tujuan, ruang lingkup, dan arah pengujian. |
| **Test Items** | Daftar komponen, modul, atau fitur perangkat lunak yang akan diuji. |
| **Software Risk Issues** | Potensi risiko seperti modul kompleks, integrasi sulit, atau spesifikasi tidak jelas. |
| **Features to be Tested** | Fitur utama yang diuji berdasarkan fungsi dan risiko penggunaannya. |
| **Features Not to be Tested** | Fitur yang dikecualikan dari pengujian karena sudah stabil atau tidak dirilis bersamaan. |
| **Approach** | Strategi umum pengujian, termasuk jenis, metode, dan teknik uji yang digunakan. |
| **Item Pass/Fail Criteria** | Standar yang menentukan keberhasilan atau kegagalan setiap test case. |
| **Suspension & Resumption Criteria** | Kondisi penghentian sementara dan syarat melanjutkan pengujian setelah perbaikan. |
| **Test Deliverables** | Artefak yang dihasilkan seperti test plan, test case, hasil eksekusi, laporan bug, dan ringkasan uji. |
| **Remaining Test Tasks** | Daftar tugas atau aktivitas yang belum selesai saat laporan status dibuat. |
| **Environmental Needs** | Konfigurasi lingkungan pengujian (hardware, software, data uji, jaringan, dan kredensial). |
| **Responsibilities** | Pembagian peran dan tanggung jawab antar anggota tim selama proses pengujian. |
| **Staffing and Training Needs** | Kebutuhan personel dan pelatihan agar tim siap melakukan eksekusi pengujian. |
| **Schedule** | Jadwal pelaksanaan lengkap dari persiapan, eksekusi, hingga sign-off rilis. |
| **Glossary** | Daftar istilah teknis dan singkatan beserta definisinya agar pemahaman antar tim seragam. |
| **Approvals** | Bagian tanda tangan persetujuan dari pihak yang berwenang seperti manajer proyek atau QA. |

---

## Penjelasan Beberapa Komponen Penting

### Plan Identifier
Digunakan untuk menandai setiap dokumen test plan agar mudah dikelola, diidentifikasi, dan direvisi.

### References
Menjamin test plan mengikuti acuan dan dokumen utama proyek sehingga hasil pengujian konsisten dan valid.

### Introduction
Memberi gambaran awal tentang tujuan dan ruang lingkup pengujian agar semua pihak memahami konteks sebelum tahap teknis dimulai.

### Test Items
Menjelaskan elemen perangkat lunak yang diuji, seperti modul, fitur, atau komponen utama.

### Software Risk Issues
Berisi daftar risiko yang mungkin muncul, seperti modul baru, ketidakjelasan spesifikasi, atau masalah integrasi.

### Features to Be Tested
Mendetailkan fungsi utama yang diuji untuk memastikan sesuai kebutuhan pengguna dan standar kualitas.

### Features Not to Be Tested
Menjelaskan fitur yang tidak diuji karena:
- Sudah stabil atau sering digunakan.
- Tidak termasuk dalam lingkup rilis saat ini.

---

## Approach (Pendekatan Pengujian)
Pendekatan pengujian menjelaskan **strategi umum** yang digunakan, meliputi:

| Faktor | Deskripsi |
|--------|------------|
| **Tipe Pengujian** | Unit testing, integration testing, system testing, acceptance testing. |
| **Metode Pengujian** | Black-box, white-box, atau gray-box testing. |
| **Teknik Pengujian** | Manual testing atau automated testing. |
| **Tujuan Pengujian** | Validasi fungsionalitas, performa, keamanan, dan reliabilitas sistem. |

---

## Item Pass/Fail Criteria
Kriteria ini digunakan untuk menentukan apakah suatu test case dianggap **berhasil (pass)** atau **gagal (fail)**.

| Status | Deskripsi |
|---------|------------|
| **Pass Criteria** | Semua test case utama berjalan sesuai harapan tanpa bug kritis. Fitur berfungsi sesuai spesifikasi. |
| **Fail Criteria** | Terdapat test case gagal atau bug mayor yang mempengaruhi fungsi utama aplikasi. |

---

## Suspension Criteria & Resumption Requirements
- **Suspension Criteria**: Kondisi ketika pengujian dihentikan sementara, misalnya karena bug kritis yang membuat tes tidak produktif.  
- **Resumption Requirements**: Kondisi yang harus dipenuhi agar pengujian dapat dilanjutkan setelah masalah diperbaiki.

---

## Test Deliverables
Hasil nyata yang dihasilkan selama proses pengujian, seperti:
- Dokumen test plan  
- Test case dan data uji  
- Hasil eksekusi dan laporan bug  
- Ringkasan hasil pengujian (test summary report)

---

## Remaining Test Tasks
Menjelaskan tugas pengujian yang belum diselesaikan dan langkah lanjutan sebelum pengujian dinyatakan selesai.

---

## Environmental Needs
Menjabarkan spesifikasi lingkungan pengujian:
- Perangkat keras (hardware)  
- Perangkat lunak dan versinya  
- Data uji dan kredensial  
- Jaringan dan alat bantu yang digunakan  

---

## Responsibilities
Membagi tanggung jawab antar anggota tim, meliputi:
- Koordinator pengujian  
- Penulis dan eksekutor test case  
- Verifikator hasil perbaikan  
- Pihak yang memberi persetujuan (approval)  

---

## Staffing and Training Needs
Menentukan jumlah dan kompetensi personel pengujian.  
Meliputi:
- Peran utama (Test Manager, Tester, Developer, Support).  
- Program pelatihan dan sesi orientasi untuk efisiensi tim.

---

## Schedule
Jadwal mencakup seluruh fase pengujian dari persiapan, pelaksanaan, hingga persetujuan akhir (sign-off).  
Termasuk milestone penting seperti:
- Review test case  
- End-to-end test  
- Approval rilis  

---

## Glossary
Berisi daftar istilah teknis atau singkatan yang digunakan dalam dokumen test plan, misalnya:
- Test Plan Identifier  
- Test Items  
- Software Risk Issues  
- Pass/Fail Criteria  

---

## Approvals
Memuat persetujuan resmi dari pihak terkait, termasuk:
- Nama dan jabatan  
- Tanda tangan  
- Tanggal persetujuan  

---

## Penutup
Testing Plan merupakan panduan utama bagi tim QA dan pengembang untuk memastikan proses pengujian berjalan terarah, efisien, dan menghasilkan perangkat lunak berkualitas tinggi.

