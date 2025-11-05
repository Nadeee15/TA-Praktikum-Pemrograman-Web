# Praktikum Judul 2 — Workflow Git Website Portofolio

## Deskripsi
Proyek ini merupakan implementasi **Workflow Git (Git Workflow)** pada website portofolio hasil Percobaan 1.  
Kegiatan ini bertujuan agar mahasiswa memahami dan mampu menerapkan proses pengelolaan versi proyek menggunakan Git secara sistematis — mulai dari inisialisasi repository, pembuatan commit bertahap, pembuatan branch untuk eksperimen styling, penyelesaian konflik, hingga sinkronisasi akhir ke repository GitHub.

Melalui praktikum ini, mahasiswa tidak hanya mempelajari teori dasar Git, tetapi juga **menerapkannya secara langsung** dalam proyek web statis yang terdiri atas struktur file HTML, CSS, dan aset gambar pendukung.  
Setiap tahap commit dan branch dilakukan serta didokumentasikan secara runtut untuk menunjukkan penerapan alur kerja Git yang profesional, efisien, dan sesuai standar kolaborasi dalam pengembangan perangkat lunak.

---

## Hasil Screenshot

### 1. Inisialisasi Repository
![Inisialisasi Repository](./Screenshoot/WhatsApp%20Image%202025-11-05%20at%2017.57.8a.png)

Perintah `git init` digunakan untuk memulai repository Git di folder **TA-Praktikum-Pemrograman-Web**.  
Git akan membuat folder tersembunyi `.git` yang berfungsi menyimpan seluruh riwayat versi (commit log, branch, merge, dan sebagainya).  
Pesan *“Reinitialized existing Git repository”* menunjukkan bahwa folder ini sudah pernah diinisialisasi sebelumnya, dan Git hanya mengaktifkannya kembali.

---

### 2. Menambahkan Semua File ke Staging Area
![Menambahkan Semua File](./Screenshoot/WhatsApp%20Image%202025-11-05%20at%2017.58.23.png)

Perintah `git add .` menambahkan semua file di folder kerja ke *staging area*, yaitu tahap sebelum file disimpan permanen dalam commit.  
Titik (.) berarti semua file dan subfolder di direktori ini. Pada tahap ini, seluruh file di folder **Source Code** seperti `index.html`, `style.css`, dan gambar telah siap untuk di-commit.

---

### 3. Membuat Commit Pertama
![Commit Pertama](./Screenshoot/Screenshot%202025-11-05%2018.04.34.png)

Perintah `git commit -m "Judul 2"` digunakan untuk membuat commit pertama dalam proyek.  
Commit ini berfungsi sebagai titik awal (snapshot) dari seluruh file di folder **Praktikum Judul 2**.  
Git mencatat semua perubahan hasil `git add .`, termasuk file HTML, CSS, dan aset gambar.  
Hasil menunjukkan tujuh file baru dengan total 991 baris kode, menandakan bahwa struktur proyek telah tersimpan di histori versi Git dan siap untuk pengembangan selanjutnya.

---

### 4. Menampilkan Riwayat Commit
![Riwayat Commit](./Screenshoot/Screenshot%202025-11-05%2018.05.18.png)

Perintah `git log --graph --oneline --decorate --all` dijalankan sebelum tahap branch dan merge.  
Hasil menampilkan commit yang terdapat pada cabang utama (**main**) untuk memastikan seluruh perubahan awal tercatat dengan benar sebelum melanjutkan eksperimen styling.

---

### 5. Push ke Repository GitHub
![Push ke GitHub](./Screenshoot/Screenshot%202025-11-05%2018.06.39.png)

Setelah semua commit selesai di-buat di branch utama, perintah `git push` digunakan untuk mengunggah seluruh commit dari repositori lokal ke GitHub.  
Langkah ini memastikan setiap pembaruan, termasuk file proyek dan riwayat versinya, tersimpan secara online dan dapat diakses publik.

---

### 6. Membuat Branch Baru
![Branch Baru](./Screenshoot/Screenshot%202025-11-05%2018.07.45.png)

Branch baru bernama **style-experiment-peach** dibuat menggunakan perintah `git checkout -b style-experiment-peach`.  
Branch ini digunakan untuk melakukan eksperimen styling tanpa memengaruhi kode utama di branch **main**, sehingga proses pengembangan tetap aman dan terpisah.

---

### 7. Commit Section About
![Section About](./Screenshoot/Screenshot%202025-11-05%2018.11.14.png)

