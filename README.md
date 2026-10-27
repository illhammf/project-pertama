# Panduan Git dan GitHub untuk Pemula

Repository ini berisi panduan belajar **Git dan GitHub dari dasar hingga mampu mengelola project secara mandiri**. Materi disusun secara bertahap, mulai dari instalasi, konfigurasi, pembuatan repository, pencatatan perubahan, hingga mengunggah project ke GitHub.

Panduan ini ditujukan terutama untuk mahasiswa, pelajar, dan programmer pemula yang ingin mempelajari version control serta membiasakan diri menggunakan Git dalam kegiatan perkuliahan maupun pengembangan perangkat lunak.

Seluruh materi menggunakan Bahasa Indonesia dengan istilah teknis dalam Bahasa Inggris agar mudah dipahami sekaligus membiasakan pembaca dengan istilah yang digunakan dalam dokumentasi pemrograman.

---

## Daftar Isi

- [1. Tujuan Pembelajaran](#1-tujuan-pembelajaran)
- [2. Mengenal Git dan GitHub](#2-mengenal-git-dan-github)
- [3. Persiapan Sebelum Memulai](#3-persiapan-sebelum-memulai)
- [4. Instalasi Git](#4-instalasi-git)
- [5. Konfigurasi Awal Git](#5-konfigurasi-awal-git)
- [6. Membuat Repository GitHub](#6-membuat-repository-github)
- [7. Membuat Project Lokal](#7-membuat-project-lokal)
- [8. Inisialisasi Repository dengan git init](#8-inisialisasi-repository-dengan-git-init)
- [9. Memeriksa Status dengan git status](#9-memeriksa-status-dengan-git-status)
- [10. Menambahkan File dengan git add](#10-menambahkan-file-dengan-git-add)
- [11. Menyimpan Perubahan dengan git commit](#11-menyimpan-perubahan-dengan-git-commit)
- [12. Mengatur Branch dengan git branch](#12-mengatur-branch-dengan-git-branch)
- [13. Menghubungkan Repository dengan GitHub](#13-menghubungkan-repository-dengan-github)
- [14. Mengunggah Project dengan git push](#14-mengunggah-project-dengan-git-push)
- [15. Alur Kerja Git Sehari-hari](#15-alur-kerja-git-sehari-hari)
- [16. Daftar Perintah Git yang Sering Digunakan](#16-daftar-perintah-git-yang-sering-digunakan)
- [17. Mengenal .gitignore](#17-mengenal-gitignore)
- [18. Mengunduh Repository dengan git clone](#18-mengunduh-repository-dengan-git-clone)
- [19. Mengambil Perubahan dengan git pull](#19-mengambil-perubahan-dengan-git-pull)
- [20. Mengenal Branch dan Merge](#20-mengenal-branch-dan-merge)
- [21. Melihat Riwayat dan Perbedaan Perubahan](#21-melihat-riwayat-dan-perbedaan-perubahan)
- [22. Mengatasi Error Umum](#22-mengatasi-error-umum)
- [23. Latihan Mandiri](#23-latihan-mandiri)
- [24. Kesimpulan](#24-kesimpulan)
- [25. Referensi Resmi](#25-referensi-resmi)
- [Lisensi](#lisensi)

---

## 1. Tujuan Pembelajaran

Setelah mempelajari panduan ini, pembaca diharapkan mampu:

1. Memahami perbedaan Git dan GitHub.
2. Menginstal dan melakukan konfigurasi Git.
3. Membuat repository Git lokal.
4. Memahami fungsi `git init`, `git status`, `git add`, dan `git commit`.
5. Menghubungkan repository lokal dengan repository GitHub.
6. Mengunggah project menggunakan `git push`.
7. Mengunduh repository menggunakan `git clone`.
8. Mengambil pembaruan menggunakan `git pull`.
9. Memahami branch, merge, dan riwayat perubahan.
10. Menyelesaikan permasalahan Git yang umum terjadi.

## 2. Mengenal Git dan GitHub

### 2.1 Apa Itu Git?

Git adalah sistem version control terdistribusi (*Distributed Version Control System* atau DVCS) yang digunakan untuk mencatat dan mengelola perubahan pada file.

Dengan Git, kita dapat:

- Melihat riwayat perubahan project.
- Mengetahui siapa yang membuat suatu commit.
- Membandingkan perubahan antarversi.
- Mengembangkan fitur melalui branch.
- Berkolaborasi dengan programmer lain.
- Kembali ke versi sebelumnya jika diperlukan.

Git dapat digunakan secara lokal tanpa harus terhubung ke internet.

### 2.2 Apa Itu GitHub?

GitHub adalah platform berbasis web untuk menghosting repository Git. GitHub menyediakan berbagai fasilitas, seperti:

- Penyimpanan repository secara online.
- Kolaborasi dalam pengembangan perangkat lunak.
- Pull request untuk mengusulkan perubahan.
- Issues untuk mencatat masalah atau pekerjaan.
- Dokumentasi project menggunakan README.
- Publikasi project agar dapat dipelajari orang lain.

### 2.3 Perbedaan Git dan GitHub

| Aspek | Git | GitHub |
|---|---|---|
| Bentuk | Software version control | Platform hosting repository |
| Penggunaan | Mencatat perubahan project | Menyimpan dan membagikan repository |
| Koneksi internet | Dapat digunakan secara offline | Membutuhkan internet untuk layanan online |
| Riwayat perubahan | Disimpan di repository lokal | Commit dapat dikirim dan disimpan di repository remote |
| Contoh | `git commit` | Membuka repository melalui browser |

**Kesimpulan:** Git digunakan untuk mengelola versi project, sedangkan GitHub digunakan untuk menyimpan dan membagikan repository Git secara online.

## 3. Persiapan Sebelum Memulai

Sebelum mengikuti praktik, persiapkan beberapa hal berikut:

1. Komputer atau laptop.
2. Sistem operasi Windows, Linux, atau macOS.
3. Git yang sudah terinstal.
4. Akun GitHub.
5. Terminal seperti PowerShell, Command Prompt, Git Bash, atau terminal VS Code.
6. Text editor seperti Visual Studio Code.
7. Koneksi internet untuk menghubungkan repository ke GitHub.

Dalam panduan ini, contoh praktik menggunakan **Windows PowerShell**. Jika menggunakan terminal lain, sebagian besar perintah Git tetap sama.

## 4. Instalasi Git

### 4.1 Mengunduh Git

Buka halaman resmi Git:

https://git-scm.com/install/

Pilih installer yang sesuai dengan sistem operasi yang digunakan, kemudian ikuti proses instalasi.

Pada Windows, pilihan pengaturan bawaan installer umumnya cukup untuk mulai belajar.

### 4.2 Memeriksa Instalasi

Buka PowerShell atau terminal VS Code, lalu jalankan:

```powershell
git --version
```

Jika Git terinstal dengan benar, terminal akan menampilkan versi Git yang tersedia.

Contoh output:

```text
git version 2.x.x.windows.x
```

Nomor versi dapat berbeda sesuai dengan versi yang terinstal.

Jika perintah tidak dikenali, periksa instalasi Git dan pastikan Git sudah tersedia pada `PATH`. Tutup dan buka kembali terminal setelah melakukan perubahan konfigurasi.

## 5. Konfigurasi Awal Git

Sebelum membuat commit, Git perlu mengetahui identitas pembuat perubahan.

### 5.1 Mengatur Nama

```powershell
git config --global user.name "Nama Lengkap"
```

Contoh:

```powershell
git config --global user.name "Ilham Firmansyah"
```

### 5.2 Mengatur Email

```powershell
git config --global user.email "email@example.com"
```

Gunakan email yang sesuai dengan identitas commit yang ingin digunakan. Jika ingin menghubungkan identitas commit dengan akun GitHub, gunakan email yang terdaftar atau alamat `noreply` GitHub yang sesuai.

### 5.3 Memeriksa Konfigurasi

```powershell
git config --global --list
```

Contoh output:

```text
user.name=Ilham Firmansyah
user.email=email@example.com
```

Pengaturan `--global` berlaku untuk seluruh repository Git milik pengguna tersebut. Identitas ini merupakan metadata commit, bukan metode autentikasi ke GitHub.

## 6. Membuat Repository GitHub

Repository merupakan tempat penyimpanan file project beserta riwayat perubahannya.

### 6.1 Membuka GitHub

Buka:

https://github.com/

Login menggunakan akun GitHub yang dimiliki.

### 6.2 Membuat Repository Baru

1. Klik tombol **New repository**.
2. Isi nama repository, misalnya `project-pertama`.
3. Tambahkan deskripsi singkat jika diperlukan.
4. Pilih visibilitas repository.
5. Tentukan apakah repository akan menggunakan README, `.gitignore`, atau lisensi.
6. Klik **Create repository**.

Untuk latihan mengunggah project lokal yang sudah memiliki commit pertama, cara yang paling sederhana adalah membuat repository GitHub dalam keadaan kosong, tanpa menambahkan README, `.gitignore`, atau lisensi dari GitHub terlebih dahulu.

Dengan begitu, riwayat awal dari repository lokal dapat dikirim tanpa perlu menyatukan dua riwayat yang berbeda.

### 6.3 Public dan Private

**Public**
- Dapat dilihat oleh siapa pun.
- Cocok untuk dokumentasi, portofolio, dan project open source.
- Jangan pernah mengunggah password, API key, token, atau data pribadi.

**Private**
- Hanya dapat diakses oleh pemilik dan pihak yang diberi izin.
- Cocok untuk project yang belum ingin dipublikasikan atau membutuhkan akses terbatas.

Pilih visibilitas berdasarkan kebutuhan project.

## 7. Membuat Project Lokal

Setelah menyiapkan repository GitHub, buat folder project di komputer.

Contoh menggunakan PowerShell:

```powershell
mkdir project-pertama
cd project-pertama
```

Keterangan:

- `mkdir` membuat folder baru.
- `cd` berpindah ke direktori tertentu.

Jika folder sudah dibuat melalui File Explorer atau VS Code, buka terminal langsung di folder tersebut.

### 7.1 Membuat README.md

Buat file bernama `README.md`.

File README umumnya berisi informasi seperti:

- Nama project.
- Deskripsi project.
- Tujuan pembuatan.
- Teknologi yang digunakan.
- Cara instalasi dan menjalankan project.
- Informasi kontributor dan lisensi.

Contoh isi:

```markdown
# Project Pertama

Ini adalah project pertama saya yang menggunakan Git dan GitHub.

## Tujuan

Mempelajari dasar version control dan cara mengunggah project ke GitHub.
```

Simpan file tersebut sebelum melanjutkan.

## 8. Inisialisasi Repository dengan git init

Perintah `git init` digunakan untuk menginisialisasi repository Git di direktori saat ini.

Jalankan:

```powershell
git init
```

Contoh output:

```text
Initialized empty Git repository in C:/Dokumen/project-pertama/.git/
```

Git akan membuat direktori tersembunyi bernama `.git` yang menyimpan metadata dan riwayat repository.

### 8.1 Memahami Direktori .git

Direktori `.git` merupakan bagian penting dari repository lokal. Jangan menghapus atau mengubah isinya secara manual jika tidak memahami konsekuensinya.

Perlu diketahui bahwa `git init` tidak otomatis mengunggah file ke GitHub. Perintah ini hanya menginisialisasi repository di komputer.

### 8.2 Memahami Branch Awal

Setelah menjalankan `git init`, Git dapat menggunakan nama branch awal seperti `master` atau `main`, bergantung pada konfigurasi.

Periksa branch aktif dengan:

```powershell
git branch
```

Jika ingin menggunakan `main` sebagai branch utama, kita dapat mengganti namanya menggunakan:

```powershell
git branch -M main
```

## 9. Memeriksa Status dengan git status

Perintah `git status` digunakan untuk melihat kondisi repository.

Jalankan:

```powershell
git status
```

Contoh output sebelum file ditambahkan:

```text
On branch master

No commits yet

Untracked files:
  README.md

nothing added to commit but untracked files present
```

Penjelasan:

- `On branch master`: repository sedang berada di branch `master`.
- `No commits yet`: belum ada commit.
- `Untracked files`: terdapat file yang belum dilacak Git.
- `README.md`: file README belum dimasukkan ke staging area.

`git status` merupakan salah satu perintah yang paling sering digunakan. Biasakan menjalankannya sebelum dan sesudah melakukan perubahan penting.

## 10. Menambahkan File dengan git add

Perintah `git add` digunakan untuk memasukkan perubahan ke staging area, yaitu area persiapan sebelum commit.

### 10.1 Menambahkan Satu File

```powershell
git add README.md
```

Perintah ini menambahkan perubahan pada `README.md` ke staging area.

### 10.2 Menambahkan Semua Perubahan

```powershell
git add .
```

Perintah tersebut menambahkan perubahan yang tercakup dalam direktori saat ini dan subdirektorinya ke staging area, dengan tetap mengikuti aturan pengabaian Git.

Pastikan file sensitif tidak ikut ditambahkan.

### 10.3 Memeriksa Hasil git add

```powershell
git status
```

Setelah file berhasil ditambahkan, Git biasanya menampilkan:

```text
Changes to be committed:
  new file:   README.md
```

Artinya, perubahan sudah masuk staging area dan siap direkam melalui commit.

### 10.4 Perbedaan git add dan git commit

- `git add`: menyiapkan perubahan yang akan direkam.
- `git commit`: merekam perubahan yang sudah disiapkan ke dalam riwayat repository lokal.

Menjalankan `git add` saja belum membuat commit dan belum mengunggah file ke GitHub.

## 11. Menyimpan Perubahan dengan git commit

Perintah `git commit` digunakan untuk merekam snapshot perubahan yang berada di staging area.

Jalankan:

```powershell
git commit -m "Initial commit"
```

Keterangan:

- `git commit`: membuat commit.
- `-m`: menambahkan pesan commit.
- `"Initial commit"`: pesan yang menjelaskan commit pertama.

Contoh output:

```text
[master (root-commit) 3d75d5a] Initial commit
 1 file changed, 1 insertion(+)
 create mode 100644 README.md
```

Penjelasan:

- `root-commit`: commit pertama pada repository tersebut.
- `3d75d5a`: contoh singkatan hash commit.
- `1 file changed`: satu file berubah.
- `create mode 100644 README.md`: Git merekam penambahan file README.

Hash commit dapat berbeda pada setiap repository.

### 11.1 Praktik Pesan Commit yang Baik

Gunakan pesan yang jelas dan menjelaskan perubahan.

Contoh:

```powershell
git commit -m "Initial commit"
git commit -m "Add README documentation"
git commit -m "Add login page"
git commit -m "Fix navigation bug"
git commit -m "Update installation instructions"
```

Hindari pesan yang terlalu umum seperti:

```text
update
fix
coba
perubahan
```

Pesan yang deskriptif akan memudahkan pembaca memahami riwayat project.

### 11.2 Memeriksa Commit

```powershell
git log --oneline
```

Perintah tersebut menampilkan ringkasan riwayat commit, termasuk hash dan pesan commit.

## 12. Mengatur Branch dengan git branch

Branch merupakan jalur pengembangan terpisah yang memungkinkan kita mengerjakan fitur atau perbaikan tanpa harus langsung mengubah branch utama.

### 12.1 Mengganti Nama Branch Menjadi main

```powershell
git branch -M main
```

Perintah tersebut mengganti nama branch aktif menjadi `main`.

Opsi `-M` memaksa penggantian nama jika diperlukan. Gunakan dengan hati-hati jika sudah ada branch lain dengan nama yang sama.

### 12.2 Melihat Branch

```powershell
git branch
```

Contoh output:

```text
* main
```

Tanda `*` menunjukkan branch yang sedang aktif.

### 12.3 Membuat Branch Baru

```powershell
git switch -c fitur-baru
```

Perintah tersebut membuat branch bernama `fitur-baru` sekaligus berpindah ke branch tersebut.

Branch membantu mengorganisasi pengembangan, terutama ketika project memiliki banyak fitur atau dikerjakan oleh beberapa orang.

## 13. Menghubungkan Repository dengan GitHub

Setelah repository lokal memiliki commit, hubungkan repository tersebut ke repository GitHub.

### 13.1 Menambahkan Remote

Contoh URL repository:

```text
https://github.com/USERNAME/project-pertama.git
```

Tambahkan remote bernama `origin`:

```powershell
git remote add origin https://github.com/USERNAME/project-pertama.git
```

Ganti `USERNAME` dengan username GitHub sendiri.

Keterangan:

- `git remote`: mengelola alamat repository remote.
- `add`: menambahkan remote baru.
- `origin`: nama alias remote yang umum digunakan.
- URL: alamat repository GitHub tujuan.

Nama `origin` bukan nama wajib, tetapi sudah menjadi konvensi yang umum.

### 13.2 Memeriksa Remote

```powershell
git remote -v
```

Contoh output:

```text
origin  https://github.com/USERNAME/project-pertama.git (fetch)
origin  https://github.com/USERNAME/project-pertama.git (push)
```

Jika URL salah, periksa kembali sebelum melakukan push.

Untuk mengganti URL remote yang sudah ada:

```powershell
git remote set-url origin https://github.com/USERNAME/project-pertama.git
```

Jangan menjalankan `git remote add origin` berulang kali jika remote dengan nama tersebut sudah terdaftar.

## 14. Mengunggah Project dengan git push

Perintah `git push` digunakan untuk mengirim commit dari repository lokal ke repository remote.

Pastikan repository GitHub tujuan sudah tersedia dan dapat diakses oleh akun yang digunakan.

### 14.1 Mengunggah Branch Pertama Kali

```powershell
git push -u origin main
```

Penjelasan:

- `git push`: mengirim commit ke remote.
- `origin`: nama remote.
- `main`: branch lokal yang akan dikirim.
- `-u`: mengatur upstream tracking untuk branch lokal tersebut.

Jika berhasil, terminal dapat menampilkan:

```text
To https://github.com/USERNAME/project-pertama.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
```

Artinya, branch `main` berhasil dikirim ke GitHub dan branch lokal telah diatur untuk melacak branch remote yang sesuai.

### 14.2 Push Berikutnya

Setelah upstream tracking diatur, alur yang biasa digunakan adalah:

```powershell
git add .
git commit -m "Update project"
git push
```

Periksa perubahan sebelum melakukan commit. Jika tidak ada perubahan baru, Git tidak akan membuat commit baru.

### 14.3 Autentikasi GitHub

Jika Git meminta autentikasi, ikuti metode autentikasi yang tersedia, seperti browser-based sign-in melalui Git Credential Manager atau SSH.

Password akun GitHub biasa tidak dapat digunakan sebagai password Git untuk operasi HTTPS. Jika menggunakan personal access token, jaga kerahasiaannya dan jangan pernah menyimpannya di README atau mengunggahnya ke repository.

## 15. Alur Kerja Git Sehari-hari

Setelah repository berhasil terhubung dengan GitHub, alur kerja yang umum adalah:

```powershell
git status
git add .
git commit -m "Deskripsi perubahan"
git push
```

Fungsi setiap langkah:

1. `git status`: memeriksa perubahan.
2. `git add .`: menyiapkan perubahan untuk commit.
3. `git commit`: merekam perubahan secara lokal.
4. `git push`: mengirim commit ke GitHub.

Alur ini dapat diulang setiap kali ada perubahan baru.

**Penting:** Git tidak otomatis mengunggah perubahan setiap kali file disimpan. Perubahan perlu diproses sesuai alur Git sebelum tersedia pada repository remote.

## 16. Daftar Perintah Git yang Sering Digunakan

| Perintah | Fungsi |
|---|---|
| `git --version` | Memeriksa versi Git |
| `git config --global --list` | Melihat konfigurasi global |
| `git init` | Menginisialisasi repository |
| `git status` | Memeriksa status repository |
| `git add nama-file` | Menyiapkan file tertentu |
| `git add .` | Menyiapkan perubahan dalam direktori saat ini |
| `git commit -m "Pesan"` | Membuat commit |
| `git log` | Melihat riwayat commit |
| `git log --oneline` | Melihat ringkasan commit |
| `git branch` | Melihat daftar branch lokal |
| `git branch -M main` | Mengganti nama branch aktif menjadi `main` |
| `git switch main` | Berpindah ke branch `main` |
| `git switch -c nama-branch` | Membuat dan berpindah ke branch baru |
| `git remote -v` | Melihat remote yang terdaftar |
| `git remote add origin URL` | Menambahkan remote |
| `git remote set-url origin URL` | Mengubah URL remote |
| `git push` | Mengirim commit ke remote |
| `git pull` | Mengambil dan mengintegrasikan perubahan dari remote |
| `git fetch` | Mengambil pembaruan remote tanpa mengintegrasikannya |
| `git clone URL` | Mengkloning repository remote |
| `git diff` | Melihat perbedaan perubahan yang belum di-stage |
| `git diff --staged` | Melihat perubahan yang sudah di-stage |
| `git restore nama-file` | Mengembalikan perubahan file yang belum di-stage |
| `git restore --staged nama-file` | Mengeluarkan perubahan dari staging area |
| `git rm --cached nama-file` | Menghentikan pelacakan file tanpa menghapus file lokal |
| `git merge nama-branch` | Menggabungkan branch ke branch aktif |

Perintah yang mengubah atau membuang perubahan perlu digunakan dengan hati-hati. Selalu periksa status repository dan simpan pekerjaan penting sebelum menjalankannya.

## 17. Mengenal .gitignore

File `.gitignore` digunakan untuk menentukan file atau direktori yang tidak perlu dilacak Git.

Contoh `.gitignore`:

```gitignore
# File konfigurasi lokal yang berisi rahasia
.env

# Dependensi Node.js
node_modules/

# File build Flutter
build/

# File sementara Windows
Thumbs.db
Desktop.ini

# File sementara editor
*.tmp
```

Sesuaikan aturan `.gitignore` dengan teknologi project. Contoh di atas merupakan template umum, bukan aturan yang harus digunakan seluruhnya pada setiap project.

### 17.1 Mengapa .gitignore Penting?

`.gitignore` membantu mencegah file yang tidak diperlukan masuk ke repository, seperti:

- File sementara.
- Folder dependensi yang dapat diinstal ulang.
- Hasil build.
- Konfigurasi lokal yang berisi rahasia.

**Catatan:** `.gitignore` tidak otomatis menghentikan pelacakan file yang sebelumnya sudah di-commit. File yang sudah terlacak perlu dikeluarkan dari index secara terpisah. Jika rahasia sudah pernah diunggah, menghapusnya dari commit terbaru saja belum tentu menghilangkannya dari riwayat repository.

## 18. Mengunduh Repository dengan git clone

Perintah `git clone` digunakan untuk menyalin repository remote ke komputer lokal, termasuk riwayat commit yang tersedia.

Contoh:

```powershell
git clone https://github.com/USERNAME/project-pertama.git
```

Setelah proses selesai, masuk ke direktori project:

```powershell
cd project-pertama
```

Periksa status repository:

```powershell
git status
```

Clone cocok digunakan ketika:

- Ingin melanjutkan project di komputer lain.
- Ingin mempelajari project orang lain.
- Ingin bekerja bersama anggota kelompok.
- Ingin mengambil repository yang sudah ada di GitHub.

Jika repository bersifat private, akun yang digunakan harus memiliki akses yang sesuai.

## 19. Mengambil Perubahan dengan git pull

Perintah `git pull` digunakan untuk mengambil perubahan dari remote dan mengintegrasikannya ke branch lokal yang sedang aktif.

Contoh:

```powershell
git pull
```

Perintah ini umumnya menggabungkan proses fetch dengan integrasi melalui merge atau metode yang dikonfigurasi.

Contoh situasi:

1. Kamu mengubah README langsung melalui website GitHub.
2. Repository remote memiliki commit baru.
3. Repository lokal belum memiliki perubahan tersebut.
4. Jalankan `git pull` untuk mengambil dan mengintegrasikan perubahan.

Sebelum melakukan pull, periksa apakah terdapat perubahan lokal yang belum disimpan. Jika terjadi konflik, selesaikan konflik tersebut sebelum melanjutkan pekerjaan.

### Perbedaan git fetch dan git pull

- `git fetch`: mengambil informasi dan commit baru dari remote tanpa langsung mengintegrasikannya ke branch aktif.
- `git pull`: mengambil perubahan sekaligus mengintegrasikannya ke branch lokal sesuai konfigurasi.

## 20. Mengenal Branch dan Merge

### 20.1 Apa Itu Branch?

Branch memungkinkan pengembangan fitur secara terpisah dari branch utama.

Misalnya, project memiliki branch:

- `main`: versi utama project.
- `fitur-login`: pengembangan halaman login.
- `perbaikan-bug`: perbaikan kesalahan program.

### 20.2 Membuat Branch Baru

```powershell
git switch -c fitur-login
```

Lakukan perubahan pada file, lalu rekam perubahan:

```powershell
git add .
git commit -m "Add login feature"
```

Untuk mengirim branch ke GitHub:

```powershell
git push -u origin fitur-login
```

### 20.3 Menggabungkan Branch

Pindah ke branch tujuan:

```powershell
git switch main
```

Gabungkan branch fitur:

```powershell
git merge fitur-login
```

Jika merge berhasil, perubahan dari branch fitur akan diintegrasikan ke branch `main`.

Untuk kerja kelompok, merge juga dapat dilakukan melalui pull request di GitHub agar perubahan bisa ditinjau sebelum digabungkan.

### 20.4 Merge Conflict

Merge conflict terjadi ketika Git tidak dapat menentukan secara otomatis cara menggabungkan perubahan yang saling bertentangan.

Langkah penanganan umum:

1. Periksa file yang mengalami konflik.
2. Buka file tersebut di editor.
3. Tentukan perubahan yang ingin dipertahankan.
4. Hapus penanda konflik setelah menyelesaikan isinya.
5. Simpan file.
6. Jalankan `git add` pada file yang sudah diperbaiki.
7. Selesaikan merge dengan commit jika diperlukan.

Jangan langsung menghapus seluruh isi file ketika terjadi konflik. Pahami perubahan dari masing-masing branch terlebih dahulu.

## 21. Melihat Riwayat dan Perbedaan Perubahan

### 21.1 Melihat Riwayat Commit

```powershell
git log
```

Menampilkan detail commit, termasuk hash, penulis, tanggal, dan pesan commit.

### 21.2 Melihat Ringkasan Riwayat

```powershell
git log --oneline
```

Lebih ringkas untuk melihat daftar commit.

### 21.3 Melihat Perubahan File

```powershell
git diff
```

Menampilkan perbedaan perubahan pada file yang belum masuk staging area.

### 21.4 Melihat Perubahan yang Sudah di-Stage

```powershell
git diff --staged
```

Menampilkan perubahan yang sudah disiapkan untuk commit.

Perintah-perintah ini membantu memeriksa isi perubahan sebelum merekamnya ke riwayat repository.

## 22. Mengatasi Error Umum

### 22.1 Error: `Author identity unknown`

Penyebab: nama atau email Git belum dikonfigurasi.

Solusi:

```powershell
git config --global user.name "Nama Lengkap"
git config --global user.email "email@example.com"
```

Kemudian ulangi perintah commit.

### 22.2 Error: `remote origin already exists`

Penyebab: remote bernama `origin` sudah terdaftar.

Periksa remote:

```powershell
git remote -v
```

Jika URL salah, perbaiki dengan:

```powershell
git remote set-url origin https://github.com/USERNAME/project-pertama.git
```

### 22.3 Error: `src refspec main does not match any`

Penyebab yang umum adalah branch `main` belum tersedia atau belum memiliki commit yang dapat dikirim.

Periksa status:

```powershell
git status
git branch
git log --oneline
```

Jika belum memiliki commit, tambahkan file dan buat commit terlebih dahulu. Jika branch masih bernama `master`, ganti nama branch aktif:

```powershell
git branch -M main
```

Setelah itu, coba push kembali.

### 22.4 Error: `failed to push some refs`

Salah satu penyebabnya adalah repository remote sudah memiliki commit yang belum tersedia secara lokal.

Periksa status dan riwayat kedua repository. Jika perubahan remote memang perlu diintegrasikan, lakukan pull dengan strategi yang sesuai, selesaikan konflik jika ada, lalu push kembali.

Hindari langsung menggunakan `git push --force` karena dapat menimpa riwayat remote.

### 22.5 Error: `Authentication failed`

Penyebabnya dapat berupa sesi autentikasi yang tidak valid, kredensial tersimpan yang salah, atau akses repository yang tidak sesuai.

Solusi umum:

1. Pastikan URL repository benar.
2. Pastikan akun memiliki akses ke repository.
3. Ikuti proses autentikasi melalui browser atau Git Credential Manager.
4. Periksa kredensial yang tersimpan jika autentikasi masih gagal.
5. Jika menggunakan token, pastikan token memiliki izin yang diperlukan dan belum kedaluwarsa.

Jangan pernah membagikan token autentikasi kepada orang lain.

### 22.6 File Tidak Muncul di GitHub

Periksa langkah-langkah berikut:

```powershell
git status
git log --oneline
git remote -v
```

Pastikan file sudah di-stage, commit berhasil dibuat, dan branch yang benar sudah di-push ke remote yang sesuai.

Jika file diabaikan oleh `.gitignore`, periksa aturan yang berlaku sebelum mencoba menambahkannya.

## 23. Latihan Mandiri

Setelah memahami materi, kerjakan latihan berikut untuk memperkuat pemahaman.

### Latihan 1 — Membuat Repository Pertama

1. Buat folder bernama `latihan-git`.
2. Inisialisasi repository menggunakan `git init`.
3. Buat file `README.md`.
4. Isi file dengan deskripsi singkat.
5. Periksa status repository menggunakan `git status`.
6. Tambahkan file dengan `git add README.md`.
7. Buat commit pertama menggunakan `git commit`.
8. Periksa riwayat menggunakan `git log --oneline`.

### Latihan 2 — Mengunggah Project ke GitHub

1. Buat repository publik bernama `latihan-git` di GitHub.
2. Pastikan repository remote kosong.
3. Ubah nama branch utama menjadi `main`.
4. Hubungkan repository lokal dengan remote menggunakan `git remote add origin`.
5. Periksa remote menggunakan `git remote -v`.
6. Unggah branch menggunakan `git push -u origin main`.
7. Buka repository GitHub dan pastikan file README sudah muncul.

### Latihan 3 — Memperbarui Project

1. Ubah isi README.
2. Tambahkan bagian tujuan project.
3. Jalankan `git status`.
4. Tambahkan perubahan dengan `git add .`.
5. Buat commit baru.
6. Unggah perubahan menggunakan `git push`.
7. Periksa riwayat commit di terminal dan GitHub.

### Latihan 4 — Menggunakan Branch

1. Buat branch bernama `fitur-dokumentasi`.
2. Tambahkan bagian baru pada README.
3. Buat commit.
4. Push branch tersebut ke GitHub.
5. Pindah kembali ke `main`.
6. Gabungkan branch fitur ke `main`.
7. Periksa hasil penggabungan.

### Latihan 5 — Pertanyaan Evaluasi

Jawablah pertanyaan berikut berdasarkan praktik yang sudah dilakukan.

1. Apa perbedaan Git dan GitHub?
2. Apa fungsi `git init`?
3. Apa perbedaan `git add` dan `git commit`?
4. Mengapa commit tetap dapat dibuat tanpa internet?
5. Apa fungsi `git remote add origin`?
6. Apa perbedaan `git commit` dan `git push`?
7. Mengapa branch `main` sering digunakan sebagai branch utama?
8. Apa perbedaan `git clone` dan `git pull`?
9. Apa fungsi file `.gitignore`?
10. Mengapa kita perlu memeriksa `git status` sebelum commit?

## 24. Kesimpulan

Git dan GitHub merupakan alat penting dalam pengembangan perangkat lunak. Git membantu programmer mencatat, mengelola, dan meninjau perubahan project, sedangkan GitHub menyediakan tempat untuk menyimpan dan membagikan repository secara online.

Perintah dasar yang perlu dikuasai oleh pemula adalah:

```powershell
git init
git status
git add .
git commit -m "Pesan commit"
git branch -M main
git remote add origin URL
git push -u origin main
```

Untuk penggunaan sehari-hari, alur yang paling penting adalah:

```powershell
git status
git add .
git commit -m "Deskripsi perubahan"
git push
```

Pahami fungsi setiap perintah dan jangan hanya menghafal sintaksnya. Biasakan memeriksa status repository, membuat pesan commit yang jelas, dan menjaga keamanan data sebelum mengunggah project ke GitHub.

## 25. Referensi Resmi

Gunakan dokumentasi berikut untuk mempelajari Git dan GitHub lebih lanjut.

- [Git Official Website](https://git-scm.com/)
- [Git Documentation](https://git-scm.com/doc)
- [Git Book — Pro Git](https://git-scm.com/book/en/v2)
- [GitHub Docs](https://docs.github.com/)
- [GitHub: Creating a Repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository)
- [GitHub: Pushing Commits to a Remote Repository](https://docs.github.com/en/get-started/using-git/pushing-commits-to-a-remote-repository)

---

## Lisensi

Repository ini menggunakan **MIT License**.

Materi dalam repository ini boleh digunakan, dipelajari, dimodifikasi, dan didistribusikan kembali sesuai ketentuan MIT License. Penggunaan lisensi MIT tidak menghilangkan kewajiban untuk mempertahankan pemberitahuan hak cipta dan teks lisensi pada salinan atau bagian substansial dari perangkat lunak atau materi yang dilisensikan.

Lihat file [`LICENSE`](LICENSE) untuk teks lisensi lengkap.

---

**Selamat belajar Git dan GitHub!**

Mulailah dari perintah dasar, lakukan setiap praktik secara bertahap, dan biasakan menggunakan Git dalam setiap project pemrograman yang kamu kerjakan.
