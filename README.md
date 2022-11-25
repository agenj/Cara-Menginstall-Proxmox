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

- Install Proxmox pada VirtualBox
Pembuatan nama virtual machine yang akan dibuat. Selanjutnya klik next

Kemudian setting memori yang dibutuhkan

Pilih Virtual Hard Disk yang akan digunakan

Masukkan file iso yang sudah download tadi ke VirtualBox

Selanjutnya klik Setting > Network ubah network menjadi Network Adapter

Setelah selesai klik Start lalu pilih Install Proxmox VE

Kemudian tunggu beberapa saat, akan tampil seperti gambar dibawah. Lalu pilih I agree

Pada pilihan Country pilih Indonesia kemudian pada Time Zone masukan Jakarta

Masukan Password dan Email

Pada Hostname, masukan hostname yang di miliki, lalu pada IP Address, Gateway dan DNS telah terisi otomatis. Lalu klik Next kemudian tunggu Instalasi selesai

Setelah proses instalisasi berhasil klik reboot, akan tampil layar hitam pada layar Login masukan “root” Kemudian pada Password masukan password yang telah di buat 

Buka Browser masukan IP yang di minta pada layar hitam yang telah di jalankan* Masukan IP lengkap dengan“https” karena jika tidak cocok maka Proxmox tidak akan terbuka

Jika sudah tampil form Proxmox VE Login masukan Username “root”, lalu pada Password masukan Password telah di buat

- Upload ISO

Yang pertama adalah klik nodenya contoh > klik PVE > klik hdd Local > Pilih menu ISO Images > upload ISO , tunggu proses selesai 

Jika sudah selesai, akan muncul tampilan seperti berikut

Pada menu ISO images akan ada ISO yang telah di upload yaitu ubuntu 18.04 server

- Create Virtual Machine

Pilih menu Create VM. Masukan nama sesuai keinginan, contoh Database Server. Lalu Klik Next

Pada bagian OS, masukan file iso yang ingin kalian gunakan. Dan isi type OS dan Versionnya. Sebagai contoh saya menggunakan ubuntu 20.04-live-server-amd64

Pada bagian system biarkan default saja lalu klik next

Selanjutnya adalah menentukan Harddisk. Tentukan ukuran disk yang ingin kalian guankan. Kalian juga bisa menentukan format disknya. Bisa menggunakan raw atau qcow2

Pada tab Memory, pilih berapa banyak ram untuk dialokasikan ke vm

Step terakhir adalah bagian network. Pilih network adapter yang ingin digunakan

Semua konfigurasi untuk vm sudah untuk create VM. Pada tab confirm akan menampilkan kesimpulan config vm. Jika sudah oke, klik finish

- Install Linux

Install linux yang sudah dimasukkan pada proxmox seperti menginstall linux di virtual machine seperti biasanya
