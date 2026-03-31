# 🎟️ Sistem Simulasi Antrian Tiket Konser (War Ticket)
> Implementasi Struktur Data **Queue** berbasis **Array** menggunakan bahasa Python.

---

## 📌 Deskripsi Proyek
Proyek ini adalah simulasi sistem *Waiting Room* digital yang sering digunakan pada platform penjualan tiket konser besar. Program ini menerapkan prinsip **FIFO (First-In-First-Out)** untuk mengelola lonjakan trafik pengguna secara teratur, adil, dan efisien menggunakan struktur data Array.

## 🧐 Mengapa Memilih Tema Ini?

### 1. Relevansi Fenomena Digital (Deep Dive)
Pemilihan tema ini didasari oleh tantangan nyata dalam industri teknologi saat ini:
* **Pencegahan Server Crash (Load Balancing):** Di dunia nyata, ribuan permintaan masuk dalam satu detik. Antrian berfungsi sebagai *buffer* (penyangga) agar server tidak memproses semua data sekaligus yang bisa menyebabkan sistem tumbang (*crash*).
* **Algoritma Keadilan (Fairness Algorithm):** Dalam *war ticket*, keadilan diukur dalam satuan milidetik. Struktur data Queue menjamin bahwa siapa yang datanya sampai ke server lebih dulu, dialah yang menempati indeks terdepan. Tidak ada data yang bisa "menyerobot" di tengah barisan.
* **Manajemen Antrian Virtual:** Pesan seperti *"You are in the queue, please do not refresh"* adalah implementasi visual dari panjang antrian (`len(array)`) yang sedang diproses oleh sistem.

### 2. Representasi Struktur Data yang Ideal
Secara teknis, tema ini merupakan media simulasi yang sempurna untuk menerapkan **Queue berbasis Array**:
* **Linearitas:** Alur logikanya sangat jelas, mencerminkan barisan pengguna yang menunggu giliran.
* **Operasi Enqueue (`append()`):** Merepresentasikan pengguna yang berhasil menembus trafik dan masuk ke daftar tunggu.
* **Operasi Dequeue (`pop(0)`):** Merepresentasikan pengguna yang berhasil dialihkan ke halaman pembayaran.

---

## 🛠️ Logika Operasi (Prinsip FIFO)

| Operasi | Fungsi Python | Analogi Digital |
| :--- | :--- | :--- |
| **Enqueue** | `.append(user)` | User masuk ke *Waiting Room* (Antrian). |
| **Dequeue** | `.pop(0)` | User diarahkan ke halaman "Pilih Kursi". |
| **Peek** | `array[0]` | Mengecek user mana yang sedang bertransaksi. |
| **Capacity** | `MAX_SIZE` | Batas maksimal pengguna yang bisa ditampung server. |

---

## 💻 Contoh Implementasi Kode
```python
# Potongan logika utama
antrian = [] 
kapasitas = 5

# User masuk (Enqueue)
if len(antrian) < kapasitas:
    antrian.append("User_ID_123")
    
# User diproses (Dequeue)
if antrian:
    user_aktif = antrian.pop(0)
