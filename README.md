# Project Title

Belajar membuat docker image dengan dockerfile menggunakan github workflow

## Getting Started

Disini kita belajar mensimulasikan sebuah project, dimana setiap kali continuous integration tertrigger di workflow, dockerfile akan membuat image dari changes terakhir, dan menguploadnya secara otomatis ke docker hub registry.

### Prerequisites

Yang dibutuhkan:

* Folder sample berisi project (disini bernama web_dir)
* Dockerfile untuk membuat image
* https://hub.docker.com/ account (buat gratis)
* https://hub.docker.com/ remote repository (buat gratis)
* Secret action variable untuk menyimpan akun docker hub di github repository

### Step

Ikuti langkah berikut:


* Buat aku di docker hub 
* Buat dockerfile (seperti contoh di repo ini)
* Buat folder project (contoh disini folder web_dir)
* Buat workflow file (contoh disini docker-image.yaml)
* Save username, password, dan nama repo dockerhub nya, kedalam "secret" variable di github, sesuai nama variable didalam file docker-image.yaml


## Usage

Yang terjadi saat terjadi merge,

* workflow tertrigger
* github login ke akun dockerhub menggunakan username dan password yang telah anda disimpan ke secret sebelumnya
* workflow membuild sebuah docker image menggunakan dockerfile dari project directory
* jika sukses, workflow akan mengupload image yang sudah terbuild, ke dockerhub registry sesuai nama repo dockerhub yg disimpan di secret variable.


### Credit

* [suyog shinde - Medium](https://medium.com/nonstopio/part-1-github-actions-docker-hub-versioning-continous-integrations-142cbd95fe0b)
