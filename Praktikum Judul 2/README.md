# Praktikum Judul 2 — Workflow Git Website Portofolio

## Deskripsi
Proyek ini merupakan implementasi **Workflow Git (Git Workflow)** pada website portofolio hasil Percobaan 1.  
Kegiatan ini bertujuan agar mahasiswa memahami dan mampu menerapkan proses pengelolaan versi proyek menggunakan Git secara sistematis — mulai dari inisialisasi repository, pembuatan commit bertahap, pembuatan branch untuk eksperimen styling, penyelesaian konflik, hingga sinkronisasi akhir ke repository GitHub.

Melalui praktikum ini, mahasiswa tidak hanya mempelajari teori dasar Git, tetapi juga **menerapkannya secara langsung** dalam proyek web statis yang terdiri atas struktur file HTML, CSS, dan aset gambar pendukung.  
Setiap tahap commit dan branch dilakukan serta didokumentasikan secara runtut untuk menunjukkan penerapan alur kerja Git yang profesional, efisien, dan sesuai standar kolaborasi dalam pengembangan perangkat lunak.

---

## Hasil Screenshot

### 1️. Inisialisasi Repository
![Inisialisasi Repository](./Screenshoot/WhatsApp%20Image%202025-11-05%20at%2017.57.8a.png)  
Perintah git init digunakan untuk memulai repository Git di folder TA-Praktikum-Pemrograman-Web. Git akan membuat folder tersembunyi .git yang berfungsi untuk menyimpan seluruh riwayat versi (commit log, branch, merge, dsb). Pesan “Reinitialized existing Git repository” artinya sebelumnya folder ini sudah pernah diinisialisasi, dan Git hanya mengaktifkannya kembali.

---

### 2️. Menambahkan Semua File ke Staging Area
![Menambahkan Semua File](./Screenshoot/WhatsApp%20Image%202025-11-05%20at%2017.58.23.png)  
Perintah ini menambahkan semua file yang ada di folder kerja ke staging area, yaitu tahap sebelum disimpan permanen ke dalam commit. Titik (.) berarti semua file dan subfolder di direktori ini. Pada tahap ini, seluruh file di dalam folder “Source Code” seperti index.html, style.css, dan gambar sudah siap untuk di-commit.

---

### 3️. Membuat Commit Pertama
![Commit Pertama](./Screenshoot/Screenshot%202025-11-05%2018.04.34.png)  
Perintah git commit -m "Judul 2" digunakan untuk membuat commit pertama dalam proyek ini. Commit ini berfungsi sebagai titik awal atau snapshot dari seluruh file yang ada di dalam folder “Praktikum Judul 2”. Pada tahap ini, Git mencatat semua perubahan yang telah ditambahkan sebelumnya dengan perintah git add ., termasuk file HTML, CSS, dan berbagai file gambar di dalam folder Source Code. Setelah perintah dijalankan, Git menampilkan hasil bahwa ada tujuh file baru dengan total 991 baris kode yang dimasukkan. Hal ini menunjukkan bahwa seluruh struktur proyek—mulai dari file tampilan (index.html dan style.css) hingga aset pendukung (gambar)—telah resmi tersimpan ke dalam histori versi Git dan siap untuk proses pengembangan selanjutnya seperti commit bertahap, pembuatan branch, dan merge.

---

### 4️. Menampilkan Riwayat Commit
![Riwayat Commit](./Screenshoot/Screenshot%202025-11-05%2018.05.18.png)  
Perintah git log --graph --oneline --decorate --all ini dijalankan sebelum tahap branch dan merge, sehingga hasilnya hanya menampilkan commit yang terjadi di cabang utama (main). Tujuannya adalah untuk memeriksa riwayat commit awal proyek — seperti inisialisasi repository, penambahan struktur folder, dan commit pertama berisi file HTML serta CSS. Tampilan grafik ini membantu memastikan bahwa semua perubahan awal telah tercatat dengan benar di branch utama sebelum melanjutkan ke tahap eksperimen styling (branch baru) dan penggabungan (merge).

---

### 5️. Push ke Repository GitHub
![Push ke GitHub](./Screenshoot/Screenshot%202025-11-05%2018.06.39.png)  
Setelah semua perubahan dan commit selesai dilakukan di branch utama (main), perintah git push digunakan untuk mengunggah seluruh commit dari repositori lokal ke repositori GitHub.
Langkah ini memastikan bahwa setiap pembaruan, termasuk file proyek dan riwayat versi, tersimpan secara online dan dapat diakses publik sesuai instruksi tugas. 

---

### 6️. Membuat Branch Baru
![Branch Baru](./Screenshoot/Screenshot%202025-11-05%2018.07.45.png)  
Pada tahap ini dibuat branch baru bernama style-experiment-peach menggunakan perintah git checkout -b. Branch ini digunakan untuk mencoba perubahan styling tanpa memengaruhi kode utama di branch main, sehingga proses pengembangan tetap aman dan terpisah.

---

