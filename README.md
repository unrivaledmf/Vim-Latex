# Halo, ini Fadil 👨‍🔬
Seorang pelajar yang sekarang sedang antusias terhadap Competitive Programming.
## 🔗 Links 
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://katherinempeterson.com/)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://katherinempeterson.com/)
[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/)
[![instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)]()
[![whatsapp](https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)]()
[![gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)]()

---
---

## 📖 Vim-Latex
Menggunakan Vim untuk Latex
### Motivasi dan Curhat

Tujuan asli dari saya menginstall Ubuntu 22.04 ditahun 2022 ini adalah bagian dari saya berprogres. Sejauh mana saya dapat melangkah di lingkungan yang bisa dibilang jauh dari kata "_melihat lebih jauh_" sebagai anak SMA (ditahun ini saya lulus) saya sendiri tidak terlalu yakin tentang apa yang mau saya capai, apa yang jadi target saya. Tentang apa yang saya upload pertama kali di Github ini adalah karena saya yang hanya sekedar menonton hal-hal tidak berguna di Youtube dan sesuatu muncul diberanda saya yakni tentang programming. Sebenarnya sebelum itu memang saya sudah sedikit tahu tentang hal itu dan sistem operasi yang saya gunakan sebelumnya adalah windows dan IDE-nya `Visual Studio Code.` Saya pun terpukau tentang betapa cantiknya alat yang dia gunakan yah pasti saya mencari tahu apa itu dan itu yah Vim yang sekarang saya gunakan ini. Mencari tahu bagaimana menginstall dan membuat vim milik saya itu seperti miliknya akhirnya membuat saya sedikit putus asa karena Vim itu berbasis terminal yang hanya dapat digunakan disistem operasi Linux dan Mac IOS. Alih-alih saya menginstall VM linux di windows, saya malah ingin bagaimana agar Linux jadi milik saya dan yah tidak lain dan tidak bukan dual boot. Menyakinkan diri saya untuk benar-benar mencoba menginstallnya tanpa pernah mencoba hal tersebut sebelumnya dengan kata lain pertama kali saya menginstall tanpa masalah sama sekali (cukup bangga). Tidak lama dari itu saya mencoba hal yang sangat lazim saya dengar yakni terminal dan seterusnya (ini bakal diteruskan dilain waktu).

### Pengantar
Disini saya akan menjelaskan bagiamana agar Vim dapat digunakan untuk Latex :
- Instalasi
- Konfigurasi

#### 1️⃣ Instalasi
Instalasi menggunakan terminal untuk memunculkan terminal cukup tekan `ctrl+alt+t`
atau dapat dicari di `Show Application` (tanda 9 titik) bisa juga dengan menekan logo windows pada keyboard jika anda menggukan keyboard. 
#### 🌸 Vim
Install Vim menggukanan command 
```bash
sudo apt install vim
```
untuk versi keren dari vim yakni `neovim` yang pada dasarnya sama bisa diinstall dengan command. 
```bash
sudo apt install neovim
```
tapi direpositori ini hanya menjelaskan untuk `vim` saja.
#### 🌸 Distribusi Latex
Install distribusi Latex dikasus ini kita mengggukan `TexLive` yakni distribusi 	
	utama untuk Linux, Windows, dan Mac IOS.
	Untuk installnya menggunakan command. 
  ``` bash
  sudo apt install texlive-full -y
  ```
  itu untuk full instalasi sebesar `5gb` nah untuk basic instalasi menggunakan 
	command.
```bash
sudo apt install texlive -y
```
sebesar sekitar `260mb` saya 
	menyarankan untuk menginstall penuh agar supaya ketika proses pengetikan 
	dokumen di Latex tidak terjadi error karena package yang belum tersedia. 
	Akhirnya akan repot sendiri untuk menginstall manual atau lainnya.
