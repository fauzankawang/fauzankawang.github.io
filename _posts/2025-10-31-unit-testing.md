---
title: 5. Unit Testing
date: 2025-10-31
categories: [Artikel, Software Testing and Quality Assurance]
tags: [Artikel]
---

# Pengantar Unit Testing

---

## 1. Pendahuluan
**Unit Testing** merupakan tahap awal dan paling mendasar dalam proses *Software Testing*.  
Tujuannya adalah memastikan bahwa setiap bagian kecil dari kode (unit), seperti **fungsi, metode, atau kelas**, bekerja dengan benar secara terpisah sebelum digabungkan ke sistem yang lebih besar.

Pengujian ini umumnya dilakukan langsung oleh **developer** sebelum tahap pengujian lain seperti *integration testing* atau *system testing*.

> Dengan kata lain, Unit Testing adalah upaya untuk memastikan bahwa “batu bata” terkecil dari perangkat lunak telah kokoh sebelum membangun seluruh bangunannya.

---

## 2. Apa Itu Unit Testing?
**Unit Testing** adalah proses pengujian terhadap unit terkecil dari kode program, misalnya satu fungsi atau metode, dengan tujuan memastikan bahwa logika di dalamnya memberikan hasil yang benar.

Ciri khas Unit Testing:
- Fokus hanya pada satu unit (fungsi, method, atau class).  
- Tidak bergantung pada modul atau sistem lain.  
- Menggunakan data uji (*test data*) yang dikontrol secara penuh.  

### Analogi
Bayangkan proses **perakitan mobil**:
- Setiap komponen seperti rem, roda, dan mesin diuji **secara terpisah** sebelum dirakit menjadi satu mobil utuh.  
- Jika seluruh komponen lulus uji, maka mobil yang dirakit akan lebih handal.  
- Jika terjadi kesalahan, kita dapat langsung tahu komponen mana yang menjadi sumber masalah.

---

## 3. Mengapa Unit Testing Itu Penting?
Melakukan Unit Testing secara disiplin memberikan banyak manfaat jangka panjang, baik untuk pengembang individu maupun tim besar.

| Manfaat | Penjelasan |
|----------|-------------|
| **Meningkatkan Kepercayaan Diri** | Developer dapat lebih percaya diri bahwa kode yang mereka ubah tidak akan merusak bagian lain dari sistem. |
| **Mendeteksi Bug Lebih Awal** | Kesalahan ditemukan pada tahap awal, sehingga biaya perbaikannya lebih rendah. |
| **Meningkatkan Kualitas Kode** | Mendorong penulisan kode yang modular, bersih, dan mudah diuji. |
| **Mempermudah Perubahan (Refactoring)** | Saat kode diubah, Unit Test akan membantu memastikan perilaku lama tetap berfungsi. |
| **Menghemat Waktu dan Biaya** | Dengan bug yang ditemukan sejak awal, proyek menjadi lebih efisien secara keseluruhan. |
| **Memberikan Dokumentasi Hidup** | Test-case berfungsi sebagai dokumentasi interaktif tentang bagaimana kode seharusnya bekerja. |

---

## 4. Pola Dasar Unit Testing: *Arrange, Act, Assert (AAA)*

Pendekatan paling umum dalam menulis Unit Test adalah **pola AAA (Arrange, Act, Assert)**.  
Pola ini membagi setiap pengujian menjadi tiga bagian utama agar mudah dibaca, dipahami, dan dipelihara.

| Tahap | Deskripsi | Contoh |
|--------|------------|---------|
| **Arrange** | Menyiapkan semua kebutuhan awal sebelum menjalankan tes (data uji, objek, variabel). | `cart = ShoppingCart()` |
| **Act** | Menjalankan aksi utama yang ingin diuji (fungsi atau metode tertentu). | `cart.add_item("Buku", 2)` |
| **Assert** | Memverifikasi apakah hasil dari aksi sesuai dengan ekspektasi. | `assert cart.total_items() == 2` |

Kelebihan pola AAA:
- Struktur tes menjadi lebih rapi dan mudah dipahami.  
- Mengurangi risiko kesalahan dalam penulisan test case.  
- Memudahkan proses debugging saat test gagal.

---

## 5. Framework Populer untuk Unit Testing
Setiap bahasa pemrograman memiliki framework pengujian tersendiri yang membantu developer membuat, menjalankan, dan mengelola Unit Test.

