# catatan-git
catatan pribadi tentang command line git

## git - github

- 1. commit : menyimpan setiap perubahan kedalam repo
- 2. branch : jalur 'development' bebas dari sebuah commit
- 3. checkout : berpindah ke branch / commit yang lain
- 4. merge : 
	- 4.1 merge conflict : baris yang sama diubah oleh 2 branch yang berbeda
- 5. pull request : meminta pemilik repo untuk 'mengambil' perubahan yang telah dilakukan
- 6. fork / forking : 
	+ membuat 'copy / duplicate' dari repo orang lain (beserta history-nya)
	+ jembatan antara repo original dan duplikatnya
	+ modifikasi terhadap repo original
	+ berkontribusi pada repo orang lain
	+ Fork != Clone

##=== GIT command (LOCAL) ===
 link : https://git-scm.com/book

- 1. $ git init
- 2. $ git add <file(s)> / git add .
- 3. $ git status
- 4. $ git commit
- 5. $ git config
- 6. $ git branch
- 7. $ git help
- 8. $ git log
	- melihat log 2 perubahan trakhir : $ git log -2
	- melihat log file tertentu, misal : $ git log -- index.html

-  === 3 area pada repo GIT ===
- 1. Working tree ----> staging area ---> History

- working tree = folder repo project pada local pc
- staging area = file yang sudah di  git add ke repo

##==== tutorial membuat repositori git local / working tree ====
- 1. pilih folder project 
- 2. klik kanan kemudian pilih : git bash here
- 3. ketik command : git init (agar folder menjadi repositori)

## ==== membuat staging area ====
- 1. git add namafile / git add . (untuk semua file)
- 2. git config --global user.email "you@example.com"
- 3. git config --global user.name "Your Name"

##=== cara commit file ===
- 1. pastikan file sudah di add staging (git add namafile)
- 2. git status , cek status file, kalau nama file berwarna hijau maka sudah masuk staging
- 3. git commit -m "tulis pesan"

##== cara mengembalikan file yang sudah terhapus ==
- 1. cari log histori ketika file tersebut di hapus 
	contoh : git log -- style.css
- 2. git checkout "5 digit pertama commit" -- namafile
	contoh : git checkout  b315e -- style.css

##=== membuat nama alias ==
- contoh membuat log graph
- $ alias graph="git log --all --decorate --oneline --graph"
cukup ketik $ graph untuk memanggil alias

##=== membuat branch ===
- contoh membuat branch mahasiswa
- $ git branch mahasiswa
- $ git branch

##=== pindah branch ===
- $ git checkout mahasiswa

## === cara merge branch ke branch  master ===
- 1. masuk ke pointer branch master = $ git checkout master
- 2. $ git status : branch master harus hijau
- 3. $ git merge mahasiswa

##=== cara menghapus branch yang sudah di merge ===
- 1. cek branch yang sudah di merge ke master : $ git branch --merged
- 2. $ git branch -d mahasiswa

## === create ssh keygen ===
- $ move to dir : cd /c/Users/danilsyah/.ssh
- $ ssh-keygen -o -t rsa -C "danilsyaharihardjo@gmail.com" -b 4096
- $ cat danil.pub
  copy and paste to github
- $ eval $(ssh-agent -s)
- $ ssh-add ~/.ssh/danil

##=== git --> github https / ssh ===
- 1. $ git clone masukan url_clone
- 2. git remote
- 3. git remote -v
- 4. git config --global

##=== cara push ke repo github ===
- 1. git add .
- 2. git commit -m "pesan"
- 3. git push

##=== cara update / menarik  project dari github ke local ===
- 1. $ git pull

##== cara ganti email / user repo local ==
- cek git config = $ git config --list
- 1. $ git config --global user.name "danil syah"
- 2. $ git config --global user.email "danilsyaharihardjo@gmail.com"

