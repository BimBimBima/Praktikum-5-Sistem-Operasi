# Tugas 5 - Job Control

## 1. Eksekusi seluruh profile yang ada :
### a. Edit file profile /etc/profile dan tampilkan pesan sebagai berikut :
 echo “Profile dari /etc/profile”
 Untuk melihat file /etc/profile, kita bisa gunakan command sudo lalu menggunakan command nano untuk mengedit file tersebut.

![Screenshot 2024-09-25 214401](https://github.com/user-attachments/assets/1007e5cb-d346-463f-bef9-ed3d9422f7f7)

![Screenshot 2024-09-25 210350](https://github.com/user-attachments/assets/c10cebf2-a0cd-4f2b-8ede-347d167066e9)



### b.  Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu :
/home/stD02001/.bash_profile /home/. stD02001/.bash_login /home/mahasiswa/.profile /home/mahasiswa/.bashrc
Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile :

echo “Profile dari .bash_profile”

Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang bersangkutan.

![Screenshot 2024-09-25 215412](https://github.com/user-attachments/assets/fd621bda-48c6-4755-9d2a-dd19cfe846a0)

![Screenshot 2024-09-25 215314](https://github.com/user-attachments/assets/e40f535a-e4a4-4e5e-96ed-f6610acedcc6)

![Screenshot 2024-09-25 215403](https://github.com/user-attachments/assets/d923d227-feba-4c07-b299-1eab5a658605)

echo "Profile dari .bash_login"

![Screenshot 2024-09-25 215638](https://github.com/user-attachments/assets/5293d877-cf2e-4fe8-ac99-20db72a7e633)

![Screenshot 2024-09-25 215608](https://github.com/user-attachments/assets/6e462036-f46d-4858-a8ce-54830d875cba)

![Screenshot 2024-09-25 215647](https://github.com/user-attachments/assets/13cc243e-7b7d-4cb1-b5b5-5633d968413c)

echo "Profile dari .profile"

![Screenshot 2024-09-25 215815](https://github.com/user-attachments/assets/3bf51a02-1ffe-46af-b78d-faa8ff6e9d17)

echo "Profile dari .bashrc"

![Screenshot 2024-09-25 220041](https://github.com/user-attachments/assets/dc567e99-13a9-430c-b837-cd2b8c7a9ff2)

### c.  Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut:
$ su mahasiswa $ exit
kemudian gunakan opsi – sebagai berikut :
$ su – mahasiswa $ exit
Jelaskan perbedaan kedua utilitas tersebut. 

![Screenshot 2024-09-25 220819](https://github.com/user-attachments/assets/96e5ec17-2f22-47ec-9b34-eaef4bd03919)

Perintah su (substitute user) digunakan untuk berpindah pengguna dalam sistem Linux.

Sedangkan, jika menggunakan su - bima, perintah ini tidak hanya mengganti pengguna tetapi juga memuat seluruh lingkungan pengguna bima.

## 2. Prompt String (PS)
### a.  Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell
PS1=‟> „
export PS1

![Screenshot 2024-09-25 222630](https://github.com/user-attachments/assets/d9127f83-4274-49a7-a6f4-fd9052d29bdc)

![Screenshot 2024-09-25 222415](https://github.com/user-attachments/assets/198c1f1f-da51-4f95-a592-c745c63cbc27)

### b. Eksperimen hasil PS1 :
$ PS1=“\! > “
69 > PS1=”\d > “
Mon Sep 23 > PS1=”\t > “ 
10:10:20 > PS1=”Saya=\u > “ 
Saya=mahasiswa > PS1=”\w >”
~ > PS1=\h >”

![Screenshot 2024-09-25 223421](https://github.com/user-attachments/assets/af4425b0-2053-48c3-9059-5388a12815cb)

## 3. Logout
Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout

Echo “Terima kasih atas sesi yang diberikan” 

Sleep 5

clear

![Screenshot 2024-09-25 223938](https://github.com/user-attachments/assets/c80f5567-3663-4b30-ba12-1d5f24198fe5)
![Screenshot 2024-09-25 223917](https://github.com/user-attachments/assets/aa4f9585-1486-438b-93aa-0c6c722b5a72)
![Screenshot 2024-09-25 224300](https://github.com/user-attachments/assets/2b01bc31-05ec-4279-802a-4a8164547b0a)

## 4. Bash script
### a.  Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing :
p1.sh 

#! /bin/bash 

echo “Program p1” 

ls –l 

p2.sh 

#! /bin/bash 

echo “Program p2” 

who 

p3.sh 

#! /bin/bash 

echo “Program p3” 

ps x

![Screenshot 2024-09-25 230045](https://github.com/user-attachments/assets/682226d4-ee4f-486f-94ac-ee24853c2b20)

![Screenshot 2024-09-25 225831](https://github.com/user-attachments/assets/58340f99-b69f-452b-aac9-c335f0dcc917)

![Screenshot 2024-09-25 230050](https://github.com/user-attachments/assets/444d4581-a412-4d80-b25c-907661968344)

![Screenshot 2024-09-25 225911](https://github.com/user-attachments/assets/3d7138c8-e646-4434-93bd-abab636bc5c7)

![Screenshot 2024-09-25 230153](https://github.com/user-attachments/assets/1f252351-7f0e-4b64-bade-f460a337b509)

![Screenshot 2024-09-25 230317](https://github.com/user-attachments/assets/c572b954-95c9-4088-a006-1b051565d68d)

### b.Jalankan script tersebut sebagai berikut :
$  ./p1.sh ; ./p3.sh ; ./p2.sh 

$  ./p1.sh & 

$  ./p1.sh $ ./p2.sh & ./p3.sh & 

$  ( ./p1.sh ; ./p3.sh ) &

![Screenshot 2024-09-25 232848](https://github.com/user-attachments/assets/9347310b-3116-49fe-89e5-aa0279011c75)
![Screenshot 2024-09-25 232931](https://github.com/user-attachments/assets/0b866261-83bc-4b9e-84d0-95d299a56867)
![Screenshot 2024-09-25 233026](https://github.com/user-attachments/assets/cddd9822-834a-492a-b431-3a259aa087ca)
![Screenshot 2024-09-25 233138](https://github.com/user-attachments/assets/566f9968-a488-4a32-81d7-d8d27546e5bf)


## 5. Jobs
### a. Buat shell-script yang melakukan loop dengan nama pwaktu.sh, setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil.

#!/bin/bash 
while [ true ] 
do 
date >> hasil 
sleep 10 
done


![Screenshot 2024-09-25 235249](https://github.com/user-attachments/assets/fb33c94e-5070-4792-90e6-ed070aeab77d)

![Screenshot 2024-09-25 233730](https://github.com/user-attachments/assets/2b618ee8-093a-4087-b928-5c19c36c7229)


### b.  Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background sebagai berikut :
$ jobs 
$ find / -print > files 2>/dev/null & 
$ jobs

![Screenshot 2024-09-25 235458](https://github.com/user-attachments/assets/fc1fc103-dc37-40b5-b7bf-07c7837e1107)

### c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke background
$ fg %1 
$ bg

![Screenshot 2024-09-25 235804](https://github.com/user-attachments/assets/0dc0b4fb-dcc7-4aa2-8a3f-d4c50b0b9663)

### d.  Stop program background dengan utilitas kil
$ ps x 
$ kill [Nomor PID]

![Screenshot 2024-09-25 235912](https://github.com/user-attachments/assets/fc39348d-333a-4816-82f1-927cfc58a780)

untuk menjalankan command kill, kita harus mencari nomor PID nya dalam command "ps x"

![Screenshot 2024-09-26 000159](https://github.com/user-attachments/assets/dc0e17de-6fe9-42bf-9444-d6c3239ab6fb)

jika berhasil akan muncul tulisan "Terminated ./pwaktu.sh" seperti gambar dibawah
![Screenshot 2024-09-26 000233](https://github.com/user-attachments/assets/de403ca5-207f-44db-8350-15a6bc2f9c7c)

## 6. History
### a. Ganti nilai HISTSIZE dari 1000 menjadi 20
$ HISTSIZE=20
$ h
![Screenshot 2024-09-26 000826](https://github.com/user-attachments/assets/164f4c7d-4fb7-41fe-94a6-8a172008fb71)

### b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir dilakukan
$ !-5

![Screenshot 2024-09-26 002055](https://github.com/user-attachments/assets/56145658-dd32-4c75-9ff7-8b3e9dcd05d2)


### c. Ulangi instruksi yang terakhir.  Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer
$ !!

![Screenshot 2024-09-26 002101](https://github.com/user-attachments/assets/288be5f0-89d9-451a-850f-0c321bb56085)

### d.  Ulangi instruksi pada history bufer nomor 150
$ !150

![Screenshot 2024-09-26 002158](https://github.com/user-attachments/assets/6c2572b7-c6e8-4e9a-8fdc-87c9e9875c4a)

### e.  Ulangi instruksi dengan prefix “ls”
$ !ls

![Screenshot 2024-09-26 002249](https://github.com/user-attachments/assets/df884a95-cab7-4f5e-9113-731062542ee3)

