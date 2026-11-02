# Algoritma Penyelesaian Persamaan Non-Linear (Metode Bisection)

1. **Inisialisasi**: Definisikan persamaan matematika non-linear f(x). Tetapkan tebakan interval awal berupa batas_kiri dan batas_kanan, serta batas toleransi error dan iterasi maksimum.
2. **Validasi Interval**: Pastikan f(batas_kiri) dikali f(batas_kanan) < 0. Jika tidak, akar tidak dijamin berada di dalam interval dan tebakan harus diubah.
3. **Proses Pencarian (Iterasi)**:
   - Lakukan perulangan hingga mencapai iterasi maksimum.
   - Hitung titik pembagi (tengah): `titik_tengah = (batas_kiri + batas_kanan) / 2`.
   - Cek kondisi berhenti: Jika f(titik_tengah) == 0 atau rentang (batas_kanan - batas_kiri)/2 lebih kecil dari toleransi error, maka titik_tengah ditetapkan sebagai akar, lalu hentikan perulangan.
   - Jika kondisi berhenti belum terpenuhi, geser batas interval:
     * Jika f(batas_kiri) * f(titik_tengah) < 0, maka akar berada di paruh kiri, ubah `batas_kanan = titik_tengah`.
     * Jika tidak, maka akar berada di paruh kanan, ubah `batas_kiri = titik_tengah`.
4. **Output**: Cetak nilai estimasi akar persamaan.
5. **Selesai**.
