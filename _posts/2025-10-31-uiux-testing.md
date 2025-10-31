---
title: 2. UI/UX Testing
date: 2025-10-31
categories: [Artikel, Software Testing and Quality Assurance]
tags: [Artikel]
---
#  UI/UX Testing
---

##  Perbedaan Mendasar antara UI & UX Testing

| **Aspek** | **UI Testing** | **UX Testing** |
|------------|----------------|----------------|
| **Fokus** | Tampilan antarmuka: warna, ikon, ukuran tombol, layout, konsistensi, dan responsivitas. | Pengalaman pengguna secara keseluruhan saat berinteraksi dengan aplikasi. |
| **Contoh Uji** | Memastikan tombol Login tampil di posisi yang benar, font terbaca, dan tampilan konsisten di desktop & mobile. | Menguji apakah pengguna dapat menemukan produk dan menyelesaikan pembelian dengan mudah tanpa kebingungan. |

---

##  Fokus UI Testing

### 1 Konsistensi Visual
- Semua halaman harus memiliki gaya seragam (warna, ikon, font, ukuran tombol).  
- **Contoh pengujian:**  
  - Manual checklist.  
  - *Automated Visual Regression Testing* → *Percy*, *Applitools*, *Selenium + visual plugin*.  
  - Periksa apakah tombol “Login” memiliki warna & ukuran sama di semua halaman.

### 2️ Responsivitas
- Desain tetap nyaman pada berbagai ukuran layar (desktop, tablet, smartphone).  
- **Tools:** *BrowserStack*, *LambdaTest*, *Responsively App*.  
- **Contoh:** Buka website pada HP 5", tablet 10", laptop 14" → teks & gambar tetap terbaca.

### 3️ Kompatibilitas
- UI harus berfungsi baik di berbagai browser dan OS (Chrome, Firefox, Safari, Edge, Windows, macOS, Android, iOS).  
- **Tools:** *BrowserStack*, *Sauce Labs*, *LambdaTest*.  
- **Contoh:** Periksa apakah animasi dan ikon tampil konsisten di iOS dan Android.

---

## Fokus UX Testing

### Alur Kerja (Workflow)
UX testing bersifat iteratif dan terintegrasi dalam pengembangan (Agile atau Waterfall).

| **Tahapan Alur Kerja** | **Kegiatan Utama** |
|--------------------------|--------------------|
| **Perencanaan** | Menentukan tujuan, metode, dan peserta uji. |
| **Rekrutmen Pengguna** | Memilih pengguna representatif sesuai target audien. |
| **Pelaksanaan Sesi Uji** | Observasi, wawancara, dan pencatatan perilaku pengguna. |
| **Analisis Data** | Mengidentifikasi hambatan, pola perilaku, dan insight pengalaman. |
| **Iterasi Desain** | Melakukan perbaikan berdasarkan temuan uji. |

**Contoh Kasus:**  
Shopify – Pengujian Profil Pakar:  
- Dimulai dengan wawancara generatif, diikuti *card sorting* & *tree testing*.  
- Hasil temuan (pengguna menyukai profil lebih manusiawi) digunakan untuk iterasi desain.

---

### Kegunaan (Usability Testing)
Usability Testing mengevaluasi seberapa **mudah & efektif** pengguna berinteraksi dengan sistem menggunakan pengguna nyata.

| **Tujuan Utama** | **Manfaat** |
|-------------------|--------------|
| Mengamati kesulitan pengguna saat menyelesaikan tugas. | Mengidentifikasi cacat desain lebih awal, mengurangi biaya perbaikan, dan meningkatkan kepuasan pengguna. |

**Contoh Kasus:**  
Movista – Pengiriman Pesan:  
- Menggunakan *remote usability testing* dengan prototipe high-fidelity via Maze.  
- Uji dilakukan *unmoderated* dengan tugas & pertanyaan follow-up.  
- Feedback → mengubah urutan pemilihan penerima & iterasi sebelum peluncuran.

---

### Aksesibilitas (Accessibility Testing)
Menjamin aplikasi dapat digunakan oleh semua orang, termasuk penyandang disabilitas (penglihatan, pendengaran, motorik).

| **Aspek yang Diuji** | **Deskripsi** | **Contoh Pengujian** |
|------------------------|----------------|------------------------|
| **Standar WCAG** | Mengacu pada *Web Content Accessibility Guidelines*. | Menilai penggunaan *screen reader*, navigasi keyboard, dan kontras warna. |
| **Kontras Warna** | Memastikan teks dan latar belakang memenuhi rasio WCAG. | Verifikasi bahwa teks mudah dibaca oleh pengguna dengan gangguan penglihatan. |

---

## Metode & Tools UI/UX Testing

| **Metode** | **Fokus Utama** | **Contoh Tools** |
|-------------|------------------|------------------|
| **Heatmaps** | Melihat area yang paling sering di-klik / diperhatikan user. | *Hotjar*, *Crazy Egg*, *Microsoft Clarity*. |
| **A/B Testing** | Membandingkan dua versi UI untuk mengetahui mana yang lebih efektif. | *Google Optimize*, *Optimizely*. |
| **Prototyping & Checklist** | Mengevaluasi tampilan (UI) dan alur interaksi (UX). | *Figma*, *Zeplin*, *Maze*. |

---

## Heuristic Evaluation
Evaluasi heuristik adalah metode UX yang menggunakan prinsip-prinsip desain Nielsen Norman untuk memeriksa masalah penggunaan.

| **Prinsip Heuristik** | **Deskripsi Singkat** |
|-------------------------|------------------------|
| **1. Visibilitas Status Sistem** | Sistem harus memberikan umpan balik yang jelas dan tepat waktu. |
| **2. Kecocokan dengan Dunia Nyata** | Gunakan bahasa & ikon yang familiar bagi pengguna. |
| **3. Kontrol & Kebebasan Pengguna** | Sediakan opsi *undo* atau *emergency exit*. |
| **4. Konsistensi & Standar** | Terminologi & elemen desain harus konsisten di seluruh platform. |
| **5. Pencegahan Kesalahan** | Desain harus mencegah error sejak awal, bukan hanya menampilkan pesan. |
| **6. Mengenali daripada Mengingat** | Minimalkan beban ingatan pengguna dengan membuat opsi terlihat. |
| **7. Fleksibilitas & Efisiensi** | Sediakan jalan pintas (*shortcuts*) bagi pengguna ahli. |
| **8. Desain Estetis & Minimalis** | Hindari informasi berlebihan dan tampilkan hanya yang relevan. |
| **9. Bantu Pengguna Mengatasi Kesalahan** | Tulis pesan error yang jelas & sertakan solusi. |
| **10. Bantuan & Dokumentasi** | Sediakan dokumentasi & bantuan yang mudah diakses. |

---

## Kesimpulan
UI/UX Testing adalah dua aspek yang saling melengkapi:
- **UI Testing** menjamin tampilan & konsistensi visual.  
- **UX Testing** memastikan pengalaman pengguna mudah, efisien, dan inklusif.  
Pengujian yang baik menghasilkan **produk digital berkualitas tinggi, mudah digunakan, dan menyenangkan bagi pengguna.**
