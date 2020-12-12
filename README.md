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
### langkah 1 mengelompokkan 
![alt text](https://github.com/NaufalRafi-hub/Jarkom_Modul4_Lapres/blob/main/imageprak4/CIDR_Diagram.jpeg)
cara :
+ mengelompokkan dengan yang A terlebih dahulu
+ mengelompokkan subnet dari yang terjauh dari surabaya
+ 
