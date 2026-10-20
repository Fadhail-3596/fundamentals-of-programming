# Memahami Error dan Melakukan Debugging

## 1. Pengertian

Error adalah masalah yang muncul ketika kode ditulis atau dijalankan. Debugging merupakan proses menelusuri, memahami, dan memperbaiki penyebab masalah tersebut.

## 2. Jenis Kesalahan

### Syntax Error

Terjadi ketika kode tidak mengikuti aturan sintaks bahasa pemrograman.

Contoh Python:

```python
if 10 > 5
    print("Benar")
```

Kode tersebut menghasilkan kesalahan karena tanda titik dua (`:`) setelah kondisi tidak ada.

Perbaikan:

```python
if 10 > 5:
    print("Benar")
```

### Runtime Error

Terjadi ketika program sedang dijalankan.

Contoh:

```python
hasil = 10 / 0
```

Pembagian dengan nol menghasilkan `ZeroDivisionError` pada Python.

### Logic Error

Terjadi ketika program berjalan, tetapi hasilnya tidak sesuai dengan tujuan yang diharapkan.

Contoh:

```python
panjang = 10
lebar = 5

luas = panjang + lebar
print(luas)
```

Program berjalan, tetapi perhitungan luas persegi panjang seharusnya menggunakan perkalian.

Perbaikan:

```python
luas = panjang * lebar
```

## 3. Langkah Melakukan Debugging

1. Baca pesan error dengan teliti.
2. Periksa lokasi kode yang disebutkan dalam pesan.
3. Cari tahu penyebab kesalahan, bukan hanya mengubah kode secara acak.
4. Periksa nilai variabel dan alur program.
5. Lakukan perbaikan kecil.
6. Jalankan kembali program untuk menguji hasilnya.

## 4. Menggunakan Try dan Except

Python menyediakan `try` dan `except` untuk menangani exception tertentu.

```python
try:
    angka = int(input("Masukkan angka: "))
    print(10 / angka)
except ValueError:
    print("Input harus berupa angka.")
except ZeroDivisionError:
    print("Angka tidak boleh nol.")
```

Contoh tersebut menangani input yang tidak dapat dikonversi menjadi integer dan pembagian dengan nol.

Penanganan exception sebaiknya disesuaikan dengan jenis kesalahan yang memang ingin ditangani.

## 5. Kebiasaan yang Baik

- Baca pesan error sebelum mencari solusi.
- Gunakan contoh kecil untuk mengisolasi masalah.
- Periksa dokumentasi resmi jika belum memahami perilaku fungsi.
- Uji kembali program setelah melakukan perubahan.
- Hindari menangkap semua exception tanpa memahami konsekuensinya.

## Referensi

- [Python: Errors and Exceptions](https://docs.python.org/3/tutorial/errors.html)
- [MDN: JavaScript Debugging and Error Handling](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/Debugging_JavaScript)
