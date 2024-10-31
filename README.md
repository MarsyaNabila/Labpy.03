# Labpy.03
## Nama : MARSYA NABILA PUTRI
## Kelas : TI.24.A.4
## NIM : 312410338
## Matkul : BAHASA PEMROGRAMAN

# Soal Latihan

![WhatsApp Image 2024-10-31 at 21 07 25_8e06d639](https://github.com/user-attachments/assets/403d1fa1-0a72-4b15-acbb-0cf88f9d4380)

# Latihan1.py

```PYTHON
import random

n = int(input("Masukkan nilai N: "))

for i in range(1, n+1):
  angka_acak = random.random()
  print(f"data ke: {i} => {angka_acak}")

print("Selesai")
````

```PYTHON
import random
````

Baris ini mengimpor modul random, yang berisi fungsi-fungsi untuk menghasilkan angka acak.

```PYTHON
n = int(input("Masukkan nilai N: "))
````

Pengguna meminta untuk memasukkan nilai integer nyang menentukan berapa banyak angka acak yang akan dihasilkan. Berfungsi input() menerima masukan dari pengguna dalam bentuk string, dan int () mengubahnya menjadi integer.

```PYTHON
for i in range(1, n + 1):
````

foradalah perulangan yang akan berjalan sebanyak N kali, range (1, n + 1) menghasilkan urutan angka mulai dari 1 hingga N (termasuk N), yang digunakan untuk menentukan jumlah angka acak yang akan dihasilkan.

```PYTHON
angka_acak = random.random()
  print(f"data ke: {i} => {angka_acak}")
````

Di dalam perulangan, random.random()digunakan untuk menghasilkan angka acak dalam rentang 0.0 hingga 1.0, dengan nomor urut datanya ( data ke: {i}). Format {i} dan {angka_acak} digunakan dalam f-stringuntuk menampilkan nilai variabel idan angka_acaksecara langsung di dalam string.

```PYTHON
print("Selesai")
````

Setelah perulangan selesai, baris ini menampilkan pesan "Selesai" untuk menandakan bahwa program telah selesai menjalankan seluruh instruksi.

Kode program tersebut:

![WhatsApp Image 2024-10-31 at 21 39 34_11c4009e](https://github.com/user-attachments/assets/c3d17576-f5aa-4102-a4d4-b3730b9b1e1e)

Hasil dari program tersebut:

![WhatsApp Image 2024-10-31 at 21 41 48_1e17f736](https://github.com/user-attachments/assets/c990b9d2-4053-40c4-9a49-8772ef51ae24)

# Latihan2.py
# Menghitung Laba Usaha selama 8 Bulan

## Deskripsi 

Program ini melakukan perhitungan laba bulanan dengan aturan sebagai berikut:
1. **Bulan 1 dan 2**: Belum mendapatkan laba (0%).
2. **Bulan 3 dan 4**: Mendapatkan laba sebesar 1% dari modal awal.
3. **Bulan 5, 6, dan 7**: Mendapatkan laba sebesar 5% dari modal awal.
4. **Bulan 8**: Mengalami penurunan laba menjadi 3% dari modal awal.

Program akan menghitung laba untuk setiap bulan dan menampilkan hasilnya. Setelah 8 bulan, program juga menampilkan total laba yang diakumulasi selama periode tersebut.

## Cara Menjalankan Program

1. Pastikan Python sudah terinstal di komputer Anda.
2. Simpan program ini sebagai latihan2.py.
3. Buka terminal atau command prompt di lokasi penyimpanan file tersebut.
4. Jalankan perintah berikut:

```PYTHON
python3 latihan2.py
````

## Penjelasan Kode
### 1. Modal Awal dan Variabel Laba
```PYTHON
modal_awal = 100_000_000
total_laba = 0
````

```PYTHON
   - `modal_awal: menyimpan modal awal pengusaha, yaitu 100 juta rupiah.`
   - `total_laba: akumulasi total laba dari bulan 1 hingga 8, dimulai dari 0.`
````

### 2. Lingkaran Perhitungan Laba per Bulan

```PYTHON
for bulan in range(1, 9):
    if bulan in [1, 2]:        # Bulan 1 dan 2 belum mendapatkan laba
        laba = 0
    elif bulan == 3:           # Bulan 3 mendapatkan laba 1%
        laba = 0.01 * modal_awal
    elif bulan == 4:           # Bulan 4 mendapatkan laba 1%
        laba = 0.01 * modal_awal
    elif bulan == 5:           # Bulan 5 mendapatkan laba 5%
        laba = 0.05 * modal_awal
    elif bulan in [6, 7]:      # Bulan 6 dan 7 mendapatkan laba 5%
        laba = 0.05 * modal_awal
    elif bulan == 8:           # Bulan 8 mendapatkan laba 3%
        laba = 0.03 * modal_awal
````

Program menggunakan loop fordari bulan 1 hingga 8. Di setiap iterasi, program menentukan besarnya laba berdasarkan kondisi:
   - Bulan 1 dan 2 : laba 0%.
   - Bulan 3 dan 4 : laba 1% dari modal awal.
   - Bulan 5, 6, dan 7 : laba 5% dari modal awal.
   - Bulan 8 : laba 3% dari modal awal.

### 3. Menambahkan Laba ke Total Laba dan Menampilkan Laba per Bulan

```PYTHON
total_laba += laba
print(f"laba bulan ke- {bulan} sebesar: {laba}")
````

Setiap laba bulanan yang dihitung akan ditambahkan ke total_laba. Selain itu, program menampilkan laba yang diperoleh pada bulan tersebut.

### 4. Akhir Program: Menampilkan Total Laba

```PYTHON
print(f"Total laba adalah: {total_laba}")
````

Setelah loop selesai, program menampilkan total laba yang diperoleh selama 8 bulan.

## Contoh Output

Jika Anda menjalankan program ini, outputnya mungkin akan terlihat seperti berikut:
```PYTHON
laba bulan ke- 1 sebesar: 0
laba bulan ke- 2 sebesar: 0
laba bulan ke- 3 sebesar: 1000000.0
laba bulan ke- 4 sebesar: 1000000.0
laba bulan ke- 5 sebesar: 5000000.0
laba bulan ke- 6 sebesar: 5000000.0
laba bulan ke- 7 sebesar: 5000000.0
laba bulan ke- 8 sebesar: 3000000.0
Total laba adalah: 19000000.0
````

## Berikut adalah hasin screenshot visual studio code

![WhatsApp Image 2024-10-31 at 22 01 39_3e1bf7f3](https://github.com/user-attachments/assets/8fead30d-9e00-46ae-bce4-9d52479c8c1e)

# LATIHAN 3.latihan3.py
# Simulasi Mesin ATM Sederhana

## Deskripsi
Program ini adalah simulasi mesin ATM sederhana yang memungkinkan pengguna untuk melakukan penarikan uang dengan saldo awal sebesar Rp 1.000.000. Pengguna dapat memilih untuk menarik uang atau keluar dari sistem.

## Fitur Program
1. **Menampilkan Saldo** - Program akan selalu menampilkan saldo saat ini.
2. **Penarikan Uang** - Pengguna dapat melakukan penarikan uang dengan nominal tertentu.
3. **Validasi Saldo** - Program akan mengecek apakah saldo mencukupi sebelum memproses penarikan.
4. **Keluar dari Program** - Pengguna dapat memilih untuk keluar dari program.

## Cara Menggunakan Program

 1. **Menjalankan Program**:
    
   - Pastikan Anda memiliki Python 3 terinstal di komputer Anda.
   - Simpan file kode ini sebagai `latihan3.py`.
   - Buka terminal atau command prompt, navigasikan ke folder tempat file `latihan3.py` disimpan, dan jalankan perintah berikut:
     
```PYTHON
     python3 latihan3.py
````

2. **Interaksi dengan Program**:
   
   - **Menu Tarik Uang**: Masukkan "1" dan kemudian masukkan jumlah penarikan. Program akan memvalidasi saldo dan mengurangi saldo sesuai dengan jumlah penarikan.
   - **Menu Keluar**: Masukkan "2" untuk keluar dari program. Program akan menampilkan pesan perpisahan sebelum keluar.

## Penjelasan Kode

### 1. Inisialisasi Saldo
```PYTHON
saldo = 1000000
````

Saldo awal pengguna diatur sebesar Rp 1.000.000.

### 2. Fungsi tampilkan_menu
```PYTHON
def tampilkan_menu():
    print("\nSaldo saat ini: Rp", saldo)
    print("1. Tarik Uang")
    print("2. Keluar")
````

Fungsi ini menampilkan saldo pengguna dan dua opsi: Tarik Uang dan Keluar.

### 3. Loop Utama
Program menggunakan loop while yang berjalan terus-menerus hingga pengguna memilih untuk keluar.

- Pilihan 1 (Tarik Uang):
   Program meminta jumlah uang yang ingin ditarik.
   Jika jumlah yang diminta lebih besar dari saldo, program menampilkan pesan bahwa saldo tidak mencukupi.
   Jika saldo mencukupi, saldo dikurangi sesuai jumlah penarikan dan ditampilkan pesan "Penarikan berhasil!".
- Pilihan 2 (Keluar):
   Program akan menampilkan pesan terima kasih dan menghentikan loop, sehingga program berakhir.
- Input Tidak Valid:
   Jika pengguna memasukkan pilihan selain "1" atau "2", program akan menampilkan pesan error dan meminta pengguna untuk memasukkan pilihan yang valid.

## Contoh Output
Berikut adalah contoh tampilan saat program berjalan:
```PYTHON
Saldo saat ini: Rp 1000000
1. Tarik Uang
2. Keluar
Pilih menu (1/2): 1
Masukkan jumlah penarikan: 500000
Penarikan berhasil!

Saldo saat ini: Rp 500000
1. Tarik Uang
2. Keluar
Pilih menu (1/2): 2
Terima kasih telah menggunakan ATM!
````
- Pada contoh ini:
   Pengguna memilih opsi "Tarik Uang" dan memasukkan jumlah penarikan Rp 500.000. Program berhasil melakukan penarikan dan mengurangi saldo.
   Pengguna kemudian memilih opsi "Keluar" untuk mengakhiri program.

## Berikut adalah hasin screenshot visual studio code

![WhatsApp Image 2024-10-31 at 22 12 01_b45186e2](https://github.com/user-attachments/assets/9151d782-3561-4643-a8f9-f50b7ab4c8b5)











  























































