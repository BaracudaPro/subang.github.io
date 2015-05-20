---
layout: post
title: Cara Upgrade Memory VPS Ubuntu 14 Untuk Upload
date: 2015-05-06 16:27:31
disqus: y
---

Tergantung pada perusahaan web hosting yang Anda pilih dan paket yang Anda pilih , Anda masing-masing akan melihat batas upload file maksimum pada halaman Media Uploader Anda di WordPress . Bagi beberapa itu adalah serendah 2MB yang jelas tidak cukup untuk file media seperti ( audio / video ) . Kebanyakan gambar di bawah 2MB , sehingga baik untuk hanya gambar . Dalam artikel ini , kami akan menunjukkan cara untuk meningkatkan ukuran file upload maksimal di WordPress .

> Catatan : Ini adalah tutorial tingkat menengah . Ini mungkin tidak bekerja dengan beberapa host bersama dalam hal ini Anda harus meminta penyedia layanan hosting Anda untuk dukungan . Kami menggunakan HostGator , dan mereka lebih daripada membantu ketika datang ke masalah seperti ini .

### Theme Functions File

Ada kasus di mana kita telah melihat bahwa hanya dengan menambahkan kode berikut dalam file tema fungsi ini , Anda dapat meningkatkan ukuran upload :

{% highlight ruby %}
@ini_set( 'upload_max_size' , '64M' );
@ini_set( 'post_max_size', '64M');
@ini_set( 'max_execution_time', '300' );
{% endhighlight %}

### Buat atau Ubah PHP.INI file

Dalam kebanyakan kasus jika Anda berada di host bersama , Anda tidak akan melihat file php.ini di direktori Anda . Jika Anda tidak melihat satu , kemudian membuat file bernama php.ini dan meng-upload di folder root. Dalam file yang tambahkan kode berikut :

{% highlight ruby %}
upload_max_filesize = 64M
post_max_size = 64M
max_execution_time = 300
{% endhighlight %}

Metode ini dilaporkan bekerja untuk banyak pengguna . Ingat jika 64 tidak bekerja . Coba 10MB (kadang-kadang pekerjaan itu)

### htaccess Method

Beberapa orang telah mencoba menggunakan metode htaccess mana dengan memodifikasi file .htaccess di root direktori , Anda dapat meningkatkan ukuran upload maksimum di WordPress . Membuka atau membuat file .htaccess di root folder dan tambahkan kode berikut :

{% highlight ruby %}
php_value upload_max_filesize 64M
php_value post_max_size 64M
php_value max_execution_time 300
php_value max_input_time 300
{% endhighlight %}

Sekali lagi , adalah penting bahwa kita menekankan bahwa jika Anda berada di paket shared hosting , maka teknik ini mungkin tidak bekerja . Dalam hal ini, Anda harus menghubungi penyedia hosting web Anda untuk meningkatkan batas untuk Anda . Beberapa host benar-benar menolak pengguna mereka . Kami menyarankan Anda menggunakan HostGator . Orang dukungan mereka sangat membantu dalam situasi ini 