### A. **JUnit 5 (Java)**
Framework standar dan pelopor dalam dunia Unit Testing berbasis Java.
- **Kapan digunakan:** Saat bekerja dengan Java atau bahasa berbasis JVM seperti Kotlin dan Scala.  
- **Keunggulan:**
  - Integrasi penuh dengan IDE (Eclipse, IntelliJ, VS Code).
  - Struktur berbasis anotasi seperti `@Test`, `@BeforeEach`, `@AfterEach`.
  - Ekosistem pendukung luas (Maven, Gradle, Spring).

**Contoh singkat:**
```java
@Test
void testAddition() {
    int result = Calculator.add(2, 3);
    assertEquals(5, result);
}
```

---

### B. **PyTest (Python)**
Framework Unit Testing paling populer dan mudah digunakan di ekosistem Python.
- **Kapan digunakan:** Untuk semua proyek Python, mulai dari skrip sederhana hingga aplikasi kompleks (API, data science, web).  
- **Keunggulan:**
  - Sintaks sederhana tanpa banyak *boilerplate*.
  - Dukungan fixture dan dependency injection.
  - Laporan error yang detail dan mudah dibaca.

**Contoh singkat:**
```python
def test_addition():
    result = add(2, 3)
    assert result == 5
```

---

### C. **Jest (JavaScript)**
Framework buatan Meta (Facebook) untuk aplikasi JavaScript modern.
- **Kapan digunakan:** Saat membangun aplikasi React, Node.js, TypeScript, atau frontend modern lainnya.  
- **Keunggulan:**
  - Zero configuration – langsung digunakan tanpa setup rumit.
  - Fitur *snapshot testing* untuk membandingkan hasil render.
  - Mendukung pengujian asynchronous dan mocking API.

**Contoh singkat:**
```javascript
test('adds two numbers', () => {
  expect(add(2, 3)).toBe(5);
});
```

---

## 6. Cara Memverifikasi Hasil Tes
Setelah menjalankan Unit Test, hasil harus diverifikasi apakah sesuai ekspektasi.

| Jenis Hasil | Deskripsi |
|--------------|------------|
| **Pass** | Test berhasil, hasil aktual sesuai dengan hasil yang diharapkan. |
| **Fail** | Test gagal karena hasil aktual berbeda dari ekspektasi. |
| **Error** | Terjadi kesalahan dalam penulisan atau eksekusi kode test itu sendiri. |

Pengujian yang baik akan memberikan umpan balik langsung:
- Menunjukkan bagian kode mana yang gagal.  
- Menampilkan pesan error dan nilai aktual yang menyebabkan kegagalan.  
- Dapat dijalankan ulang secara otomatis untuk regresi.

---

## 7. Contoh Studi Kasus: Unit Testing Aplikasi Sederhana

### A. Contoh 1 – *Shopping Cart* (menggunakan PyTest)
**Kode yang diuji:**
```python
class ShoppingCart:
    def __init__(self):
        self.items = []

    def add_item(self, item):
        self.items.append(item)

    def total_items(self):
        return len(self.items)
```

**Kode pengujian:**
```python
def test_add_item():
    cart = ShoppingCart()  # Arrange
    cart.add_item("Buku")  # Act
    assert cart.total_items() == 1  # Assert
```

Hasil: **PASS** jika `total_items()` mengembalikan nilai 1 seperti yang diharapkan.

---

### B. Contoh 2 – *Bank Account* (menggunakan JUnit 5)
**Kode yang diuji:**
```java
public class BankAccount {
    private double balance = 0;

    public void deposit(double amount) {
        balance += amount;
    }

    public double getBalance() {
        return balance;
    }
}
```

**Kode pengujian:**
```java
import static org.junit.jupiter.api.Assertions.assertEquals;
import org.junit.jupiter.api.Test;

class BankAccountTest {
    @Test
    void testDeposit() {
        BankAccount account = new BankAccount();  // Arrange
        account.deposit(100.0);                   // Act
        assertEquals(100.0, account.getBalance()); // Assert
    }
}
```

---

## 8. Kesimpulan
Unit Testing adalah salah satu praktik terpenting dalam pengembangan perangkat lunak modern.  
Dengan menerapkannya secara konsisten, tim pengembang akan mendapatkan manfaat besar, seperti:
- Kode yang lebih stabil dan berkualitas tinggi.  
- Deteksi bug lebih cepat dan murah.  
- Dokumentasi otomatis yang selalu relevan.  
- Kepercayaan diri tinggi dalam melakukan perubahan atau refactoring.  

Unit Testing bukan sekadar tugas tambahan, tetapi investasi dalam **keandalan dan kualitas jangka panjang perangkat lunak.**
