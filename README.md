# 🚀 **AsyncNet Auditor**

**Advanced Multi-Threaded Network Scanner & Proxy Auditor for Windows**

AsyncNet Auditor adalah aplikasi Windows canggih yang dirancang untuk melakukan **pemindaian jaringan**, **validasi proxy**, **pengujian kredensial**, dan **audit server** secara cepat dan akurat menggunakan **arsitektur multithreading** berbasis *Parallel OTL* dan *TThread*, aplikasi ini memungkinkan proses scanning berskala besar tanpa membuat UI freeze, lengkap dengan monitoring status, progress, dan pencatatan log secara real-time.

---

## 📌 **Key Features**

### 🔍 **1. High-Performance Multi-Thread Scan**

* Memanfaatkan **OmniThreadLibrary (OTL)** & **TThread**
* Mendukung 10–500 thread paralel
* Zero freeze / non-blocking UI

### 🌐 **2. Proxy Checker Engine**

* Cek proxy HTTP / HTTPS
* Validasi respons, latency, dan status code
* Auto-rotate proxy (list-based)
* Menyimpan proxy valid ke file

### 🔑 **3. Credential & Login Pattern Testing**

* Cek username/password otomatis
* Support pola dinamis (regex & custom pattern)
* Status code result: Valid / Invalid / Timeout / Error

### 🧪 **4. URL Auditor & Server Info Extractor**

* GET/POST request
* Mendapatkan server header, country lookup, dan response time
* Mendeteksi status server (online/offline)

### 🧵 **5. Thread-Safe Synchronization**

* CriticalSection
* Mutex proxy list
* Queue UI di main thread (TThread.Queue)

### 📝 **6. Real-Time Logging**

* Monitoring lengkap pada:

  * Scan count
  * Active thread
  * Error count
  * Valid proxy
* Semua log dikirim ke **MemoResult** secara runtime

### 🎨 **7. Modern UI with AlphaControls**

* Skin ringan & smooth
* ProgressBar beranimasi
* Status monitor lengkap

---

## 🛠 **Tech Stack**

| Komponen            | Keterangan                 |
| ------------------- | -------------------------- |
| Delphi VCL          | Core Application Framework |
| OmniThreadLibrary   | Parallel Tasks Engine      |
| Indy's IdHTTP + SSL | HTTP/HTTPS Networking      |
| WebView2            | Optional Web Loader        |
| AlphaControls       | UI Skinning                |
| Regex (TRegEx)      | Pattern Matching           |
| WinAPI + TLHelp32   | System & Process Utils     |

---

## ⚡ **Cara Menggunakan**

### 1. **Import daftar target**

Masuk folder \data\ edit list:

* list_ipaddress.txt IP (Address)
* list_username.txt (Username)
* list_password.txt (Password)
* list_http_proxy.txt (Proxy)
* list_ports.txt (Ports)

### 2. **Klik Start Scan**

Aplikasi akan:

* Membuat worker thread
* Mengambil 1 data per thread
* Mengirim request
* Mencatat hasil secara real-time

### 3. **Pantau Status**

Status akan muncul di panel:

* Scan Count
* Active Thread
* Valid Proxy
* Total Errors

### 5. **Export Result**

Hasil dapat disimpan otomatis menjadi:

* `output_exclude_types.txt`
* `output_include_types.txt`
* `output_regex_password.txt`
* `output_regex_submit.txt`
* `output_regex_text.txt`

---

## 📘 **Roadmap**

* [ ] Export to CSV/JSON
* [ ] Add WebSocket check
* [ ] Integrasi Laravel Rest API
* [ ] Logging ke SQLite

---

## 🤝 **Contributing**

Pull request sangat diterima — mulai dari perbaikan kecil sampai fitur baru.

---

## ⭐ **Support Project**

Jika aplikasi ini membantu, dukung dengan klik **Star ⭐** di GitHub Anda.