### 7️. Commit Section About
![Section About](./Screenshoot/Screenshot%202025-11-05%2018.11.14.png)  
Pada tahap ini dilakukan penambahan section About pada file index.html menggunakan perintah git add dan git commit. Bagian ini berisi profil singkat dan deskripsi diri sebagai mahasiswa Teknik Informatika Universitas Lampung. Commit tersebut terdokumentasi dengan pesan “Percobaan 2: Tambah Section About (profil & deskripsi singkat)”, menandakan adanya pembaruan struktur halaman portofolio yang menampilkan informasi pribadi secara lebih jelas.

---

### 8️. Commit Section Projects
![Section Projects](./Screenshoot/Screenshot%202025-11-05%2018.12.12.png)  
Pada tahap ini dilakukan penambahan Section Projects ke dalam file index.html untuk menampilkan daftar proyek yang telah dibuat. Bagian ini berisi dua proyek utama, yaitu Smart Home dan Tickle Task, lengkap dengan deskripsi, teknologi yang digunakan, serta gambar pendukung. Commit dilakukan dengan pesan “Percobaan 2: Tambah Section Projects (kartu proyek & link proyek)” sebagai dokumentasi perubahan tampilan dan konten portofolio.


---

### 9️. Perubahan Font di Branch Main
![Perubahan Font](./Screenshoot/Screenshot%202025-11-05%2018.13.15.png)  
Pada tahap ini dilakukan perubahan styling pada file style.css di branch main dengan mengganti font menjadi Arial. Langkah ini bertujuan untuk melihat perbedaan tampilan antara branch utama dan branch eksperimen. Commit dilakukan dengan pesan “Ubah font ke Arial di main” sebagai dokumentasi modifikasi visual dasar sebelum dilakukan merge untuk menguji potensi konflik antar-branch.

---

### 10. Percobaan Konflik di Branch Eksperimen
![Konflik Font](./Screenshoot/Screenshot%202025-11-05%2018.14.56.png)  
Pada tahap ini dilakukan perubahan pada file style.css di branch style-experiment-peach dengan mengganti font menjadi Poppins dan menambahkan komentar pembeda. Langkah ini dilakukan setelah branch utama (main) menggunakan font Arial, sehingga perbedaan tersebut akan memunculkan konflik ketika proses merge dilakukan. Commit ini dicatat dengan pesan “Konflik: ubah font ke Poppins di style-experiment-peach” sebagai bagian dari simulasi penyelesaian konflik Git.

---

### 11. Simulasi Konflik dan Merge
![Simulasi Merge](./Screenshoot/Screenshot%202025-11-05%2018.18.12.png)  
Pada tahap ini dilakukan proses merge antara branch main dan style-experiment-peach.
Konflik terjadi karena kedua branch melakukan perubahan berbeda pada file style.css:
•	Branch main menggunakan font Arial dengan background #e3e3e3.
•	Branch style-experiment-peach menggunakan font Poppins dengan tambahan komentar pembeda.
Git menampilkan tanda konflik (<<<<<<<, =======, >>>>>>>) yang menandakan bagian berbeda di kedua branch. Konflik ini kemudian harus diselesaikan secara manual di Visual Studio Code sebelum dilakukan commit lanjutan untuk menyelesaikan proses merge.

---

### 12️. Penyelesaian Konflik dan Merge Selesai
![Penyelesaian Merge](./Screenshoot/Screenshot%202025-11-05%2018.19.39.png)  
Tahap ini merupakan langkah terakhir dari proses merge antara branch main dan style-experiment-peach. Setelah konflik di file style.css berhasil diselesaikan dengan memilih font Poppins sebagai hasil akhir, dilakukan commit dengan pesan “Merge selesai: resolve conflict di style.css (pilih Poppins sebagai final)”. Langkah ini menandai bahwa seluruh konflik telah terselesaikan dan perubahan dari kedua branch berhasil digabungkan ke dalam branch utama tanpa error.

---

### 13. Visualisasi Riwayat Commit
![Riwayat Merge](./Screenshoot/Screenshot%202025-11-05%2018.20.31.png)  
Gambar ini menunjukkan hasil dari perintah git log --graph --oneline --decorate --all yang menampilkan riwayat commit lengkap dalam bentuk visual pohon. Terlihat bahwa branch main dan style-experiment-peach telah berhasil di-merge setelah penyelesaian konflik pada file style.css. Commit terakhir memiliki pesan “Merge selesai: resolve conflict di style.css (pilih Poppins sebagai final)” yang menandakan penyatuan akhir antara perubahan di branch utama dan branch percobaan styling. Visual ini menunjukkan alur kerja Git yang rapi, mulai dari inisialisasi proyek, pembuatan branch, hingga penggabungan hasil eksperimen styling kembali ke branch utama.

---

### 14️. Sinkronisasi Akhir ke Repository GitHub
![Push Final](./Screenshoot/Screenshot%202025-11-05%2018.20.01.png)  
Gambar ini menunjukkan tahap terakhir dari workflow Git, yaitu perintah git push.
Pesan “Everything up-to-date” menandakan bahwa seluruh commit lokal sudah berhasil disinkronkan ke repository GitHub, dan tidak ada perubahan baru yang perlu dikirim.
Tahap ini memastikan bahwa hasil merge, termasuk penyelesaian konflik pada file style.css, telah aman tersimpan secara online di repository publik proyek.