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