#### 🌸 Keperluan lain
Sebelum konfigurasi perlu dipastikan untuk menginstall hal-hal berikut.
##### Install curl
command 
``` bash 
sudo apt install curl
```
#### Install git 
command
```bash
sudo apt install git
```
##### Install Vim-Plug 
Untuk lebih jelasnya anda dapat membaca tentang [Vim-Plug](https://github.com/junegunn/vim-plug) dulu.
```bash
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```
#### 2️⃣ Konfigurasi 
Untuk konfigurasi disini adalah bagaimana agar `vim` ini bisa digunakan untuk `latex` dan tidak menjelaskan tentang `plug-in` karena itu pilihan dan selera anda sendiri untuk itu anda bisa mengecek tentang [plug-in itu.](https://vimawesome.com/).
#### .vimrc
Untuk bisa menggunakan konfigurasinya ada bisa membuka terminal `ctrl+alt+t` dan mengetikkan `vim .vimrc`. Setelah masuk silahkan ketik `i` untuk insert konfigurasinya. Berikut konfigurasinya.
```bash
" SIMPLE SETTINGS FILE

" STARTUP {{{

let mapleader = " " 
syntax on 	

" }}}
" SET {{{
set relativenumber
set autoindent                               
set linebreak 			             " Wrap lines; last word gets shifted
set mouse=a                          " optional: enable mouse everywhere
set number                           " doesn't get set by default
set spell
set spelllang=en_gb                  " closest to Indian
set wildmenu			             " A menu for tabbing
colorscheme nord


set conceallevel=2		            " conceals math

if exists('+termguicolors')
    set termguicolors              "16 million colours' support
endif

set foldmethod=marker
set encoding=utf8		           " required by VimTeX features

" }}}
" HIGHLIGHT {{{

highlight Conceal guibg=bg 


"}}}
" MAP {{{

nmap <Leader>, :vs $MYVIMRC<CR>
nmap <F5> :w<CR>:source $MYVIMRC<CR>
"nmap <Leader>, :UltiSnipsEdit<CR>

" After installing fzf and wiki
nmap <Leader>ff :Files<CR>
nmap <Leader>fr :History<CR>
nmap <Leader>fh :Helptags<CR>
nmap <Leader>fw <plug>(wiki-fzf-pages)

"Recommended mappings - quick movement between splits 
nmap <C-h> <C-w><C-h>
nmap <C-l> <C-w><C-l>
nmap <C-k> <C-w><C-k>
nmap <C-j> <C-w><C-j>


"}}}
" LET {{{

" UltiSnips {{{2

let g:UltiSnipsExpandTrigger = '<Tab>'
let g:UltiSnipsJumpForwardTrigger = '<Tab>'
let g:UltiSnipsJumpBackwardTrigger = '<S-Tab>'
let g:UltiSnipsEditSplit = 'vertical'
let g:UltiSnipsEnableSnipMate = 0

if has('win32')
    let g:UltiSnipsSnippetDirectories = [$HOME.'\vimfiles\UltiSnips'] "FOR WINDOWS
else
    let g:UltiSnipsSnippetDirectories = [$HOME.'/.vim/UltiSnips'] "FOR THE REST
endif

"}}}
" LaTeX with Vim {{{2

let g:tex_flavor='latex'
let g:vimtex_fold_enabled=1
let g:vimtex_fold_manual=1

"  }}}
" Wiki {{{2

let g:wiki_root = '~/.vim/wiki'        "where are your notes
let g:wiki_link_extension = '.tex'     "what extension
let g:wiki_filetypes = ['tex']         "what format (not always = ext)

" }}}

"}}}
" PLUGINS {{{

call plug#begin('~/.vim/plugged')

Plug 'SirVer/ultisnips'         
Plug 'lervag/vimtex'         

" Essentials:
" Quickly opening files
" Plug 'junegunn/fzf', { 'do': { -> fzf#install() } }   "fuzzy name filter
" Plug 'junegunn/fzf.vim'			       "very quickly open files

" Organizing notes
Plug 'lervag/wiki.vim' 	 " by vimtex author, modular   
"  -------------- OR ----------------------------
" Plug 'fiatjaf/neuron.vim' 	 " simpler; needs neuron - check if you like.

" Extras:
" Plug 'luochen1990/rainbow'	  		" rainbow colours for parentheses
" Plug 'junegunn/goyo.vim' 			    " focused writing
" Plug 'junegunn/limelight.vim'			" super focused writing

" When you get irritated, be sure to look into these
" Plug 'tpope/vim-commentary'     " quickly (un)commenting
" Plug 'tpope/vim-eunuch'         " utility functions
" Plug 'tpope/vim-fugitive'       " for using git
" Plug 'tpope/vim-repeat'         " supercharging dot command
" Plug 'tpope/vim-surround'       " surrounding expressions with [({$ etc.
" Plug 'tpope/vim-unimpaired'     " more utility functions


call plug#end()

"}}}

" YOUR CHANGES 
silent! source ~/.myvimrc         "Add your additions in this file

```
setelah itu anda tekan `esc` agar kembali ke mode normal dan kemudian tekan `shift+:` untuk masuk ke mode command tujuannya untuk menyimpan konfigurasi tadi kemudian ketik `wq` otomatis akan kembali ke tampilan awal terminal dan selesai. 
![vim  vimrc](https://user-images.githubusercontent.com/107534586/174306504-fb262ca2-2989-48a4-b5c6-484c0b3cd009.png)


#### Tes
Untuk mencoba mengetik Latex dengan Vim cukup buka terminal dan ketikkan `vim yang_mau_kau_ketik.tex` contoh `vim kamucantik.tex`. Berikut contoh file yang bisa anda ketik. 
``` tex
documentclass[12pt]{article}

\begin{document}
\begin{center}
	\textbf{Dokumen pertama yang saya ketik dengan latex di vim }\\
	\textit{sangat bangga hahahahahah}\\
\underline{dibuat oleh : Muhammad fadil }
\end{center}
[txt dlm hati : demi apaaa? ah dameyo dame dame]\\

Asli sebenarnya ini ribetnya minta ampun | untung saya |
cuman minesnya di Linux rada susah mau install package yang dibutuhkan untuk menunjang kinerja kita di latex, for example kalo mau buat diagram otomatis pake tizk kan, nulis matematika pun harus pake amsmath-amsfont-amssymb nah itu semua kudu diinstall dulu kalau tidak yah pasti kode tidak jalan dan error pun menyenangkan hati.\\

Problem keduanya adalah kalau masuk semua terpenuhi harus install full distribusinya kataku, kalau diLinux kode terminallnya "sudo apt-get install texlive -full -y" kurang lebih seperti itu lah. \\

Big problemnya adalah ini asli yang paling susah,BAGAIMANA AGAR VIM PUNYA MU ITU BISA TERKONFIGURASI DENGAN LATEX  ini asli yang bikin kepala mu mau menyerah anj, keknya bisa bisa tonji mau belajar tapi harus ko pelajari satu-satu hahaha, kek seperti kalau mau compile file mu harus pake baris kode apa yang kau isi di .vimrc wkwkkwkwkwkwkw belum lagi plug-in - plug-in yang lainnya. (catatan : kalau kau anak youtue yg ada apa apa youtube youtube, sabarko wkwkwk tidak ada perihal ini di youtube dengan kata lain - malas membaca = ngangong-ngangon) \\

Sebenarnya yang paling susah sejauh ini menurutku itu BAGAIMANA CARANYA AGAR APA YANG ADA DALAM SISTEM OPERASI LINUX MU BISA SESUAI DENGAN YANG KAU MAU, asli itu yang paling susah, seperti mau ko isi apa, varna apa, model apa, gaya apa, cara apa, terbang kah, tidur kah, ikon nya kah. apalagi kalau sedikit ji penyimpanan mu habis mi kwwkwk kasusku 8gb untuk linux-swapnya,20gb untuk ext4 / nya, 25 gb untuk home nya, jadi kalau mau ko pake lama mending kasih banyak memang mi, kek saya pusing ma bagaimana caranya tambah partisinya. Intinya itu ji yang bisa kusampaikan sebagai anak yang baru sekali dilinux wkwk tetapi semangat. 



\end{document}
```
![latex with vim](https://user-images.githubusercontent.com/107534586/174306098-7d78ca01-3d1c-41be-80ea-98cd50b4c609.png)

Untuk menampilkan dokumen hasilnya cukup sederhana dengan menyimpan kode latexnya terlebih dulu dengan command `w` dan kemudian kembali ke mode normal dengan `esc` dan ketikkan `\ll` maka dokumen hasil latex akan muncul.

### Kesimpulan
sangat bangga untuk ini setidaknya saya telah melakukannya dan sepertinya akan banyak yang ingin saya tambahkan lebih untuk repositori pertama saya ini hahahaha terlihat seperti blog pada umumnya yang sangat-sangat tidak menggambarkan repositori github. Mungkin saya akan melakukannya dilain waktu saja.


