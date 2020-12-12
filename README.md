# Jarkom_Modul4_Lapres
Laporan Resmi Praktikum Modul 4 Jaringan Komputer 2020  Kelompok C07 (0099 &amp; 0157)
# Pembahasan Jawaban
## VLSM
![alt text](https://github.com/NaufalRafi-hub/Jarkom_Modul4_Lapres/blob/main/imageprak4/VLSM_table.png)
### langkah 1 menentukan jumlah IP yang dibutuhkan oleh tiap subnet dan melakukan labelling
maka akn mendapatkan subnet, jumlah IP, dan Netmask
### langkah 2 pembagian IP, dan dibenetuk seperti tree
![alt text](https://github.com/NaufalRafi-hub/Jarkom_Modul4_Lapres/blob/main/imageprak4/VLSM_Tree.jpeg)
tree  ini akan digunakan untuk routing dalam aplikasi cisco packet tracer
### langkah 3 subnetting untuk pemabagian IP sesuai kebutuhan subnet
![alt text](https://github.com/NaufalRafi-hub/Jarkom_Modul4_Lapres/blob/main/imageprak4/VLSM_table.png)

dari tree yang sudah di subnetting maka akan terdapat NID netmask dan broadcast ID
### langkah 4 routing dalam aplikasi CPT   
cara :
+ membuat topologi jaringan seperti di soal dari cloud, server, router, PC, Switch
+ sesudah membuat topologi jaringan lalu klik `options` lalu ke `preferences` dan centang `always show port labels`
+ menyetting interface sesuai jumlah subnet yang tadi dibuat

![alt text](https://github.com/NaufalRafi-hub/Jarkom_Modul4_Lapres/blob/main/imageprak4/img4.1.jpg)

+ misal menyambungkan router pasuruan dengan probolinggo : `termasuk subnet A4/30` , `lihat di dalam tree IP A4`, `IP SUBNET A4 : 192.168.4.0` , `buka interface router pasuruan lalu pilih port label yang menyambung dengan probolinggo` , `lalu isi dalam IPv4 Address bit terakhir ditambah +1, dan isi subnet mask sesuai netmask ip tersebut, dan tutup router pasuruan` , `buka router probolinggo` , `lakukan hal yang sama seperti router pasuruan tetapi dalam kolom IPv4 Address ditambah +2`
+ lakukan itu pada semua router 
+ sesudah menyetting interface, selanjutnya menyetting routing static
+ isi kolom network dan mask sesuai subnet yang dibuat 
+ isi kolom next hop isi IP yang ingin disambungkan di router tersebut
+ lalu untuk sambung kebalikannya isi network dan mask dengan `0.0.0.0` dan next hop ke arah router sebaliknya
+ lakukan static routing kedalam semua router
### langkah 5 melakukan ping test
cara : 
+ klik logo seperti bentuk surat dalam panel atas
+ pilih yang ingin di test ping
+ misal :
ROUTER SURABAYA KE PC BANYUWANGI

![alt text](https://github.com/NaufalRafi-hub/Jarkom_Modul4_Lapres/blob/main/imageprak4/img4.2.jpg)

+ akan menghasilkan output succesfull jika ping berhasil
+ jika tidak maka output akan keluar failed


## CIDR
### langkah 1 melakukan labelling subnet 
cara :
+ label subnet kelompok A terlebih dahulu

![alt text](https://github.com/NaufalRafi-hub/Jarkom_Modul4_Lapres/blob/main/imageprak4/img4.3.jpg)

+  label subnet kelompok B dan untuk mengtahui netmasknya dilihat dari subnet keloompok A yang terkecil dan dikurang 1

![alt text](https://github.com/NaufalRafi-hub/Jarkom_Modul4_Lapres/blob/main/imageprak4/img4.4.jpg)

+ label subnet kelompok C, untuk mengetahui netmasknya lakukan hal seperti menentukan netmask B

![alt text](https://github.com/NaufalRafi-hub/Jarkom_Modul4_Lapres/blob/main/imageprak4/img4.5.jpg)

menentukan c3 , dengan perbandingan B3 dan A11
menentukan C1 , dengan perbandingan B1 dan A12
menentukan C2 , dengan perbandingan B2 dan A4

+ label subnet kelompok D

![alt text](https://github.com/NaufalRafi-hub/Jarkom_Modul4_Lapres/blob/main/imageprak4/img4.6.jpg)

menentukan D1 , dengan perbandingan C1 dan C3
menentukan D2 , dengan perbandingan A7 dan C2

+ label subnet kelompok E

![alt text](https://github.com/NaufalRafi-hub/Jarkom_Modul4_Lapres/blob/main/imageprak4/img4.7.jpg)

menentukan E1 ,  dengan perbandingan D2 dan A5
menentukan E2 , dengan perbandingan D1 dan A8

+ label subnet kelompok F

![alt text](https://github.com/NaufalRafi-hub/Jarkom_Modul4_Lapres/blob/main/imageprak4/img4.8.jpg)

menentukan F1 , dengan perbandingan E1 dan A2

+ label subnet kelompok G

![alt text](https://github.com/NaufalRafi-hub/Jarkom_Modul4_Lapres/blob/main/imageprak4/img4.9.jpg)

menentukan G1 , dengan perbandingan F1 dan E2

### langkah 2 mendapatkan NID : 192.168.0.0 dan Netmask : /16 dari hasil labelling tersebut
### langkah 3 membuat tree sesuai labelling tadi

![alt text](https://github.com/NaufalRafi-hub/Jarkom_Modul4_Lapres/blob/main/imageprak4/CIDR_tree.jpeg)

### langkah 4 mendapatkan NID NETMASK DAN BROADCAST ADDRESS

![alt text](https://github.com/NaufalRafi-hub/Jarkom_Modul4_Lapres/blob/main/imageprak4/CIDR_table.png)


