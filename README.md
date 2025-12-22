# Dokumentasi Menjalankan Project Web GIS Menggunakan Python Server

## 1. Deskripsi Project

Project **Web GIS Dashboard Medical** merupakan aplikasi web sederhana berbasis **HTML** yang menampilkan data rumah sakit (format CSV) pada wilayah Kota Bandung. Project ini dijalankan menggunakan **Python HTTP Server** agar file dapat diakses melalui browser secara lokal.

---

## 2. Prasyarat (Requirements)

Sebelum menjalankan project, pastikan sistem telah memenuhi persyaratan berikut:

### 2.1 Software

* **Python** versi 3.x
* **Git** (opsional, untuk clone repository)
* **Web Browser** (Google Chrome, Firefox, Edge, dll)

### 2.2 Struktur Folder Project

Pastikan struktur folder project seperti berikut:

```
app-web/
│── index.html
│── data/
│   ├── rs_bandung_lengkap.csv
│   ├── rs_bgd.csv
│   └── rumah_sakit_di_kota_bandung_2.csv
```

---

## 3. Menjalankan Project dengan Python Server

### 3.1 Masuk ke Direktori Project

Buka **Command Prompt / PowerShell**, lalu arahkan ke folder project:

```bash
cd D:\PROJECT_ALL\PROJECT_WEB_GIS\app-web
```

Pastikan file `index.html` berada di direktori tersebut.

---

### 3.2 Menjalankan Python HTTP Server

#### Opsi A: Python 3 (Direkomendasikan)

```bash
python -m http.server 8000
```

Jika berhasil, akan muncul output seperti:

```text
Serving HTTP on :: port 8000 (http://[::]:8000/) ...
```

#### Opsi B: Jika Python tidak terdeteksi

Cek versi Python terlebih dahulu:

```bash
python --version
```

atau

```bash
py --version
```

Jika menggunakan launcher Python:

```bash
py -m http.server 8000
```

---

## 4. Mengakses Aplikasi di Browser

Buka browser, lalu akses:

```
http://localhost:8000
```

atau langsung ke file utama:

```
http://localhost:8000/index.html
```

Jika server berjalan dengan benar, halaman Web GIS akan tampil dan data CSV dapat diakses.

---

## 5. Menghentikan Server

Untuk menghentikan server Python:

* Kembali ke terminal
* Tekan **Ctrl + C**

Server akan berhenti dan port tidak lagi digunakan.

---

## 6. Troubleshooting

### 6.1 Halaman Tidak Muncul

* Pastikan server masih berjalan
* Pastikan port `8000` tidak digunakan aplikasi lain
* Cek kembali lokasi `index.html`

### 6.2 File CSV Tidak Terbaca

* Pastikan path folder `data/` benar
* Jangan membuka `index.html` langsung (double click)
* Gunakan **Python server** agar fetch CSV tidak diblokir browser (CORS)

---

## 7. Catatan Tambahan

* Python server ini **hanya untuk development / testing**
* Tidak disarankan untuk production
* Cocok untuk demo project, tugas kuliah, dan pengembangan Web GIS lokal

---

## 8. Kesimpulan

Dengan menggunakan **Python HTTP Server**, project Web GIS dapat dijalankan secara lokal tanpa konfigurasi server tambahan. Metode ini sederhana, ringan, dan sangat cocok untuk keperluan pengemban
