---
layout: post
title: Blogging Dengan Jekyll
date: 2015-05-06 15:27:31
disqus: y
---

Sebuah permulaan keberanian untuk menulis dan ngeblog dengan Jekyll dan ini adalah variasi baru dalam ngeblog saya dan pertama kali memakai Jekyll, kenapa saya berganti ke jekyll, karena ini blog paling sederhana untuk menulis secara / dengan tipe markdown.

Jekyll adalah blog platform yang dibangun dengan Ruby dan ini pertama kali saya mempelajari Ruby. Sudah banyak yang ahli dan bahkan expert. dengan bahasa Ruby, namun saya masih baru mempelajarinya dan masih acak-acakan hahaha..

Untuk Hosting Jekyll ada banyak yang menyediakan gratis, diantaranya Github dan bisa dijadikan Page contohnya halaman Github Saya dan Layanan lainnya yang menyediakan untuk hosting gratis jekyll adalah Heroku.

Jekyll itu platform Blogging yang sangat seru dimana penulisannya harus menggunakan IDE, dan setelah menulis untuk publish konten menggunakan GIT sangat sulit namun seru, ribet tidak seperti di Wordpress, yang mana setiap nulis bisa langsung publish dengan satu kali klik.
Perubahan Menulis dibanding Wordpress

Untuk Membuat link saja di jekyll harus lengkap dalam penulisannya contoh :

{% highlight ruby %}
[Github Saya](http://nakamuraapp.github.io)
{% endhighlight %}

Bagaimana Cara Upload Jekyll ke Heroku

Masing-masing Jekyll ada beberapa setup namun anda bisa menambahkan code ini di ```_config.yml``` dan di salin dipaling bawah

### Build settings

{% highlight ruby %}
exclude:
 - unicorn.rb
 - README.md
 - Procfile
 - Gemfile
 - Gemfile.lock
 - config.ru
 - vendor
 - app.json
{% endhighlight %}

 anda juga harus menambahkan Procfile di folder ```Project``` anda.

 lalu membuat apps di heroku dengan nama aplikasi blogsaya

{% highlight ruby %}
heroku create blogsaya
git add .
git commit -m "first commit"
git push heroku master
{% endhighlight %}