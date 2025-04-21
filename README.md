CCTV Hunter v1 (Slow Scan)

CCTV Hunter v1 adalah tool Python untuk melakukan scanning terhadap IP publik guna mencari feed CCTV yang terbuka (tanpa autentikasi). Tool ini dapat mengambil screenshot dari feed video, menyimpannya ke lokal.


---

Fitur

Scanning IP acak dan port umum CCTV (81, 8080, 8000, dll)

Deteksi otomatis feed video (stream, mjpg, ipcam, dsb)

Screenshot feed menggunakan Chromium (headless)

Log semua CCTV ditemukan ke cctv_feeds.txt


---

Persiapan Sebelum Menjalankan

1. Install Paket di Termux atau Linux

Untuk Termux:

pkg update && pkg upgrade
pkg install python ffmpeg chromium git wget -y
pip install selenium requests
termux-setup-storage

Untuk Linux (Debian/Ubuntu):

sudo apt update && sudo apt upgrade
sudo apt install python3 python3-pip ffmpeg chromium-browser git -y
pip3 install selenium requests


---

2. Download Script

Clone dari GitHub (jika tersedia):

git clone https://github.com/andirozaS-SKD/cctv-hunter
cd cctv-hunter


---

Cara Menjalankan

Setelah semua dependensi terpasang dan konfigurasi selesai:

python run.py


---

Output

Screenshot Feed: Disimpan di folder ./screenshot

Log Feed: Dicatat di cctv_feeds.txt


---

Contoh Tampilan

[+] CCTV: http://123.45.67.89:8080/
    -> Feed: http://123.45.67.89:8080/live/mjpg
[=] Screenshot disimpan ke ./screenshot/123.45.67.89_8080.png
[=] Dikirim ke Telegram


---

Catatan Penting

Script ini menggunakan Selenium + Chromium headless, pastikan chromedriver cocok dengan versi Chromium kamu.

Folder /sdcard bisa diakses di Termux setelah menjalankan termux-setup-storage.

Waktu scanning bisa lama tergantung koneksi dan IP yang ditemukan.



---

Disclaimer

> Tool ini hanya untuk tujuan edukasi dan riset keamanan jaringan.
Segala bentuk penyalahgunaan adalah tanggung jawab pengguna.



---

Author: Andiroza

GitHub: github.com/andirozaS-SKD

