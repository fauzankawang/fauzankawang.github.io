---
title: 6. API Testing
date: 2025-10-31
categories: [Artikel, Software Testing and Quality Assurance]
tags: [Artikel]
---

# API Testing

---

## 1. Apa Itu API Testing?

API Testing adalah proses pengujian terhadap **Application Programming Interface (API)** untuk memastikan bahwa:

* API bekerja sesuai spesifikasi.
* API dapat menangani berbagai skenario input dan output dengan benar.
* API menghasilkan output yang sesuai ketika menerima input tertentu.

Tujuan utamanya adalah menjaga kualitas, keandalan, dan keamanan sistem yang menggunakan API.

---

## 2. Keunggulan API Testing

* Memastikan fungsi API sesuai spesifikasi dan menghasilkan output yang benar.
* Meningkatkan keandalan sistem dengan mendeteksi bug sejak awal.
* Menjamin keamanan API dari akses tidak sah dan potensi celah keamanan.
* Mengukur performa API di bawah beban tertentu.
* Mempercepat pengembangan dengan pengujian otomatis.
* Menjadi pondasi penting untuk integrasi antar sistem.

---

## 3. Tools API Testing

### a. Postman

**Alasan penggunaan:**

* Antarmuka yang mudah digunakan (user-friendly)
* Mendukung berbagai metode HTTP (GET, POST, PUT, DELETE, dll)
* Mendukung autentikasi, environment, dan variabel
* Mendukung otomatisasi pengujian dan dokumentasi API

**Fitur utama Postman:**

* Mengirim request HTTP
* Mengelola environment
* Testing otomatis
* Collection dan dokumentasi API
* Mock server dan monitoring

**Contoh Request di Postman:**

```http
GET https://api.example.com/users
Authorization: Bearer <token>
```

**Contoh Response:**

```json
{
  "status": "success",
  "data": [
    {"id": 1, "name": "John Doe"},
    {"id": 2, "name": "Jane Doe"}
  ]
}
```

---

### b. SOAPUI

**Kelebihan:**

* Mendukung SOAP dan REST API.
* Dapat digunakan untuk functional, security, dan load testing.
* Mendukung data-driven testing (mengambil data dari Excel atau database).
* Cocok untuk pengujian enterprise dengan skenario kompleks.

---

## 4. Anatomi Request & Response API

### Anatomi Request

Request adalah **permintaan dari client ke server** untuk mengakses atau memanipulasi data.

| Komponen | Deskripsi |
| ------------------ | ------------------------------------------------------ |
| Method (HTTP Verb) | Jenis aksi: `GET`, `POST`, `PUT`, `DELETE`             |
| URL | Alamat resource yang akan diakses                      |
| Header             | Informasi tambahan, seperti otorisasi atau format data |
| Body               | Data yang dikirim (biasanya dalam `POST` atau `PUT`)   |

**Contoh:**

```http
POST https://api.example.com/users
Content-Type: application/json

{
  "name": "Alice",
  "email": "alice@example.com"
}
```

---

### Anatomi Response

Response adalah **balasan dari server** setelah memproses request.

| Komponen    | Deskripsi                                                                  |
| ----------- | -------------------------------------------------------------------------- |
| Status Code | Kode hasil eksekusi, contoh: `200 OK`, `404 Not Found`, `401 Unauthorized` |
| Headers     | Informasi tambahan dari server                                             |
| Body        | Isi respon berupa data, biasanya dalam format JSON atau XML                |

**Contoh:**

```json
{
  "status": "success",
  "message": "User created successfully"
}
```

---

## 5. Kesimpulan

API Testing merupakan tahap penting dalam pengembangan perangkat lunak modern. Dengan penggunaan tools seperti **Postman** dan **SOAPUI**, pengujian dapat dilakukan secara efisien untuk menjamin kualitas, performa, dan keamanan API yang digunakan dalam aplikasi.

