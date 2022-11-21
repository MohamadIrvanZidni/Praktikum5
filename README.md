# Praktikum5

Repository ini digunakan untuk memenuhi Tugas Bahasa Pemrograman Pertemuan-9

Nama    : Mohamad Irvan Zidni

NIM     : 312210308

Kelas   : TI.22.A.3

| No | Daftar Isi | Link |
| 1 | | |
| 2 | | |
| 3 | | |

1. Gunakan perulangan while untuk memasukkan data secara berulang
    data = []
    stop = False

    while(not stop):
        nama = input("Nama : ")
        nim = input("NIM : ")
        tugas = int(input("Nilai Tugas : "))
        uts = int(input("Nilai UTS : "))
        uas = int(input("Nilai UAS : "))
        akhir = (tugas * 30/100) + (uts * 35/100) + (uas * 35/100)

2. Gunakan perintah .append() untuk menambahkan setiap data ke dalam list
        data.append([nama,nim,tugas,uts,uas,int(akhir)])

3. Gunakan percabangan if untuk melakukan perulangan input data
        tanya = input('Tambahkan Data (y/t) ?')
        if (tanya == 't'):
            stop = True

Full Code :

    data = []
    stop = False

    while(not stop):
        nama = input("Nama : ")
        nim = input("NIM : ")
        tugas = int(input("Nilai Tugas : "))
        uts = int(input("Nilai UTS : "))
        uas = int(input("Nilai UAS : "))
        akhir = (tugas * 30/100) + (uts * 35/100) + (uas * 35/100)
        
        data.append([nama,nim,tugas,uts,uas,int(akhir)])
        
        tanya = input('Tambahkan Data (y/t) ?')
        if (tanya == 't'):
            stop = True
            
    print("______________________________________________________________")
    print("| No |    Nama      |  NIM  | Tugas |  UTS  |  UAS  |  Akhir |")
    print("--------------------------------------------------------------")

    i = 0

    for nilai in data:
        i += 1
        print("| {no}  | {nama:12s} | {nim:5s} | {tugas:5d} | {uts:5d} | {uas:5d} | {akhir:6.2f} |".format(no=i, nama=nilai[0], nim=nilai[1], tugas=nilai[2],uts=nilai[3],uas=nilai[4],akhir=nilai[5]))

    print("______________________________________________________________")