Tahap ini menambahkan *Section About* pada file `index.html` menggunakan perintah `git add` dan `git commit`.  
Bagian tersebut berisi profil singkat dan deskripsi diri mahasiswa Teknik Informatika Universitas Lampung.  
Commit terdokumentasi dengan pesan *“Percobaan 2: Tambah Section About (profil & deskripsi singkat)”*.

---

### 8. Commit Section Projects
![Section Projects](./Screenshoot/Screenshot%202025-11-05%2018.12.12.png)

Tahap ini menambahkan *Section Projects* ke dalam `index.html` untuk menampilkan daftar proyek yang telah dibuat.  
Bagian ini berisi dua proyek utama — **Smart Home** dan **Tickle Task** — lengkap dengan deskripsi, teknologi yang digunakan, serta gambar pendukung.  
Commit dilakukan dengan pesan *“Percobaan 2: Tambah Section Projects (kartu proyek & link proyek)”* sebagai dokumentasi perubahan tampilan portofolio.

---

### 9. Perubahan Font di Branch Main
![Perubahan Font](./Screenshoot/Screenshot%202025-11-05%2018.13.15.png)

Pada branch **main**, dilakukan perubahan styling di `style.css` dengan mengganti font menjadi **Arial**.  
Langkah ini dilakukan untuk melihat perbedaan tampilan antara branch utama dan branch eksperimen.  
Commit disimpan dengan pesan *“Ubah font ke Arial di main”*.

---

### 10. Percobaan Konflik di Branch Eksperimen
![Konflik Font](./Screenshoot/Screenshot%202025-11-05%2018.14.56.png)

Pada branch **style-experiment-peach**, font diganti menjadi **Poppins** dan ditambahkan komentar pembeda.  
Perbedaan ini menimbulkan konflik ketika dilakukan merge dengan branch utama.  
Commit terdokumentasi dengan pesan *“Konflik: ubah font ke Poppins di style-experiment-peach”*.

---

### 11. Simulasi Konflik dan Proses Merge
![Simulasi Merge](./Screenshoot/Screenshot%202025-11-05%2018.18.12.png)

Proses merge antara branch **main** dan **style-experiment-peach** menimbulkan konflik pada file `style.css`, karena:  
- Branch **main** menggunakan font Arial dengan background `#e3e3e3`.  
- Branch **style-experiment-peach** menggunakan font Poppins dengan tambahan komentar pembeda.  

Git menampilkan tanda konflik (`<<<<<<<`, `=======`, `>>>>>>>`) yang menandai bagian berbeda antar-branch.  
Konflik diselesaikan secara manual di Visual Studio Code sebelum melakukan commit penyelesaian.

---

### 12. Penyelesaian Konflik dan Merge Selesai
![Penyelesaian Merge](./Screenshoot/Screenshot%202025-11-05%2018.19.39.png)

Setelah konflik diselesaikan dengan memilih font **Poppins** sebagai hasil akhir, dilakukan commit dengan pesan:  
`Merge selesai: resolve conflict di style.css (pilih Poppins sebagai final)`  
Tahap ini menandai bahwa semua konflik telah terselesaikan dan hasil dari kedua branch berhasil digabungkan tanpa error.

---

### 13. Visualisasi Riwayat Commit
![Riwayat Merge](./Screenshoot/Screenshot%202025-11-05%2018.20.31.png)

Hasil perintah `git log --graph --oneline --decorate --all` menunjukkan riwayat commit dalam bentuk visual pohon.  
Terlihat bahwa branch **main** dan **style-experiment-peach** telah berhasil di-merge setelah penyelesaian konflik.  
Commit terakhir memiliki pesan merge yang menandakan penyatuan final antar-branch.

---

### 14. Sinkronisasi Akhir ke Repository GitHub
![Push Final](./Screenshoot/Screenshot%202025-11-05%2018.20.01.png)

Tahap akhir workflow Git dilakukan dengan perintah `git push`.  
Pesan *“Everything up-to-date”* menunjukkan bahwa seluruh commit lokal sudah berhasil disinkronkan ke repository GitHub, dan tidak ada perubahan baru yang perlu dikirim.  
Langkah ini memastikan hasil merge tersimpan aman secara online di repository publik.

---

## Kesimpulan
Melalui praktikum ini, saya telah menerapkan **Git Workflow** secara lengkap dalam pengelolaan proyek website portofolio.  
Kegiatan yang dilakukan meliputi inisialisasi repository, penambahan file ke staging area, pembuatan commit bertahap, pembuatan dan penggabungan branch, hingga penyelesaian konflik saat proses merge.  
Seluruh tahapan tersebut berhasil dilakukan dengan baik dan menghasilkan repository yang terstruktur, terdokumentasi, serta sinkron dengan GitHub sebagai media penyimpanan versi akhir proyek.