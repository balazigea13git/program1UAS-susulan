# daftar-nila.py
from view.input_nilai import *

dataMhs = {}

def tambah_data():
    global dataMhs
    nama = input_nama()
    nim = input_nim()
    nilaiTugas = input_nilaiTugas()
    nilaiUts = input_nilaiUas()
    nilaiUas = input_nilaiUas()
    nilaiAkhir = (0.30 * nilaiTugas) + (0.35 * nilaiUts) + (0.35 * nilaiUas)
    dataMhs[nama] = nim, nilaiTugas, nilaiUts, nilaiUas, nilaiAkhir
    print("\nData Berhasil Ditambahkan!")
    return dataMhs

def ubah_data():
    nama = input("Masukkan Nama: ")
    if nama in dataMhs.keys():
        nim           = input_nim()
        nilaiTugas    = input_nilaiTugas()
        nilaiUts      = input_nilaiUts()
        nilaiUas      = input_nilaiUas()
        nilaiAkhir    = (0.30 * nilaiTugas) + (0.35 * nilaiUts) + (0.35 * nilaiUas)
        dataMhs[nama]  = nim, nilaiTugas, nilaiUts, nilaiUas, nilaiAkhir
        print("\nData Berhasil Di Update!")
    else:
        print("Data tidak ditemukan!")

def hapus_data():
    nama = input("Masukkan Nama:  ")
    if nama in dataMhs.keys():
        del dataMhs[nama]
        print("Data",nama,"Telah dihapus!")
    else:
        print("Data Mahasiswa Tidak Ada".format(nama))
        
#input_nilay.py
def input_nama():
    global nama
    nama = input("Masukkan Nama        : ")
    return nama

def input_nim():
    global nim
    nim = input("Masukkan NIM         : ")
    return nim

def input_nilaiTugas():
    global nilaiTugas
    nilaiTugas = int(input("Masukkan Nilai Tugas : "))
    return nilaiTugas

def input_nilaiUts():
    global nilaiUts
    nilaiUts = int(input("Masukkan Nilai UTS   : "))
    return nilaiUts

def input_nilaiUas():
    global nilaiUas
    nilaiUas = int(input("Masukkan Nilai UAS   : "))
    return nilaiUas
    

        
        
