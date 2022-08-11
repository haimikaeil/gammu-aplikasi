Installasi Gammu dan Seting Device

# Edit file gammurc seperti ini
 [gammu]
device = com4:
connection = at19200
note: device = com4, port modem yang saya gunakan.

# Buka cmd run as administrator
# Masuk ke direktori gammu/bin : cd /gammu/bin
# Ketik perintah  : gammu --identify



# Setelah itu kita coba kirim pesan dengan perintah
gammu --sendsms text 0899xxxxx  enter 
masukan pesan yang akan dikirim, kemudian tekan CTRL+Z untuk proses kirim


# Cek pesan telah terkirim ke nomer penerima atau belum, jika sudah seting device modem sudah benar
# gammu version : untuk melihat versi gamu yang digunakan

Integrasikan  Gammu dengan  Database Mysql

# Edit file smsdrc
# isikan no port di bawah ini
port = com4:
# isikan jenis connection di bawah ini
connection = at19200
[smsd]
service = mysql
logfile = gammulog
debuglevel = 0
phoneid = modem1
commtimeout = 30
sendtimeout = 600
send = yes
receive = yes
checksecurity = 0
#PIN = 1234
# -----------------------------
# Konfigurasi koneksi ke MySQL
# -----------------------------
pc = localhost
user = root
password =
database = gammu
# Cari file mysql.sql dari source gammu yang telah diwonload 
# Import file sql gamu, kedalam database mysql komputer anda, di sisni saya menggunakan XAMPP
# Restart Service gammu terlebih dahulu, setelah itu kita coba test kirim sms dari web browser.

Kirim Pesan Melalui Web Browser dengan Aplikasi PHP

Setelah langkah -langkah di atas kita bisa mencoba kirim sms via web dengan aplikasi php yang sudah di itegrasikan dengan gammu
