# Tugas-Sistem-Operasi-Praktikum-6

Nama : Rasti Ayu Widianti
NIM : 09030282428044
Kelas : TK2B
Mata Kuliah : Sistem Operasi

1. Login sebagai studentOS dan lihat status proses, perhatikan kolom keluaran ps –au sebagai 
berikut :  
a. Sebutkan nama-nama proses yang bukan root  
b. Tulis PID dan COMMAND dari proses yang paling banyak menggunakan CPU time  
c. Sebutkan buyut proses dan PID dari proses tersebut . 
d. Sebutkan beberapa proses daemon  
e. Pada prompt login lakukan hal-hal sebagai berikut :  
$ csh   
$ who  
$ bash  
$ ls  
$ sh  
$ ps  
Sebutkan PID yang paling besar dan kemudian buat urut-urutan proses sampai ke PPID =1. 
Lakukan ^d atau exit atau logout sampai kembali muncul login: prompt
![p6 n01-1](https://github.com/user-attachments/assets/7ae5099e-c578-467e-9a4d-896b80ec4eef)
![p6 no1-2](https://github.com/user-attachments/assets/85d0a47f-bdaa-4085-9a5a-aa6b545e403d)

2. Modifikasi program prog.sh sebagai berikut :  
$ vi prog.sh  
#!/bin/sh  
trap “echo Hello Goodbye ; exit 0 “  1  2  3  15  
echo “Program berjalan …”  
while :  
do  
echo “X”  
sleep 20  
done 
Jalankan program tersebut sebagai background.  Coba lakukan kil dengan nomor sinyal 1, 2, 3 
dan 15 pada nomor PID proses tersebut.  Apakah proses berhenti atau tetap berjalan ? Nomor 
sinyal berapa yang digunakan untuk menghentikan proses diatas ?
![p6 no 2-1](https://github.com/user-attachments/assets/f8a93568-db77-428b-9ac4-cb80b3b4ac2c)
![p6 no2-2](https://github.com/user-attachments/assets/e75238c6-f213-42a7-a9d8-ec81433bb423)
![p6 n02-3](https://github.com/user-attachments/assets/91d6aa5b-5545-4376-94d2-e75e8d7a6ec7)

3. Modifikasi program  
myjob.sh. Buatlah trap sedemikian rupa, sehingga bila proses tersebut dihentikan (kil), otomatis 
file berkas akan terhapus.  
$ vi myjob.sh  
#!/bin/sh  
trap ______________________________  
i=1  
while :  
do  
find / -print > berkas  
sort berkas –o hasil  
echo “Proses selesai pada „date‟” >> proses.log  
sleep 60  
done  
$ kill –15 [Nomor PID]  
$ ls -l
![p6 n03-1](https://github.com/user-attachments/assets/edf5cb33-1304-4a07-9f67-317c303fd47f)
![p6 n03-2](https://github.com/user-attachments/assets/62e3708c-d7fd-4d47-8b57-1de3b7f28c46)
