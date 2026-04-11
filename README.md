# 🎟️ Sistem Simulasi Antrian Tiket Konser (War Ticket)
> Implementasi Struktur Data **Queue** berbasis **Array** menggunakan bahasa Python.


## Deskripsi Proyek
Proyek ini adalah simulasi sistem *Waiting Room* digital yang sering digunakan pada platform penjualan tiket konser besar. Program ini menerapkan prinsip **FIFO (First-In-First-Out)** untuk mengelola lonjakan trafik pengguna secara teratur, adil, dan efisien menggunakan struktur data Array.

## Mengapa Memilih Tema Ini?

Kami mengangkat studi kasus **Sistem Antrian Tiket (War Ticket)** karena tema ini adalah contoh nyata paling sempurna untuk menunjukkan fungsi **Queue** dalam menjaga stabilitas dan keadilan sistem digital. 

Secara teknis, antrian ini berfungsi sebagai *buffer* untuk mencegah server *crash* saat ada lonjakan ribuan pengunjung secara bersamaan. Dengan menggunakan **Array**, kita bisa mensimulasikan prinsip **FIFO (First-In-First-Out)** secara akurat; menjamin setiap pengguna dilayani berdasarkan urutan yang jujur (sesuai indeks) dan tidak dapat diserobot. Kasus ini menjadi media yang sangat relevan untuk mempraktikkan empat operasi utama: **Enqueue, Dequeue, Peek,** dan **Display** dalam skenario penyelesaian masalah dunia nyata.
## Rumusan Masalah

Berdasarkan studi kasus yang diangkat, proyek ini menjawab beberapa permasalahan akademik sebagai berikut:

1. **Efektivitas FIFO:** Bagaimana implementasi prinsip *First-In-First-Out* (FIFO) menggunakan *Array* dapat menjamin keadilan urutan dalam sistem *War Ticket*?
2. **Manajemen Kapasitas:** Sejauh mana operasi *Enqueue* dan *Dequeue* efektif dalam menangani pembatasan kuota pengunjung saat terjadi lonjakan trafik digital?
3. **Transparansi Data:** Apa peran operasi *Peek* dan *Display* dalam memberikan informasi posisi antrian yang akurat kepada pengguna?

## Solusi yang Ditawarkan

Sistem ini hadir sebagai solusi teknis untuk menangani kekacauan trafik digital melalui:

* **Otomatisasi FIFO:** Menjamin urutan pemrosesan tiket yang adil dan sistematis berdasarkan waktu kedatangan pengguna (Indeks Array).
* **Pembatasan Kuota (Load Management):** Mencegah kelebihan beban pada server dengan membatasi jumlah maksimal pengguna dalam antrian melalui parameter `kuota_antrian`.
* **Informasi Real-Time:** Memberikan transparansi status kepada pengguna lewat fungsi `peek` (melihat urutan terdepan) dan `display` (melihat seluruh daftar tunggu).
## Landasan Teori
### Struktur data
Struktur data adalah cara penyimpanan, pengorganisasian, dan pengaturan
data di dalam media penyimpanan komputer sehingga data tersebut dapat
digunakan secara efisien. *Aho, Hopcroft, Ullman, 1987,Data Structures and Algorithms,Prentice Hall*
#### konsep queue / stack
Dalam konsep penyimpanan linear, terdapat dua model utama yaitu Queue (antrean) dan Stack (tumpukan). Sjukani (2014) menjelaskan bahwa Queue adalah sekumpulan data yang penambahan elemennya dilakukan di satu ujung (rear) dan penghapusannya di ujung lain (front). Sementara itu, Stack diibaratkan sebagai tumpukan piring di mana penambahan dan penghapusan data hanya terjadi pada satu ujung yang sama (top). Perbedaan mendasar ini menentukan skenario penggunaan keduanya dalam aplikasi perangkat lunak.
#### konsep FIFO / LIFO
Metode akses data pada kedua struktur tersebut dikenal dengan prinsip FIFO (First-In-First-Out) dan LIFO (Last-In-First-Out). Jurnal penelitian dari Putra dkk. (2020) menyebutkan bahwa Queue mengikuti prinsip FIFO, di mana data yang pertama kali masuk akan menjadi yang pertama kali diproses—sangat ideal untuk sistem antrean tiket. Sebaliknya, Stack menggunakan prinsip LIFO, di mana data yang terakhir masuk justru akan menjadi yang pertama kali keluar, seperti fungsi "Undo" pada aplikasi pengolah kata.
#### implementasi menggunakan array atau linked list
Implementasi Queue maupun Stack dapat dilakukan menggunakan dua media utama, yaitu Array atau Linked List. Menurut Karumanchi (2016) dalam Data Structures and Algorithms Made Easy, implementasi menggunakan Array lebih sederhana karena data disimpan pada blok memori yang berurutan (statis). Namun, jika kapasitas data bersifat dinamis atau tidak menentu, penggunaan Linked List lebih disarankan karena setiap elemen (node) menyimpan alamat memori elemen berikutnya, sehingga lebih fleksibel dalam alokasi memori meskipun logikanya lebih kompleks dibanding Array.

###  Flowchart Logika Program
![alt text](https://github.com/nengahresti14-hub/tugas-kelompok/blob/main/flowchart.png?raw=true)

### Alur Implementasi (Input -> Proses -> Output)

1. **Input:** Nama pembeli dimasukkan melalui metode enqueue(nama_user).
2. **Proses:** - **Validasi:** Sistem mengecek kapasitas array self.antrian.
   - **Antrean:** Jika masih ada slot, nama disimpan di urutan terakhir.
   - **FIFO:** Saat dequeue() dipanggil, data pada index 0 diproses dan dihapus, sehingga data lainnya maju ke depan.
3. **Output:** - Notifikasi keberhasilan/kegagalan masuk antrian.
   - Visualisasi daftar tunggu (display).
   - Konfirmasi tiket terbit untuk user yang diproses.

      

## Kesimpulan

Berdasarkan hasil implementasi sistem **War Ticket**, dapat disimpulkan bahwa:

1. **Masalah Terselesaikan:** Sistem berhasil mengelola antrian secara adil dan transparan sesuai dengan pembatasan kuota yang ditentukan.
2. **Sesuai Teori:** Implementasi menggunakan Python terbukti mengikuti prinsip **FIFO (First-In-First-Out)** secara akurat melalui operasi `enqueue` dan `dequeue`.
3. **Manfaat Nyata:** Penggunaan struktur data *Queue* sangat efektif sebagai penyangga (*buffer*) untuk mencegah server *crash* saat lonjakan pengunjung, sekaligus menjamin urutan transaksi yang jujur bagi pengguna.
