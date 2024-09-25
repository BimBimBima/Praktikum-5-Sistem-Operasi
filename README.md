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



