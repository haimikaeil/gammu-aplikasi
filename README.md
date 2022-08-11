Installasi Gammu dan Seting Device

Edit file gammurc seperti ini
 [gammu]
device = com4:
connection = at19200
note: device = com4, port modem yang saya gunakan.

Buka cmd run as administrator
Masuk ke direktori gammu
Ketik perintah  : gammu --identify



Setelah itu kita coba kirim pesan dengan perintah
gammu --sendsms text 0899xxxxx  enter 
masukan pesan yang akan dikirim, kemudian tekan CTRL+Z untuk proses kirim


Cek pesan telah terkirim ke nomer penerima atau belum, jika sudah seting device modem sudah benar
gammu version : untuk melihat versi gamu yang digunakan

Integrasikan  Gammu dengan  Database Mysql

Edit file smsdrc
[gammu]
isikan no port di bawah ini
port = com5:
isikan jenis connection di bawah ini
connection = at115200

[smsd]
service = mysql
logfile = 
debuglevel = 0
phoneid = Modem
commtimeout = 30
sendtimeout = 600
send = yes
receive = yes
checksecurity = 0
//PIN = 1234

-----------------------------
Konfigurasi koneksi ke MySQL
-----------------------------
pc = localhost
isikan user untuk akses ke MySQL
user = root
isikan password user untuk akses ke MySQL
password = system8
isikan nama database untuk Gammu
database = gammu

Kirim Pesan Melalui Web Browser dengan Aplikasi PHP bisa lihat repository saya https://github.com/haimikaeil/CMS-SMS-Gateway-GAMMU

Setelah langkah -langkah di atas kita bisa mencoba kirim sms via web dengan aplikasi php yang sudah di itegrasikan dengan gammu
