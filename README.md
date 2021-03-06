# TUGAS PERTEMUAN 11 DAN PENJELASAN 
| Nama | kelas | Nim | Matkul |
| -- | --- | ---- | ----------- |
| Heri Anto Simamora | TI.21.C.1 | 312110365 | Bahasa Perograman |

## DAFTAR ISI 
| No | ISI | PENJELASAN |
| -- | --- | ---------- |
| 1. | Latihan   | [penjelasan](#Latihan) |
| 2. | Praktikum  | [penjelasan](#praktikum) |

## LATIHAN
![gambar1](gmbr/ss1.png.png)

## SOURCE CODE LATIHAN 
``` pyhton
#mengubah function menggunakan lambda
import math
def a(x):
    return x ** 2

lambda x: x ** 2

print("1. Mengubah function menggunakan Lambda \n   def a(x): \n \t   return x ** 2")
print("   Hasil : lambda x: x ** 2")

def b(x, y):
    return math.sqrt(x ** 2 + y ** 2)

lambda x, y: math.sqrt(x ** 2 + y ** 2)

print("________________________________________")
print("2. Mengubah function menggunakan Lambda \n   def b(x, y): \n \t   return math.sqrt(x ** 2 + y ** 2)")
print("   Hasil : lambda x, y: math.sqrt(x ** 2 + y ** 2))")

def c(*args):
    return sum(args) / len(args)

lambda *args: sum(args) / len(args)

print("________________________________________")
print("3. Mengubah function menggunakan Lambda \n   def c(*args): \n \t   return sum(args) / len(args)")
print("   Hasil : lambda *args: sum(args) / len(args))")

def d(s):
    return "".join(set(s))

lambda s: "".join(set(s))

print("________________________________________")
print("4. Mengubah function menggunakan Lambda \n   def d(s): \n \t   return "".join(set(s))")
print("   Hasil : lambda s: "".join(set(s)))")

``` 

## HASIL KELUARAN DAN PENJELASAN

![gambar2](gmbr/ss2.png.png)

- Untuk memperluas daftar fungsi matematika digunakan import math<p>



## SOAL PRAKTIKUM 

![gambar3](gmbr/ss3.png.png)

## SOURCE CODE PRAKTIKUM 

``` pyhton 

data = {}

def tambah():
    print("Tambah Data")
    nama = input("Nama\t\t: ")
    nim = int(input("NIM\t\t: "))
    tugas = int(input("Nilai Tugas\t: "))
    uts = int(input("Nilai UTS\t: "))
    uas = int(input("Nilai UAS\t: "))
    nilaiakhir = (tugas * 0.3 + uts * 0.35 + uas * 0.35)
    data[nama] = nim, tugas, uts, uas, nilaiakhir


def tampilkan():
    if data.items():
        print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~| Daftar Nilai |~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
        print("_______________________________________________________________________________________")
        print("|  No  |      NIM      |      NAMA         |    TUGAS   |   UTS   |   UAS   | AKHIR  |")
        print("|______|_______________|___________________|____________|_________|_________|________|__")
        i = 0
        for a in data.items():
            i += 1
            print(f"| {i:4} | {a[0]:13s} | {a[1][0]:17} | {a[1][1]:10d} |  {a[1][2]:6d} | {a[1][2]:7d} | {a[1][4]:6.2f} | ")
    else:
        print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~| Daftar Nilai |~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
        print("_______________________________________________________________________________________")
        print("|  No  |      Nama     |      NIM      |   TUGAS  |   UTS   |   UAS   | Nilai Akhir  |")
        print("_______________________________________________________________________________________")
        print("|      |               |             Tidak Ada Data         |         |                |")
    print("____________________________________________________________________________________________")


def hapus():
    print("Hapus Data Nilai Mahasiswa")
    nama = input(" Masukan Nama\t:")
    if nama in data.keys():
        del data[nama]
        print()
        print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
        print("===| BERHASIL MENGHAPUS DATA |===")
        print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
    else:
        print("Data {0} tidak ada".format(nama))


def ubah():
    print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
    print("===| Edit Data Nilai Mahasiswa |===")
    print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
    nama = input("Masukan Nama\t\t: ")
    print("___________________________________")
    if nama in data.keys():
        nim = input("NIM baru\t\t\t: ")
        tugas = int(input("Nilai Tugas Baru\t: "))
        uts = int(input("Nilai UTS Baru\t\t: "))
        uas = int(input("Nilai UAS Baru\t\t: "))
        nilaiakhir = (tugas * 30 / 100 + uts * 35 / 100 + uas * 35 / 100)
        data[nama] = nim, tugas, uts, uas, nilaiakhir
        print()
        print("<><><><><><><><><><><><><><><><>")
        print("====| BERHASIL MENGUBAH DATA |====")
        print("<><><><><><><><><><><><><><><><>")
    else:
        print("Data nilai {0} tidak ada ".format(nama))


while True:
    print("")
    print("|_<><><><><><><><><><><><><><><><><>_|")
    print("|~~~~~~~~| DATA MAHASISWA |~~~~~~~~~~|")
    print("|_<><><><><><><><><><><><><><><><><>_|")
    x = input("1.| Tampilkan Data \n2.| Tambah Data \n3.| Ubah Data \n4.| Hapus Data \n0.| Keluar Aplikasi \nPilih menu : ")
    if x.lower() == "1":
        tampilkan()
    elif x.lower() == "2":
        tambah()
    elif x.lower() == "3":
        ubah()
    elif x.lower() == "4":
        hapus()
    elif x.lower() == "0":
        print()
        print("<><><><><><><><><><><><><><><><>")
        print("====== KELUAR DARI PROGRAM ======")
        print("<><><><><><><><><><><><><><><><>")
        break

    else:
        print()
        print("<><><><><><><><><><><><><><><><>")
        print("== Pilihan Anda Tidak Tersedia ==")
        print("== Pilihlah Menu Yang Tersedia ==")
        print("<><><><><><><><><><><><><><><><>")

``` 

## HASIL KELUARAN DAN PENJELASAN 

- Buatlah kamus yang akan diinput oleh data<p>
```pyhton
data = {}
```

Ketika program di run pada pertama kali, maka akan muncul tampilan seperti ini :<p>

![gambar4](gmbr/ss4.png.png)

- Terdapat 5 pilihan menu yaitu :<p>
  1 Tampilkan Data<p>
  2 Tambah Data <p>
  3 Ubah Data <p>
  4 Hapus Data<p>
  0 Keluar Aplikasi<p>

- Tampilkan Data <p>
System akan menjalankan fitur ini ketika user mengetikkan perintah 1 pada pilihan Pilih Menu (1-2-3-4-5) Inilah tampilan fitur Tampilkan Data :<p>

![gambar5](gmbr/ss8.png.png)

- Tambah Data<p>
System akan menjalankan fitur ini ketika user mengetikkan perintah 2 pada pilihan Pilih Menu (1-2-3-4-5) dan kita bisa menambahkan data pada program Inilah tampilan fitur Tambah Data :<p>

![gambar6](gmbr/ss5.png.png)

- Ubah Data <p>
System akan menjalankan fitur ini ketika pengguna mengetikkan 3 perintah pada pilihan Pilih Menu (1-2-3-4-5)
Pada fitur ini user akan diminta untuk memilih data siapa yang akan diubah dan data apa yang akan dirubah Setelah user memilih data, Misalnya user ingin merubah NIM dari mahasiswa dengan nama heri , Maka akan muncul tampilan seperti ini :<p>

![gambar7](gmbr/ss6.png.png)

- Hapus Data <p>
System akan menjalankan fitur ini ketika pengguna mengetikkan 4 perintah pada pilihan Pilih Menu (1-2-3-4-5) Sebelum saya menjalankan fitur ini, saya akan menambahkan 1 data lagi dengan nama simamora dan saya menghapus data heri <p>

![gambar8](gmbr/ss7.png.png)

- Keluar Aplikasi
System akan menjalankan fitur ini ketika pengguna mengetikkan 0 perintah pada pilihan Pilih Menu (1-2-3-4-5) program akan terhenti dan keluar dari program yang dijalankan <p>

![gambar9](gmbr/ss9.png.png)

## FLOWCHART PRAKTIKUM 

![gambar10](gmbr/ss10.png.png)












