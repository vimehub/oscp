# OSCP — Open Source Code Project Scanner

🔹 Deskripsi

OSCP (Open Source Code Project Scanner) adalah tool Python yang dirancang untuk membantu menemukan data sensitif yang terekspos pada website atau aplikasi web. Tool ini dapat mendeteksi:

- API Key & Token
- Password dan kredensial database
- File konfigurasi dan file sensitif
- Alamat email dan IP internal
- Data finansial (Stripe, PayPal, Braintree)
- File backup, log, dan environment

> ⚠️ Tool ini hanya untuk website yang kamu miliki atau yang sudah ada izin eksplisit untuk di-scan. Penggunaan tanpa izin dapat melanggar hukum.

🔹 Fitur Utama

- Mendukung scan dengan sesi terautentikasi menggunakan cookie.
- Scan multi-thread (default 10 thread).
- Timeout request dapat diatur.
- Deteksi pola regex untuk API Key, Token, Password, Database, Email, IP Internal, dan file sensitif.
- Deteksi file sensitif yang terekspos secara langsung.
- Mencari URL tambahan melalui sitemap, robots.txt, dan common path.
- Menampilkan hasil secara real-time dengan warna.
- Membuat laporan JSON lengkap dengan ringkasan risiko.

🔹 Instalasi

Clone repository ini:

```
git clone https://github.com/vimehub/oscp.git
cd oscp
```

PENGGUNAAN:

```
python3 oscp.py [OPSI] URL_TARGET
```

OPSI:

```
-s, --session SESSION    Cookie sesi untuk scan terautentikasi
-t, --threads THREADS    Jumlah thread (default: 10)
--timeout TIMEOUT        Timeout request dalam detik (default: 10)
-o, --output FILE        File output untuk laporan JSON
-h, --help               Tampilkan pesan bantuan ini
```

CONTOH:

Scan dasar:

```
python3 oscp.py https://example.com
```

Scan dengan cookie sesi:

```
python3 oscp.py -s "nilai_cookie_sesi" https://example.com
```

Thread dan timeout kustom:

```
python3 oscp.py -t 5 --timeout 15 https://example.com
```

Simpan laporan ke file:

```
python3 oscp.py -o laporan_scan.json https://example.com
```

FITUR:

- Deteksi API Key & Token
- Scan kredensial database
- Penemuan file sensitif
- Deteksi file konfigurasi
- Alamat email dan IP internal
- Scan data finansial
- Scan multi-thread
- Pembuatan laporan JSON
