# Tugas-PBO-Individu  
## ManajemenKost  
**MUHAMMAD ARHAM ANUGRAH**  
**25091160044 B25**

---

## Deskripsi Proyek  
Program **Sistem Manajemen Kost** dibuat untuk membantu pengelolaan data kamar dan penghuni kost secara sederhana.  
Fungsi utama program:  
- Menyimpan informasi kamar kost (nomor kamar, harga sewa, status).  
- Membedakan jenis kamar (biasa dan premium) dengan fasilitas berbeda.  
- Menyimpan data penghuni kost dan menghubungkannya dengan kamar yang ditempati.  
- Mengelola data pembayaran penghuni, termasuk jumlah bayar, tanggal, dan status pembayaran.  

Program ini juga menerapkan konsep **OOP (Object-Oriented Programming)**: inheritance, polymorphism, encapsulation, condition, dan looping.

---

## Alur Program  
1. **Inisialisasi objek kamar**  
   - `KamarBiasa` dan `KamarPremium` dibuat dengan data masing-masing.  
2. **Inisialisasi objek penghuni**  
   - Penghuni dibuat, lalu dihubungkan dengan kamar menggunakan `setKamar()`.  
   - Ada **condition (if-else)** untuk mengecek apakah kamar masih kosong sebelum ditempati.  
3. **Inisialisasi pembayaran**  
   - Objek `Pembayaran` dibuat, lalu dihubungkan dengan penghuni menggunakan `setPenghuni()`.  
4. **Output program**  
   - Informasi kamar, fasilitas, penghuni, dan pembayaran ditampilkan.  
   - Ada **looping (for-each)** di `main` untuk menampilkan daftar kamar sekaligus menghitung harga sewa dengan **polymorphism** (`hitungHarga()` berbeda di `KamarBiasa` dan `KamarPremium`).

     <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/5ea62c02-3e13-4e3e-8026-a607af56da79" />


---

## Hierarki Class  
- **Kamar** superclass  
- **KamarBiasa** subclass dari `Kamar`  
- **KamarPremium** subclass dari `Kamar`  
- **Penghuni** memiliki objek `Kamar`  
- **Pembayaran** berhubungan dengan data `Penghuni`  

---

## Penerapan Konsep OOP  
- **Inheritance**  
  - `KamarBiasa` dan `KamarPremium` mewarisi atribut & method dari `Kamar`.
 
    <img width="1300" height="656" alt="image" src="https://github.com/user-attachments/assets/85a25082-87cf-4f84-9176-7ea73ca033f9" />

    <img width="1159" height="692" alt="image" src="https://github.com/user-attachments/assets/15239528-f4ae-4cf8-a4c6-b890bba79d46" />

    
- **Polymorphism**  
  - Method `hitungHarga()` di-override:  
    - `KamarBiasa` → harga sewa dengan diskon.
   
    <img width="959" height="126" alt="image" src="https://github.com/user-attachments/assets/dcd06678-91a5-4e81-8ccf-22f457b7a8d4" />

    
    - `KamarPremium` → harga sewa dengan tambahan biaya fasilitas.

      <img width="888" height="123" alt="image" src="https://github.com/user-attachments/assets/242c110d-1796-4a09-aec7-b86d33983167" />

- **Encapsulation**  
  - Semua atribut `private`, akses lewat getter & setter.  
- **Condition (if-else)**  
  - Di `Penghuni.setKamar()` untuk mengecek status kamar.
 
    <img width="913" height="149" alt="image" src="https://github.com/user-attachments/assets/31438451-f80b-49bc-a3c5-344302d0e68a" />

    
- **Looping**  
  - Di `main`, menggunakan `for-each` untuk menampilkan daftar kamar.
 
    <img width="875" height="183" alt="image" src="https://github.com/user-attachments/assets/8da56199-be94-4ec9-bf14-65a95b2a431f" />


---

## Dokumentasi Output  

<img width="1244" height="919" alt="image" src="https://github.com/user-attachments/assets/a78c13f8-2de7-429f-bcc4-cf91489c4af0" />

Pada dokumentasi program saat dijalankan:  
- Program menampilkan **nomor kamar, harga sewa, status, fasilitas dasar/tambahan** sesuai jenis kamar.  
- Data penghuni menampilkan **ID, nama, no HP, alamat, serta kamar yang ditempati**.  
- Data pembayaran menampilkan **jumlah bayar, tanggal pembayaran, status pembayaran, dan nama penghuni terkait**.  
- Looping menampilkan daftar kamar sekaligus harga sewa dengan hasil berbeda berkat **polymorphism**.

---
