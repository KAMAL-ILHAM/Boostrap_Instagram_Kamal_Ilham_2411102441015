
## Pertanyaam README

### 1. Mengapa memilih konfigurasi Kolom (`col-*`) tertentu untuk tiap breakpoint?

Pemilihan konfigurasi kolom sangat menentukan kenyamanan pengguna di berbagai ukuran layar.
* **Mobile:** Penggunaan kelas `.col-12` membuat setiap elemen mengambil lebar penuh sehingga konten lebih mudah dibaca di layar sempit.
* **Tablet:** Kelas `.col-sm-6` atau `.col-md-4` dimanfaatkan untuk menampilkan 2–3 kolom sekaligus, memberi keseimbangan antara jumlah konten yang terlihat dan ukuran elemen.
* **Desktop:** Kelas `.col-lg-3` atau `.col-lg-4` digunakan untuk memanfaatkan lebar layar dengan menampilkan 3–4 kolom dalam satu baris.

Dengan cara ini, mobile tetap fokus pada **keterbacaan**, tablet menampilkan **konten lebih banyak** tanpa terasa padat, dan desktop menyajikan tampilan padat serta **efisien** menyerupai galeri.

---

### 2. Bagaimana kamu memastikan tombol Follow/ Edit Profile tetap mudah dijangkau di mobile? Jelaskan pendekatannya

Prinsip utamanya adalah **ergonomi pengguna**, khususnya **thumb zone**, yaitu area bawah dan tengah layar yang mudah dijangkau jempol saat menggunakan ponsel dengan satu tangan. Tombol aksi utama, seperti *Follow* atau *Edit Profile*, idealnya ditempatkan di area ini agar tidak menyulitkan pengguna.

Selain posisi, ukuran tombol juga dibuat cukup besar agar mudah ditekan tanpa risiko salah sentuh. Untuk tombol yang jarang dipakai, seperti pengaturan, bisa ditempatkan di bagian atas karena tidak sering diakses. Pendekatan ini memastikan tombol penting selalu dalam jangkauan, sementara tombol sekunder tetap tersedia tanpa mengganggu kenyamanan.

---

### 3. Jika postingan bertambah jadi 50, apa potensi masalah dan bagaimana solusi gridmu mengatasinya?

Bertambahnya postingan hingga 50 dapat menimbulkan dua masalah utama: **pengalaman pengguna (UX)** dan **performa**. Dari sisi UX, pengguna harus melakukan *scroll* panjang yang melelahkan. Dari sisi performa, memuat 50 gambar sekaligus akan memperlambat waktu *loading* dan menghabiskan data.

Solusi yang lebih tepat bukan pada grid itu sendiri, melainkan pada cara memuat konten. Grid tetap dipakai untuk menata layout, tetapi ditambah mekanisme **pagination** (misalnya 12 postingan per halaman) atau **infinite scroll dengan lazy loading**. Pagination lebih ringan dan terstruktur, sedangkan *infinite scroll* memberi pengalaman mulus seperti Instagram. Dengan kombinasi grid yang rapi dan teknik pemuatan bertahap, masalah UX dan performa dapat diminimalisasi.

# kamllhm25 • Instagram Bootstrap Clone 📸

Aplikasi web sederhana berupa replika (clone) halaman profil Instagram yang dibuat menggunakan HTML, CSS, dan framework **Bootstrap 5**.

---

## 🚀 Penjelasan Singkat

Proyek ini adalah implementasi *frontend* dari tampilan halaman profil Instagram, berfokus pada desain yang **responsif** agar dapat ditampilkan dengan baik di perangkat seluler dan desktop.

* **Tujuan:** Untuk mendemonstrasikan kemampuan layouting menggunakan Bootstrap dan styling CSS kustom.
* **Fitur Utama:**
    * Sidebar navigasi untuk tampilan desktop.
    * Header dan navbar atas/bawah yang spesifik untuk tampilan mobile.
    * Tampilan profil (foto profil, statistik, bio).
    * Highlight cerita (Story Highlights) horizontal.
    * Grid postingan foto/video dengan efek *overlay* hover.

---

## 📁 Struktur File

Proyek ini mengasumsikan struktur file dasar sebagai berikut:

```
.
├── index.html        # File utama yang berisi semua kode HTML.
├── assets/
│   ├── style.css     # File CSS kustom untuk styling tambahan.
│   └── img/          # Direktori untuk gambar-gambar (foto profil, highlight, postingan).
│       ├── fotoprofil.jpg
│       ├── highlight1.jpg
│       ├── ...
│       └── gambar12.jpg
└── README.md
```
---

## 🛠️ Build dan Run

Karena ini adalah aplikasi *frontend* statis (hanya HTML dan CSS), Anda tidak memerlukan proses *build* yang kompleks.

### Cara Menjalankan (Run)

1.  **Kloning/Unduh Repositori:**
    ```bash
    # Jika menggunakan git:
    git clone [URL_REPO_ANDA]
    cd [NAMA_FOLDER_REPO]
    ```
    *(Ganti `[URL_REPO_ANDA]` dan `[NAMA_FOLDER_REPO]` dengan detail proyek Anda).*
2.  **Buka File:** Cukup buka file `index.html` dengan *browser* modern apa pun (seperti Chrome, Firefox, Edge).
    ```bash
    # Contoh perintah (bisa berbeda tergantung OS Anda)
    open index.html 
    ```
Aplikasi akan langsung berjalan di browser Anda.

---

## 🔗 Dependensi (Dependencies)

Proyek ini memanfaatkan beberapa sumber daya eksternal yang di-link melalui **CDN (Content Delivery Network)**, serta satu file CSS lokal.

| Nama Dependensi | Tipe | Sumber | Keterangan |
| :--- | :--- | :--- | :--- |
| **Bootstrap 5.3.3** | CSS | CDN (`https://cdn.jsdelivr.net/...`) | Digunakan untuk layout responsif (Grid System) dan komponen UI. |
| **Font Awesome 6.5.1** | CSS | CDN (`https://cdnjs.cloudflare.com/...`) | Digunakan untuk ikon-ikon (seperti ikon navigasi, hati, komentar, dll.). |
| **Google Fonts (Grand Hotel)** | Font | CDN (`https://fonts.googleapis.com/...`) | Digunakan untuk gaya logo Instagram. |
| **`assets/style.css`** | CSS | Lokal | File styling kustom yang berisi penyesuaian untuk mencapai tampilan seperti Instagram. |
| **Gambar di `assets/img/`** | Aset | Lokal | Semua gambar yang digunakan untuk profil, highlight, dan postingan. |

**Catatan:** Tidak ada JavaScript eksternal atau lokal yang digunakan dalam implementasi ini, fokusnya hanya pada struktur dan styling.