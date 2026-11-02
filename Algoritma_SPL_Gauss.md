# Algoritma Penyelesaian Sistem Persamaan Linear 3 Variabel (Eliminasi Gauss)

1. **Inisialisasi**: Mulai program dan siapkan matriks augmented (A) yang berisi koefisien persamaan dan nilai konstanta di kolom terakhir.
2. **Eliminasi Maju (Forward Elimination)**:
   - Lakukan perulangan (iterasi) pada setiap baris pivot dari baris pertama hingga sebelum baris terakhir.
   - Untuk setiap baris di bawah pivot, hitung rasio pengali: `pengali = elemen_dibawah_pivot / elemen_pivot`.
   - Lakukan operasi baris elementer: kurangi baris saat ini dengan hasil kali rasio pengali dan baris pivot.
   - Hasil dari tahap ini adalah matriks segitiga atas, di mana semua elemen di bawah diagonal utama bernilai nol.
3. **Substitusi Mundur (Backward Substitution)**:
   - Mulai dari baris paling bawah, hitung nilai variabel terakhir (x3) dengan membagi elemen konstanta dengan koefisien diagonalnya.
   - Bergerak naik ke baris sebelumnya (x2 lalu x1), substitusikan nilai variabel yang sudah ditemukan untuk mencari nilai variabel saat ini.
4. **Output**: Tampilkan solusi akhir berupa nilai x1, x2, dan x3 ke layar.
5. **Selesai**.
