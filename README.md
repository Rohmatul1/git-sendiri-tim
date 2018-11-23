# Pengelanan GIT

Git adalah version control system yang digunakan para developer untuk mengembangkan 
software secara bersama-bersama. Fungsi utamanya adalah untuk mengatur versi dari 
source code anda, menambahkan tanda/checkpoint ketika terjadi perubahan pada kode 
Anda dan tentunya akan mempermudah Anda untuk tetap mengetahui apa saja yang 
berubah dari source code Anda.

# Perintah-perintah pada GIT

Untuk mengetahui bagaimana menggunakan git, berikut perintah-perintah dasar git:

* Git init : untuk membuat repository pada file lokal yang nantinya ada folder .git
* Git status : untuk mengetahui status dari repository lokal
* Git add : menambahkan file baru pada repository yang dipilih
* Git commit : untuk menyimpan perubahan yang dilakukan, tetapi tidak ada perubahan 
pada remote repository.
* Git push : untuk mengirimkan perubahan file setelah di commit ke remote repository.
* Git branch : melihat seluruh branch yang ada pada repository
* Git checkout : menukar branch yang aktif dengan branchyang dipilih
* Git merge : untuk menggabungkan branch yang aktif dan branch yang dipilih
* Git clone : membuat Salinan repository lokal

# Cara Kerja GIT

Tiga bagian utama dari sebuah projek Git: direktori Git, direktori kerja, dan staging area.

![On Demand](https://github.com/Rohmatul1/git-sendiri-tim/blob/master/1.png)

* Direktori Git adalah dimana Git menyimpan metadata dan database objek untuk projek anda. 
Ini adalah bahagian terpenting dari Git, dan inilah yang disalin ketika anda melakukan kloning 
sebuah repository dari komputer lain.

* Direktori kerja adalah sebuah checkout tunggal dari satu versi dari projek. Berkas-berkas 
ini kemudian ditarik keluar dari basisdata yang terkompresi dalam direktori Git dan disimpan 
pada disk untuk anda gunakan atau modifikasi.

* Staging area adalah sebuah berkas sederhana, umumnya berada dalam direktori Git anda, 
yang menyimpan informasi mengenai apa yang menjadi commit selanjutnya. Ini terkadang disebut 
sebagai index, tetapi semakin menjadi standard untuk menyebutnya sebagai staging area.

Alur kerja dasar Git adalah seperti ini:
* Anda mengubah berkas dalam direktori kerja anda.
* Anda membawa berkas ke stage, menambahkan snapshotnya ke staging area.
* Anda melakukan commit, yang mengambil berkas seperti yang ada di staging area dan menyimpan s
napshotnya secara permanen ke direktori Git anda.

# GIT Untuk Kerja Sendiri 
* git config --global user.name "Rohmatul1"
* git config --global user.email "mizusan111213@gmail.com"
* git add *
* git commit -m "Pertemuan TCT"
* git remote add origin https://github.com/Rohmatul1/git-sendiri-tim.git
* git push -u origin master

# GIT Untuk Kerja Tim
1. Membuat branch baru di ambil dari branch origin/master

git checkout -b myFeature origin/master

2. Jika mendapati notif fast-forward karena ke duluan tim lain pull request dan di marge
pastikan titik saat ini sama dengan origin/master

* git status
* git log --oneline
git fetch
git rebase -i origin/master
* git status
* vi readme.md 
* git add readme.md
* git rebase --continue
git push origin firstFeatureFromChipulaja
* git pull origin firstFeatureFromChipulaja
* git push origin firstFeatureFromChipulaja

Sumber :
* https://gist.github.com/chipulaja/a510ec370e7535797126ccd27d7146de
* https://git-scm.com/book/id/v1/Memulai-Git-Dasar-Git