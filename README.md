# Cara-Menginstall-Proxmox
Ini akan menjelaskan langkah-langkah untuk mengisntall Proxmox 

DASAR TEORI
--

Proxmox VE (Virtual Environment) adalah sebuah distro Linux virtualisasi berbasis Debian 64 bit) yang mengusung OpenZV dan KVM, dengan KVM kita tidak hanya bisa menginstall linux saja akan tetapi Operating system windows pun bisa kita instal. Namun yang membuat istimewa dari proxmox adalah kemudahan dalam installasi dan administrasi berbasis Web.
Beberapa keuntungan menggunakan Proxmox sebagai berikut :
1. Kinerja terbaik.
2. Instalasi yang telah dioptimalkan, sehingga lebih cepat.
3. Mudah dalam manajemen. 
4. Cocok untuk kelas Enterprise.

LANGKAH – LANGKAH
--
- Download file iso proxmox.
Melakukan download iso proxmox melalui link webiste ini pilih file Proxmox VE. 7.2 Installer : https://www.proxmox.com/en/downloads 
![1](https://user-images.githubusercontent.com/90621908/203885222-5d014321-42d5-46b4-84e1-2c4b86963587.jpg)

- Install Proxmox pada VirtualBox
Pembuatan nama virtual machine yang akan dibuat. Selanjutnya klik next
![2](https://user-images.githubusercontent.com/90621908/203885226-242bcf42-94ec-4807-9ec3-734041c9a47e.jpg)

Kemudian setting memori yang dibutuhkan
![3](https://user-images.githubusercontent.com/90621908/203885228-b0996587-ae45-43ea-a7ff-ef250410fa74.jpg)

Pilih Virtual Hard Disk yang akan digunakan
![4](https://user-images.githubusercontent.com/90621908/203885229-62b688d4-99ca-4608-80ba-3b3a6ed2d99b.jpg)

Masukkan file iso yang sudah download tadi ke VirtualBox
![5](https://user-images.githubusercontent.com/90621908/203885231-38809c49-ec94-4896-a117-a1078f4431e3.jpg)

Selanjutnya klik Setting > Network ubah network menjadi Network Adapter
![6](https://user-images.githubusercontent.com/90621908/203885233-d6842fbe-1e2b-472f-86c6-a4a67e01b3c1.jpg)

Setelah selesai klik Start lalu pilih Install Proxmox VE
![7](https://user-images.githubusercontent.com/90621908/203885234-d376e6b2-b714-434a-a018-e4fa9fa8219c.jpg)

Kemudian tunggu beberapa saat, akan tampil seperti gambar dibawah. Lalu pilih I agree
![8](https://user-images.githubusercontent.com/90621908/203885235-73852f77-fec2-4a59-828b-7e50eebf22f3.jpg)

Pada pilihan Country pilih Indonesia kemudian pada Time Zone masukan Jakarta
![9](https://user-images.githubusercontent.com/90621908/203885237-836e2ba2-31de-4b49-8974-c37f91eff067.jpg)

Masukan Password dan Email
![10](https://user-images.githubusercontent.com/90621908/203885239-4e862934-b42c-41a1-b6c9-bc0b4a82bbeb.jpg)

Pada Hostname, masukan hostname yang di miliki, lalu pada IP Address, Gateway dan DNS telah terisi otomatis. Lalu klik Next kemudian tunggu Instalasi selesai
![11](https://user-images.githubusercontent.com/90621908/203885242-c3bede23-ca28-4956-90d7-8000db6848a4.jpg)

Setelah proses instalisasi berhasil klik reboot, akan tampil layar hitam pada layar Login masukan “root” Kemudian pada Password masukan password yang telah di buat
![12](https://user-images.githubusercontent.com/90621908/203885245-cb1f2a1f-ce00-4409-b598-dadefbb01002.jpg)

Buka Browser masukan IP yang di minta pada layar hitam yang telah di jalankan* Masukan IP lengkap dengan“https” karena jika tidak cocok maka Proxmox tidak akan terbuka
![13](https://user-images.githubusercontent.com/90621908/203885247-47df1f6c-89ac-4c58-8f07-171a6f97ca2d.jpg)

Jika sudah tampil form Proxmox VE Login masukan Username “root”, lalu pada Password masukan Password telah di buat
![14](https://user-images.githubusercontent.com/90621908/203885249-3d1b5793-ffdb-4bf6-bddc-915e89b2856c.jpg)

- Upload ISO

Yang pertama adalah klik nodenya contoh > klik PVE > klik hdd Local > Pilih menu ISO Images > upload ISO , tunggu proses selesai 
![15](https://user-images.githubusercontent.com/90621908/203885250-5db77a88-4569-46c5-b49b-87ccf106c13c.jpg)

Jika sudah selesai, akan muncul tampilan seperti berikut
![16](https://user-images.githubusercontent.com/90621908/203885253-f59b2e10-44dd-4a3e-9c40-80988f0a9349.jpg)

Pada menu ISO images akan ada ISO yang telah di upload yaitu ubuntu 18.04 server
![17](https://user-images.githubusercontent.com/90621908/203885254-ea8d678e-db7f-4061-9bb9-5da0f2f9608b.jpg)

- Create Virtual Machine

Pilih menu Create VM. Masukan nama sesuai keinginan, contoh Database Server. Lalu Klik Next
![18](https://user-images.githubusercontent.com/90621908/203885257-fcdc7804-dcf5-41cb-9813-9ca85bb1d534.jpg)

Pada bagian OS, masukan file iso yang ingin kalian gunakan. Dan isi type OS dan Versionnya. Sebagai contoh saya menggunakan ubuntu 20.04-live-server-amd64
![19](https://user-images.githubusercontent.com/90621908/203885262-37be1e91-0803-4440-bfa4-de4d0718004f.jpg)

Pada bagian system biarkan default saja lalu klik next
![20](https://user-images.githubusercontent.com/90621908/203885264-16102f45-b77a-4e67-9aea-262bda435396.jpg)

Selanjutnya adalah menentukan Harddisk. Tentukan ukuran disk yang ingin kalian guankan. Kalian juga bisa menentukan format disknya. Bisa menggunakan raw atau qcow2
![21](https://user-images.githubusercontent.com/90621908/203885265-6e790e74-01a2-4c47-86bf-c83b5c9d7f73.jpg)

Pada tab Memory, pilih berapa banyak ram untuk dialokasikan ke vm
![22](https://user-images.githubusercontent.com/90621908/203885266-de5f89ab-43ca-4b57-a0c9-9f1ddcc7af41.jpg)

Step terakhir adalah bagian network. Pilih network adapter yang ingin digunakan
![23](https://user-images.githubusercontent.com/90621908/203885270-c5cd4036-3408-4fc4-83d4-e9e09a647f59.jpg)

Semua konfigurasi untuk vm sudah untuk create VM. Pada tab confirm akan menampilkan kesimpulan config vm. Jika sudah oke, klik finish
![24](https://user-images.githubusercontent.com/90621908/203885274-85c8806a-347a-4669-aba4-27da8b9364b1.jpg)

- Install Linux

Install linux yang sudah dimasukkan pada proxmox seperti menginstall linux di virtual machine seperti biasanya
